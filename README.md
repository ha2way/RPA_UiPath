| 과제명 | 의약품 안전나라 |
|:---:|:---|
| 항목 | 기술 |
| 작업기간 | 2024. 10. 17.  ~  2024. 10. 22. |
| 주요업무 및 상세역할 |• 의약품 사이트에 접속하여 취합한 자료 중 이슈 내역을 담당자에게 공유<br>
• 품목구분 및 조회기간 설정 (의약품 등, 메일에 주어진 기간)<br>
• 템플릿 파일의 양식에 맞게 추출한 ‘전체DT’를 당월시트에 입력<br>
• ‘전체DT’ 중 키워드가 포함된 내용만 추출하여 이슈사항 시트에 입력<br>
• 이슈사항시트의 내용 중 처분일자가 당월인 것만 필터링하여 당월이슈시트
  에 입력<br>
• 결과 파일을 첨부하여 RPA 메일 발송 |
| 사용언어 및 개발환경 | • Tool : UiPath Studio Community<br>• Framework : Robotic Enterprise Framework<br>• Language : VB.NET<br>• OS : Windows 11 |
| 느낀점 | TransactionItem을 어떤 요소로 설정해야 하는지 고민하며 로직을 구성해볼 수 있었습니다. 제시된 이슈 내역 추출을 위해 이중 for문을 사용하였고, 첨부파일이 없는 경우 No data 처리하여 Exception 관리를 할 수 있었습니다. |
| 소스자료(링크 등) | https://github.com/ha2way/RPA_UiPath<br>https://haway.tistory.com/ |

| 과제명 | 외교부레포트 |
|:---:|:---|
| 항목 | 기술 |
| 작업기간 | 2024. 10. 11. ~ 2024. 10. 13. |
| 주요업무 및 상세역할 | • 외교부 월별 세출집행현황 데이터를 추출 및 가공 자동화<br>• 기간 데이터를 검색하여, 각각의 엑셀 시트에 복제하여 기입<br> - Config 활용, 기입 시 당월집행액(원)이 0원인 Row는 삭제<br>• 해당 월에 검색 결과가 없는 경우 Process Transaction에서 BRE 처리하여 시트에 기입 하지 않음, 매칭 실패 아이템 처리<br>• <종합>시트에 월별 당월집행액의 총계를 입력<br>• 결과 파일을 첨부하여 RPA 메일 발송<br> - 매칭 성공 아이템과 실패 아이템 삽입<br> - 당월집행액이 0원인 데이터를 취합하여 본문에 DT(HTML)로 입력 |
| 사용언어 및 개발환경 | • Tool : UiPath Studio Community<br>• Framework : Robotic Enterprise Framework<br>• Language : VB.NET<br>• OS : Windows 11 |
| 느낀점 | Process Transaction에서 BRE 처리하여 매칭 실패 아이템 처리를 경험하였습니다. Modern의 Excel Process Scope, Use Excel File 액티비티를 사용한 엑셀 문서 가공 처리를 경험하였고 그 과정에서 Find First/Last Data Row, Format Cells, Write Cell 등의 다양한 액티비티를 활용하며 엑셀 시트 가공을 수행할 수 있었습니다. |
| 소스자료(링크 등) | https://github.com/ha2way/RPA_UiPath<br>https://haway.tistory.com/ |


