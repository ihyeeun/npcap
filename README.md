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
9. 해결방안 [속성페이지 - 구성관리자] 에서 x64로 바꿔주니 에러가 사라짐
10. 디버그 하니 인터페이스 목록 출력
11. 내가 현재 쓰는 와이파이 목록이 무엇인지 알아내려면 [제어판\네트워크 및 인터넷\네트워크 및 공유 센터 -> 어댑터 설정변경] 누르면 확인가능
12. 이 원시 데이터를 어떻게 네트워크 목록별로 분류할건지 .. 그거 알아내야할듯 
