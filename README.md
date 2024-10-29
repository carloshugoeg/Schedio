Libreria de lectura de pdfs: dotnet add package UglyToad.PdfPig --prerelease
Libreria para google calendar: dotnet add package Google.Apis.Calendar.v3

Pasos para correr desde Visual Code:
![alt text](<WhatsApp Image 2024-10-29 at 01.00.48_0acb0199.jpg>)
![alt text](<WhatsApp Image 2024-10-29 at 01.00.48_0acb0199-1.jpg>)
Deberia creiar una carpeta llamada .vscode y un archivo json que se llama launch, en ese archivo pegar
{
    // Use IntelliSense to learn about possible attributes.
    // Hover to view descriptions of existing attributes.
    // For more information, visit: https://go.microsoft.com/fwlink/?linkid=830387
    "version": "0.2.0",
    "configurations": [
        {
            "name": ".NET Core Launch (web)",
            "type": "coreclr",
            "request": "launch",
            "preLaunchTask": "build",
            "program": "${workspaceFolder}/bin/Debug/net6.0/<NombreProyecto>.dll",
            "args": [],
            "cwd": "${workspaceFolder}",
            "stopAtEntry": false,
            "serverReadyAction": {
                "action": "openExternally",
                "pattern": "\\bNow listening on:\\s+(https?://\\S+)"
            },
            "env": {
                "ASPNETCORE_ENVIRONMENT": "Development"
            },
            "sourceFileMap": {
                "/Views": "${workspaceFolder}/Views"
            }
        }
    ]
}
Luego dentro de esa misma carpeta crear otro archivo json que se llame tasks.json y pegar:
{
    "version": "2.0.0",
    "tasks": [
        {
            "label": "build",
            "command": "dotnet",
            "type": "process",
            "args": [
                "build",
                "${workspaceFolder}"
            ],
            "problemMatcher": "$msCompile"
        }
    ]
}
luego abrir una terminal y dar el comando "cd hackaton"
dar el comando "dotnet build"
dar el comando "dotnet run"
para ver la pagina web ingresar al navegador a http://localhost:5025/

IMPORTANTE: 
cuando se haga un cambio hay que darle dotnet run a la terminal para recargar la pagina web para ver los cambios