| 과제명 | 견적서메일발송 |
|:---:|:---|
| 항목 | 기술 |
| 작업기간 | 2024. 10. 02. ~ 2024. 10. 07. |
| 주요업무 및 상세역할 | • 매월 수신 후 작업 지시서 물품의 견적서를 작성하여 메일 보내기 자동화<br>• 작업지시서 파일이 없다면 BusinessRuleException으로 Throw 처리<br>• 물품구매 사이트에서 작업지시서의 물품 코드를 검색<br>- 검색 전 장바구니를 비우고 시작하는 로직<br>- 품절 된 상품 처리<br>- 검색 결과가 복수인 상품 처리<br>• 검색하여 나온 물품의 수량을 작업지시서대로 입력하여 장바구니에 담음<br>• 장바구니 페이지에서 견적서를 클릭하여 PDF파일로 생성<br>• 생성한 PDF파일을 첨부하여 메일 발송 |
| 사용언어 및 개발환경 | • Tool : UiPath Studio Community<br>• Framework : Robotic Enterprise Framework<br>• Language : VB.NET<br>• OS : Windows 11 |
| 느낀점 | TransactionItem 반복에 대해 고려하면서 반복 전 Initialization 단계에서 장바구니를 비우고 시작하는 로직에 대해 설계할 수 있었습니다. 품절 상품 및 복수 검색 상품에 대한 처리 과정을 경험하며 다양한 상황 발생에 대응하는 설계를 고려해야했다고 생각하였습니다. |
| 소스자료(링크 등) | https://github.com/ha2way/RPA_UiPath<br>https://haway.tistory.com/ |

| 과제명 | 티켓랭킹 |
|:---:|:---|
| 항목 | 기술 |
| 작업기간 | 2024. 09. 12. |
| 주요업무 및 상세역할 | • 항목별 티켓랭킹 데이터를 추출하여 엑셀파일로 저장 후 메일발송 자동화<br>• 메일을 수신 후 날짜 추출, 추출항목을 문자열 가공을 통하여 추출<br>• 티켓랭킹 사이트에서 추출항목에 해당하는 내용을 DataTable로 추출하여 엑셀에 저장<br>- 1-3위/ 4-50위 개별 추출 후 Merge Data Table 액티비티 사용<br>• 메일본문에 처리 항목의 성공/실패 여부를 기재<br>• 각 항목의 1위 데이터를 취합하여 메일 본문에 DT(HTML)로 삽입<br>• String Format을 사용하여 본문 기입하여 메일 발송 |
| 사용언어 및 개발환경 | • Tool : UiPath Studio Community<br>• Framework : Robotic Enterprise Framework<br>• Language : VB.NET<br>• OS : Windows 11 |
| 느낀점 | 작업 사이트에서 데이터 추출을 진행할 때 1-3위와 4-50위의 형태가 달라서 한 번에 추출할 수 없었습니다. 각각 추출 후 Merge Data Table 액티비티를 사용하여 하나의 데이터 테이블로 만들어 작업을 수행할 수 있었습니다. |
| 소스자료(링크 등) | https://github.com/ha2way/RPA_UiPath<br>https://haway.tistory.com/ |

| 과제명 | 부동산공시가격 |
|:---:|:---|
| 항목 | 기술 |
| 작업기간 | 2024. 09. 09. ~ 2024. 09. 11. / 2024. 09. 25. ~ 2024. 09. 26. |
| 주요업무 및 상세역할 | • 부동산 공시가격을 추출하여 기존데이터와 비교 자동화 프로젝트<br>• 엑셀파일을 읽어서 TransactionData 생성<br>• 시, 구, 도로명, 단지명, 동, 호 순차적 검색을 위한 if 분기 처리<br>• 부동산공시가격 사이트에서 주소에 해당하는 공시기준일과 공시가준일 가격을 추출하여 기입<br>• 가격을 비교하여 상승, 하락, 상승, 정보없음 기입<br>• 결과 파일을 첨부하여 메일 발송 |
| 사용언어 및 개발환경 | • Tool : UiPath Studio Community<br>• Framework : Robotic Enterprise Framework<br>• Language : VB.NET<br>• OS : Windows 11 |
| 느낀점 | 읽어온 엑셀파일의 데이터와 사이트에서 추출, 해야하는 주소에서의 불일치를 처리하기 위한 다양한 분기를 통한 예외처리를 경험할 수 있었습니다. 최대한 TransactionItem을 정상 처리할 수 있도록 노력하고 그 외의 부분은 임의로 처리하지 않고 Throw처리를 하거나 담당자와 논의 후 처리해야 함을 배울 수 있었습니다. |
| 소스자료(링크 등) | https://github.com/ha2way/RPA_UiPath<br>https://haway.tistory.com/ |
