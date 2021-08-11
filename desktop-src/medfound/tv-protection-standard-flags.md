---
description: 下表中的常數指定輸出保護管理員 (OPM) 的電視標準及格式。
ms.assetid: 8f26aa92-ed40-483e-ac78-c071619f0e12
title: '電視保護標準旗標 (Opmapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf739e9ec2fc93f427891e2e841d7dc77049eb5d878028372b2c7757f536169
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118237577"
---
# <a name="tv-protection-standard-flags"></a>電視防護標準旗標

下表中的常數指定輸出保護管理員 (OPM) 的電視標準及格式。



| 常數/值                                                                                                                                                                                                                                                                                                              | 描述                                                    |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------|
| <span id="OPM_PROTECTION_STANDARD_OTHER"></span><span id="opm_protection_standard_other"></span><dl> <dt>**OPM \_保護 \_ 標準 \_ 其他**</dt> <dt>0x80000000</dt> </dl>                                             | 保護標準未知。<br/>                 |
| <span id="OPM_PROTECTION_STANDARD_NONE"></span><span id="opm_protection_standard_none"></span><dl> <dt>**OPM \_保護 \_ 標準 \_ 無**</dt> <dt>0x00000000</dt> </dl>                                                | 未準備好任何保護標準。<br/>                 |
| <span id="OPM_PROTECTION_STANDARD_IEC61880_525I"></span><span id="opm_protection_standard_iec61880_525i"></span><dl> <dt>**OPM \_保護 \_ 標準 \_ IEC61880 \_ 525I**</dt> <dt>0x00000001</dt> </dl>                    | 保護標準是 IEC 61880、525i。<br/>         |
| <span id="OPM_PROTECTION_STANDARD_IEC61880_2_525I"></span><span id="opm_protection_standard_iec61880_2_525i"></span><dl> <dt>**OPM \_保護 \_ 標準 \_ IEC61880 \_ 2 \_ 525I**</dt> <dt>0x00000002</dt> </dl>             | 保護標準是 IEC 61880-2、525i。<br/>       |
| <span id="OPM_PROTECTION_STANDARD_IEC62375_625P"></span><span id="opm_protection_standard_iec62375_625p"></span><dl> <dt>**OPM \_保護 \_ 標準 \_ IEC62375 \_ 625P**</dt> <dt>0x00000004</dt> </dl>                    | 保護標準是 IEC 62375、625p。<br/>         |
| <span id="OPM_PROTECTION_STANDARD_EIA608B_525"></span><span id="opm_protection_standard_eia608b_525"></span><dl> <dt>**OPM \_保護 \_ 標準 \_ EIA608B \_ 525**</dt> <dt>0x00000008</dt> </dl>                          | 保護標準為 EIA/CEA-608-B、525i。<br/>     |
| <span id="OPM_PROTECTION_STANDARD_EN300294_625I"></span><span id="opm_protection_standard_en300294_625i"></span><dl> <dt>**OPM \_保護 \_ 標準 \_ EN300294 \_ 625I**</dt> <dt>0x00000010</dt> </dl>                    | 保護標準為 ETSI EN 300 294、625i。<br/>   |
| <span id="OPM_PROTECTION_STANDARD_CEA805A_TYPEA_525P"></span><span id="opm_protection_standard_cea805a_typea_525p"></span><dl> <dt>**OPM \_保護 \_ 標準 \_ CEA805A \_ TYPEA \_ 525P**</dt> <dt>0x00000020</dt> </dl>    | 保護標準為 CEA-805-A Type A，525p。<br/>  |
| <span id="OPM_PROTECTION_STANDARD_CEA805A_TYPEA_750P"></span><span id="opm_protection_standard_cea805a_typea_750p"></span><dl> <dt>**OPM \_PROTECTION \_ STANDARD \_ CEA805A \_ TYPEA \_ 750P**</dt> <dt>0x00000040</dt> </dl>    | 保護標準為 CEA-805-A Type A，750p。<br/>  |
| <span id="OPM_PROTECTION_STANDARD_CEA805A_TYPEA_1125I"></span><span id="opm_protection_standard_cea805a_typea_1125i"></span><dl> <dt>**OPM \_PROTECTION \_ STANDARD \_ CEA805A \_ TYPEA \_ 1125I**</dt> <dt>0x00000080</dt> </dl> | 保護標準為 CEA-805-A Type A，1125i。<br/> |
| <span id="OPM_PROTECTION_STANDARD_CEA805A_TYPEB_525P"></span><span id="opm_protection_standard_cea805a_typeb_525p"></span><dl> <dt>**OPM \_PROTECTION \_ STANDARD \_ CEA805A \_ TYPEB \_ 525P**</dt> <dt>0x00000100</dt> </dl>    | 保護標準為 CEA-805-A Type B，525p。<br/>  |
| <span id="OPM_PROTECTION_STANDARD_CEA805A_TYPEB_750P"></span><span id="opm_protection_standard_cea805a_typeb_750p"></span><dl> <dt>**OPM \_PROTECTION \_ STANDARD \_ CEA805A \_ TYPEB \_ 750P**</dt> <dt>0x00000200</dt> </dl>    | 保護標準為 CEA-805-A Type B，750p。<br/>  |
| <span id="OPM_PROTECTION_STANDARD_CEA805A_TYPEB_1125I"></span><span id="opm_protection_standard_cea805a_typeb_1125i"></span><dl> <dt>**OPM \_PROTECTION \_ STANDARD \_ CEA805A \_ TYPEB \_ 1125I**</dt> <dt>0x00000400</dt> </dl> | 保護標準為 CEA-805-A Type B，1125i。<br/> |
| <span id="OPM_PROTECTION_STANDARD_ARIBTRB15_525I"></span><span id="opm_protection_standard_aribtrb15_525i"></span><dl> <dt>**OPM \_保護 \_ 標準 \_ ARIBTRB15 \_ 525I**</dt> <dt>0x00000800</dt> </dl>                 | 保護標準為 ARIB TR-B15、525i。<br/>       |
| <span id="OPM_PROTECTION_STANDARD_ARIBTRB15_525P"></span><span id="opm_protection_standard_aribtrb15_525p"></span><dl> <dt>**OPM \_保護 \_ 標準 \_ ARIBTRB15 \_ 525P**</dt> <dt>0x00001000</dt> </dl>                 | 保護標準為 ARIB TR-B15、525p。<br/>       |
| <span id="OPM_PROTECTION_STANDARD_ARIBTRB15_750P"></span><span id="opm_protection_standard_aribtrb15_750p"></span><dl> <dt>**OPM \_保護 \_ 標準 \_ ARIBTRB15 \_ 750P**</dt> <dt>0x00002000</dt> </dl>                 | 保護標準為 ARIB TR-B15、750p。<br/>       |
| <span id="OPM_PROTECTION_STANDARD_ARIBTRB15_1125I"></span><span id="opm_protection_standard_aribtrb15_1125i"></span><dl> <dt>**OPM \_保護 \_ 標準 \_ ARIBTRB15 \_ 1125I**</dt> <dt>0x00004000</dt> </dl>              | 保護標準為 ARIB TR-B15、1125i。<br/>      |



## <a name="remarks"></a>備註

這些旗標的數值相當於認證輸出保護通訊協定 (COPP) 中所使用的 **COPP \_ TVProtectionStandard** 列舉。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Opmapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎常數](media-foundation-constants.md)
</dt> <dt>

[**OPM \_ 設定 \_ ACP \_ 和 \_ CGMSA \_ 信號**](opm-set-acp-and-cgmsa-signaling.md)
</dt> <dt>

[OPM \_ 取得 \_ ACP \_ 和 \_ CGMSA \_ 信號](opm-get-acp-and-cgmsa-signaling.md)
</dt> </dl>

 

 




