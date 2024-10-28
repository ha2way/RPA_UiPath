| 과제명 | 외교부레포트 |
|:---:|:---|
| 항목 | 기술 |
| 작업기간 | 2024. 10. 11.  ~  2024. 10. 13. |
| 주요업무 및 상세내용 |• 외교부 월별 세출집행현황 데이터를 추출 및 가공 자동화
• 기간 데이터를 검색하여, 각각의 엑셀 시트에 복제하여 기입
  - Config 활용, 기입 시 당월집행액(원)이 0원인 Row는 삭제
• 해당 월에 검색 결과가 없는 경우 Process Transaction에서 BRE 처리하여   
  시트에 기입 하지 않음, 매칭 실패 아이템 처리
• <종합>시트에 월별 당월집행액의 총계를 입력.
• 결과 파일을 첨부하여 RPA 메일 발송
- 매칭 성공 아이템과 실패 아이템 삽입
- 당월집행액이 0원인 데이터를 취합하여 본문에 DT(HTML)로 입력 |
| 사용언어 및 개발환경 | • Tool : UiPath Studio Community
• Framework : Robotic Enterprise Framework
• Language : VB.NET
• OS : Windows 11| 느낀점 |Process Transaction에서 BRE 처리하여 매칭 실패 아이템 처리를 경험하였습니다. Modern의 Excel Process Scope, Use Excel File 액티비티를 사용한 엑셀 문서 가공 처리를 경험하였고 그 과정에서 Find First/Last Data Row, Format Cells, Write Cell 등의 다양한 액티비티를 활용하며 엑셀 시트 가공을 수행할 수 있었습니다.
| 소스레포(코드 등) | https://github.com/JsName/RPA-UiPath<br>https://www.uipath.com |
