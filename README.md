# jp.conda
Jaeyong's personal conda virtual environments setting project
-------------------------------
#### This project contains many virtual environment requirements files. If you want to do one of the projects in the jp project group, setting up your environment through the requirements.yml file containing the right conda envs is the best way to do the project and avoid conflicts.

#### For more information on setting up conda virtual environment, see the description below.

> 1. Launch Anaconda Prompt & Move Project Directory
>```
>>cd "your_conda_project_directory"
>```
> 2. Create Conda Virtual Enviroment
>```
>conda env create -f "your_conda_requirements.yml"
>```
> 3. Conda Virtual Enviroment Activate
>```
>conda activate "your_enviroment_name"
>```

#### If you want to make it easy for project participants to configure conda virtual envs through batch files, follow the instructions below.

> 1. Create "conda_install.bat" file (select from 1.1 or 1.2)
>> 1.1. "conda_install.bat" for initial install
>```
>set root=%USERPROFILE%
>set CURPATH=%cd%
>
>call %root%\Anaconda3\Scripts\activate.bat
>
>cd %CURPATH%
>
>call conda env create -f "your_conda_requirements.yml"
>
>exit
>```
>> 1.2. "conda_update.bat" for update conda virtual envs
>```
>set root=%USERPROFILE%
>set CURPATH=%cd%
>
>call %root%\Anaconda3\Scripts\activate.bat
>
>cd %CURPATH%
>
>call conda activate "your_enviroment_name"
>call conda env update -f "your_conda_requirements.yml" --prune
>
>exit
>```
> 2. Run git bash where conda project is located
>```
>start "your_install_batch_file"
>```

