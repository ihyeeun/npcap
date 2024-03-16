# npcap -> 네트워크 원시 데이터에 접근하기 위해 필요

1. npcap 설치 (아래 두개 설치)
  ㆍ  Npcap 1.79 installer for Windows 7/2008R2, 8/2012, 8.1/2012R2, 10/2016, 2019, 11 (x86, x64, and ARM64).
  ㆍ  Npcap SDK 1.13 (ZIP).   #lib / include 파일 옮기기 위해서 필수로 받아두기 / 압축도 풀어두기

2. installer 다운로드 받으면 클릭해서 옵션 선택 다하고 넘어가기
  Restrict Npcap driver's access to Adminitrators only -> 관리자 권한을 줘야하기에 필수로 선택  
  install Npcap in Winpcap API-compatible Mode 옵션 선택후 다음으로 ( 그냥 다 선택하고 넘어가기 )

3. install 완료되면 c:\npcap\Lib + Include 복붙해놓기 (중요!!)

4. 다운로드 받은 sdk\Examples-pcap\Make-All 열기
  
5. basic_dump에서 [ 프로젝트 - 속성 ] 에서 구성 : 활성(Debug) / 플랫폼 : x64 로 설정 한뒤 [VC++ 디렉토리] 들어가서
6. 외부 include 디렉터리에 C:\npcap\Include 링크 복붙 마지막에 ; 붙여주기
7. 라이브 디렉터리에는 C:\npcap\Lib\x64 복붙해서 마지막 ;

8. 재부팅하기? 왜냐면 난 실행이 안돼 ..
