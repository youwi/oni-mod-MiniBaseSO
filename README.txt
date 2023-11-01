开始:

Nuget下载: 
  Plib
  ILmerge
  ILrepack


# 配置脚本:
(项目:属性-生成事件)


$(SolutionDir)\packages\ilmerge.3.0.41\tools\net452\ILMerge.exe 
/lib:"C:\Program Files (x86)\Steam\steamapps\common\OxygenNotIncluded\OxygenNotIncluded_Data\Managed" 
/out:MiniBase-merged.dll /targetplatform:v4,C:\Windows\Microsoft.NET\Framework64\v4.0.30319 $(TargetPath) $(SolutionDir)\packages\PLib.4.13.0\lib\net471\PLib.dll

copy "$(TargetDir)\MiniBase-merged.dll" "%USERPROFILE%\Documents\Klei\OxygenNotIncluded\mods\local\MiniBase\$(TargetFileName)"
REM copy "$(TargetDir)\MiniBase.dll" "%USERPROFILE%\Documents\Klei\OxygenNotIncluded\mods\local\MiniBase\$(TargetFileName)"
copy "$(TargetDir)\mod.yaml" %USERPROFILE%\Documents\Klei\OxygenNotIncluded\mods\local\MiniBase\mod.yaml
copy "$(TargetDir)\mod_info.yaml" %USERPROFILE%\Documents\Klei\OxygenNotIncluded\mods\local\MiniBase\mod_info.yaml