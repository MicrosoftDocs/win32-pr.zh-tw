---
description: 限制要設定或傳回之資料的旗標。
title: 'SRRF (Shlwapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: c9dbffd1-3b3e-4a25-89ee-1666e2812a62
api_name:
- SRRF_RT_REG_NONE
- SRRF_RT_REG_SZ
- SRRF_RT_REG_EXPAND_SZ
- SRRF_RT_REG_BINARY
- SRRF_RT_REG_DWORD
- SRRF_RT_REG_MULTI_SZ
- SRRF_RT_REG_QWORD
- SRRF_RT_DWORD
- SRRF_RT_QWORD
- SRRF_RT_ANY
- SRRF_RM_ANY
- SRRF_RM_NORMAL
- SRRF_RM_SAFE
- SRRF_RM_SAFENETWORK
- SRRF_NOEXPAND
- SRRF_ZEROONFAILURE
- SRRF_NOVIRT
api_type:
- HeaderDef
api_location:
- Shlwapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3ba36b64496413a54e6d8b8b96c16c265367d05c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026904"
---
# <a name="srrf"></a>SRRF

限制要設定或傳回之資料的旗標。



| 常數/值                                                                                                                                                                                                                                           | Description                                                                                                                                                                                                            |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SRRF_RT_REG_NONE"></span><span id="srrf_rt_reg_none"></span><dl> <dt>**SRRF \_RT \_ REG \_ NONE**</dt> <dt>0x00000001</dt> </dl>                 | 輸入 REG \_ NONE。<br/>                                                                                                                                                                                             |
| <span id="SRRF_RT_REG_SZ"></span><span id="srrf_rt_reg_sz"></span><dl> <dt>**SRRF \_RT \_ REG \_ SZ**</dt> <dt>0x00000002</dt> </dl>                       | 輸入 REG \_ SZ。 \_ \_ \_ 除非指定了 SRRF NOEXPAND 旗標，否則 REG EXPAND sz 類型會自動轉換為 REG SZ \_ 。<br/>                                                                                     |
| <span id="SRRF_RT_REG_EXPAND_SZ"></span><span id="srrf_rt_reg_expand_sz"></span><dl> <dt>**SRRF \_RT \_ REG \_ EXPAND \_ SZ**</dt> <dt>0x00000004</dt> </dl> | 輸入 REG \_ EXPAND \_ SZ。 如果要取得值，您也必須取得 SRRF \_ NOEXPAND 旗標，否則 [**SHRegGetValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetvaluea) 會失敗，並出現錯誤 \_ \_ 參數無效。<br/>                                     |
| <span id="SRRF_RT_REG_BINARY"></span><span id="srrf_rt_reg_binary"></span><dl> <dt>**SRRF \_RT \_ REG \_ BINARY**</dt> <dt>0x00000008</dt> </dl>           | 輸入 REG \_ BINARY。<br/>                                                                                                                                                                                           |
| <span id="SRRF_RT_REG_DWORD"></span><span id="srrf_rt_reg_dword"></span><dl> <dt>**SRRF \_RT \_ REG \_ DWORD**</dt> <dt>0x00000010</dt> </dl>              | 輸入 REG \_ DWORD。<br/>                                                                                                                                                                                            |
| <span id="SRRF_RT_REG_MULTI_SZ"></span><span id="srrf_rt_reg_multi_sz"></span><dl> <dt>**SRRF \_RT \_ REG \_ 多重 \_ SZ**</dt> <dt>0x00000020</dt> </dl>    | 輸入 REG \_ 多重 \_ SZ。<br/>                                                                                                                                                                                        |
| <span id="SRRF_RT_REG_QWORD"></span><span id="srrf_rt_reg_qword"></span><dl> <dt>**SRRF \_RT \_ REG \_ QWORD**</dt> <dt>0x00000040</dt> </dl>              | 輸入 REG \_ QWORD。<br/>                                                                                                                                                                                            |
| <span id="SRRF_RT_DWORD"></span><span id="srrf_rt_dword"></span><dl> <dt>**SRRF \_RT \_ DWORD**</dt> <dt>0x00000018</dt> </dl>                           | REG \_ DWORD 和32位 reg \_ 二進位類型。 這相當於 SRRF \_ rt \_ reg \_ BINARY \| SRRF \_ rt \_ reg \_ DWORD。 如果要抓取值，如果值的二進位資料大於32位，則不會傳回。<br/> |
| <span id="SRRF_RT_QWORD"></span><span id="srrf_rt_qword"></span><dl> <dt>**SRRF \_RT \_ QWORD**</dt> <dt>0x00000048</dt> </dl>                           | REG \_ QWORD 和64位 reg \_ 二進位類型。 這相當於 SRRF \_ rt \_ reg \_ BINARY \| SRRF \_ rt \_ reg \_ 。 如果要抓取值，如果值的二進位資料大於64位，則不會傳回。<br/> |
| <span id="SRRF_RT_ANY"></span><span id="srrf_rt_any"></span><dl> <dt>**SRRF \_RT \_ 任何**</dt> <dt>0x0000FFFF</dt> </dl>                                 | 所有類型。 如果未設定其他 SRRF RT 值，請設定此旗標 \_ 。<br/>                                                                                                                                                 |
| <span id="SRRF_RM_ANY"></span><span id="srrf_rm_any"></span><dl> <dt>**SRRF \_RM \_ 任何**</dt> <dt>0x00000000</dt> </dl>                                 | 無模式限制。 這是預設值。<br/>                                                                                                                                                             |
| <span id="SRRF_RM_NORMAL"></span><span id="srrf_rm_normal"></span><dl> <dt>**SRRF \_RM \_ 一般**</dt> <dt>0x00010000</dt> </dl>                        | 將系統啟動模式限制為「正常開機」。<br/>                                                                                                                                                              |
| <span id="SRRF_RM_SAFE"></span><span id="srrf_rm_safe"></span><dl> <dt>**SRRF \_RM \_ SAFE**</dt> <dt>0x00020000</dt> </dl>                              | 將系統啟動模式限制為「安全模式」。<br/>                                                                                                                                                                |
| <span id="SRRF_RM_SAFENETWORK"></span><span id="srrf_rm_safenetwork"></span><dl> <dt>**SRRF \_RM \_ SAFENETWORK**</dt> <dt>0x00040000</dt> </dl>         | 將系統啟動模式限制為「具有網路功能的安全模式」。<br/>                                                                                                                                                |
| <span id="SRRF_NOEXPAND"></span><span id="srrf_noexpand"></span><dl> <dt>**SRRF \_NOEXPAND**</dt> <dt>0x10000000</dt> </dl>                            | 不要自動展開 REG \_ expand \_ SZ 環境字串。<br/>                                                                                                                                            |
| <span id="SRRF_ZEROONFAILURE"></span><span id="srrf_zeroonfailure"></span><dl> <dt>**SRRF \_ZEROONFAILURE**</dt> <dt>0x20000000</dt> </dl>             | 如果要取出值，如果 *pvData* 不是 **Null**，請將 *pvData* 緩衝區的內容設定為失敗時的所有零。<br/>                                                                                        |
| <span id="SRRF_NOVIRT"></span><span id="srrf_novirt"></span><dl> <dt>**SRRF \_NOVIRT**</dt> <dt>0x40000000</dt> </dl>                                  | 在抓取值時，如果要求的金鑰已虛擬化，將會失敗並 \_ \_ 找不到錯誤檔案 \_ 。<br/>                                                                                                            |



## <a name="remarks"></a>備註

這些值定義于 Shlwapi 中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Shlwapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SHRegSetValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shregsetvalue)
</dt> <dt>

[**SHRegGetValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetvaluea)
</dt> </dl>

 

 




