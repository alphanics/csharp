# 빌드이벤트

## 빌드 전 이벤트 명령줄
if not exist "$(TargetDir)\Dll" mkdir "$(TargetDir)\Dll"

## 빌드 후 이벤트 명령줄
move "$(TargetDir)\*.dll" "$(TargetDir)\Dll"
del "$(TargetDir)\*.xml"
RD /S /Q "$(TargetDir)\de"
RD /S /Q "$(TargetDir)\es"
RD /S /Q "$(TargetDir)\ja"
RD /S /Q "$(TargetDir)\ru"

## 위와 같이 처리시 Dll참조 경로를 app.conifg에도 참조 경로 관련 구문 추가해줘야함

```xml
  <runtime>
    <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
      <probing privatePath="dll" />
    </assemblyBinding>
  </runtime>
```



