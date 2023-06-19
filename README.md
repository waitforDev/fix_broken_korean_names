### 스크립트 작업 내용:

1. 사용자가 지정한 디렉토리를 기준으로 하위의 모든 파일과 디렉토리를 대상으로 작업을 수행합니다.
1. 각 파일과 디렉토리의 이름을 확인하며, 이 이름들 중에서 한글 초성, 중성, 종성이 분리된 문자열이 있다면 이를 원래의 한글 문자로 복원합니다. 이 과정에서 Unicode 정규화(Normalization)를 이용하여 분리된 한글 문자들을 병합합니다.
1. 복원된 한글 문자열을 CP949 인코딩으로 변환하여, 윈도우 시스템에서 제대로 표시되도록 합니다.
1. 파일과 디렉토리 이름을 변경하는 동안, 윈도우 시스템에서 사용할 수 없는 문자나 제어 문자는 제거하며, 파일 이름 끝의 점('.')도 제거합니다.

이 작업은 리눅스나 유닉스 기반 시스템에서 생성된 한글 파일이나 디렉토리를 윈도우 시스템으로 옮겼을 때 발생하는 이름 깨짐 현상을 해결하는 데 도움이 됩니다.

### 실행 방법

이 스크립트는 단일 파일로 구성되어 있으므로, 다음과 같이 실행할 수 있습니다.

```bash
python fix_broken_korean_names.py <디렉토리명>
```

- `<디렉토리명>`은 작업을 수행할 대상 디렉토리의 경로입니다.

---

### This script performs the following tasks:

1. It operates on all files and directories beneath the directory specified by the user.
1. It checks the names of each file and directory. If there are Korean characters in those names that are broken into consonants and vowels, it restores them to the original Korean characters. In this process, it uses Unicode normalization to combine the separated Korean characters.
1. It converts the restored Korean strings into CP949 encoding so they are properly displayed on the Windows system.
1. During the renaming of the files and directories, it removes any characters that can't be used in Windows system and control characters. It also removes periods ('.') at the end of file names.

This script can help solve the issue of name breakage that occurs when Korean files or directories created on a Linux or Unix-based system are transferred to a Windows system.

### Usage

This script is a single file, and it can be executed as follows:

```bash
python fix_broken_korean_names.py <directory>
```

- `<directory>` is the path to the target directory on which the script will perform the operations.
