```uml
@startuml
@startuml
start
:weather;
if(weather) then (0)
:快晴です;
endif
if(weather) then (1)
:曇りです;
endif
if(weather) then (2)
:雨です;
else (その他)
:不明です;
endif
end
@enduml
@enduml
```
