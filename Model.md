## Model

```bash
# 병원
rails g model hospital ykiho yadmnm clcd:integer sidocd:integer sggucd:integer addr telno hospurl drtotcnt:integer gdrcnt:integer intncnt:integer resdntcnt:integer sdrcnt:integer xpos:float ypos:float
# 병원코드 병원명 종별코드 종별코드 시도코드 시군구코드 주소 전화번호 사이트주소 의사총수 일반의의원수 인턴수 x좌표 y좌표

# 코드정보(시도) // 병원1 : 코드정보(시도)N
rails g model codesi sidocd:integer sidocdnm
#시도코드 시도코드명

# 코드정보(시군구) // 병원1 : 코드정보(시군구)N
rails g model codesg sggucd:integer sggucdnm
#시군구코드 시군구코드명

#코드정보(종별) // 병원1 : 코드정보(종별)N
rails g model codecl clcd:integer clcdnm
#종별코드 종별코드명
# 종류 : 상급종합, 종합병원, 병원, 요양병원, 의원, 보건소, 보건의료원, 보건지소, 보건진료소, 의원, 치과병원, 치과의원 

#진료과목(각 column이름은 코드정보(진료과목)에 써져 있음) // 병원1 : 코드정보N
rails g model hospsbj ykiho dg01:integer dg02:integer dg03:integer dg04:integer dg05:integer dg06:integer dg07:integer dg08:integer dg09:integer dg10:integer dg11:integer dg12:integer dg13:integer dg14:integer dg15:integer dg16:integer dg17:integer dg18:integer dg19:integer dg20:integer	dg21:integer dg22:integer dg23:integer dg24:integer dg25:integer dg26:integer dg50:integer dg51:integer dg52:integer dg53:integer dg54:integer dg55:integer dg56:integer dg57:integer dg58:integer dg59:integer

#코드정보(진료과목)
rails g model codesub dgsbjtcd dgsbjtcdnm
# 01:내과 02:신경과 03:정신건강의학과 04:외과 05:정형외과 06:신경외과 07:흉부외과 08:성형외과 09:마취통증의학과 10:산부인과 11:소아청소년과 12:안과 13:이비인후과 14:피부과 15:비뇨의학과 16:영상의학과 17:방사선종양학과 18:병리과 19:진단검사의학과 21:재활의학과 22:핵의학과 23:가정의학과 24:응급의학과 25:직업환경의학과 26:예방의학과 49:치과 50:구강악안면외과 51:치과보철과 52:치과교정과 53:소아치과 54:치주과 55:치과보존과 56:구강내과 57:영상치의학과 58:구강병리과 59:예방치과

# 비급여
rails g model noncondition mainclass middleclass hospname ykiho price:integer hostday:float
# 대분류 중분류 소분류(수술이름) 병원코드 평균가격 평균입원일수

# 병원평가
rails g model hospeval ykiho asmgrd11 asmgrd12 asmgrd13
# 병원코드 항생제처방율 주사제처방율 약품품목수

# 수가기준에서 진료수가의 목록 및 급여 파악하기

#질병
rails g model disease ykiho shwsbjtcdnm mf1 mf2 mf3 mf4 mf5 
# 병원기호 병원과 1위병 2위 3위 4위 5위 (없는 경우 빈칸)
# 과 종류 : 가정의학과 내과 마취통증의학과 비뇨기과 산부인과 성형외과 소아청소년과 신경과 신경외과 안과 외과 이비인후과 일반의 재활의학과 정신건강의학과 정형외과 영상의학과 피부과 흉부외과
```

