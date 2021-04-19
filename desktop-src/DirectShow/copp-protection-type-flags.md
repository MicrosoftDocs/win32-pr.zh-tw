---
description: 下列常數與認證的輸出保護通訊協定搭配使用 (COPP) 至特定的輸出保護機制。
ms.assetid: a3cd63d8-22a5-473c-83c2-3499f3d32671
title: 'COPP 保護類型旗標 (Dxva .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COPP_ProtectionType_Unknown
- COPP_ProtectionType_None
- COPP_ProtectionType_HDCP
- COPP_ProtectionType_ACP
- COPP_ProtectionType_CGMSA
- COPP_ProtectionType_Mask
- COPP_ProtectionType_Reserved
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: 57e9ccc9420659ac09c19f2bbb7a18db519c07bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996102"
---
# <a name="copp-protection-type-flags"></a>COPP 保護類型旗標

下列常數與認證的輸出保護通訊協定搭配使用 (COPP) 至特定的輸出保護機制。



| 常數/值                                                                                                                                                                                                                                                                                                             | Description                                                     |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| <span id="COPP_ProtectionType_Unknown"></span><span id="copp_protectiontype_unknown"></span><span id="COPP_PROTECTIONTYPE_UNKNOWN"></span><dl> <dt>**COPP \_Set-protectiontype \_ 不明**</dt>的 <dt>0x80000000</dt> </dl>     | 未知的保護機制。<br/>                        |
| <span id="COPP_ProtectionType_None"></span><span id="copp_protectiontype_none"></span><span id="COPP_PROTECTIONTYPE_NONE"></span><dl> <dt>**COPP \_Set-protectiontype \_ 無**</dt> <dt>0x00000000</dt> </dl>                 | 沒有防護機制。<br/>                            |
| <span id="COPP_ProtectionType_HDCP"></span><span id="copp_protectiontype_hdcp"></span><span id="COPP_PROTECTIONTYPE_HDCP"></span><dl> <dt>**COPP \_Set-protectiontype \_ HDCP**</dt> <dt>0x00000001</dt> </dl>                 | High-Bandwidth 數位內容保護 (HDCP) 。<br/>    |
| <span id="COPP_ProtectionType_ACP"></span><span id="copp_protectiontype_acp"></span><span id="COPP_PROTECTIONTYPE_ACP"></span><dl> <dt>**COPP \_Set-protectiontype \_ ACP**</dt> <dt>0x00000002</dt> </dl>                     | 類比禁止複製 (ACP) 。<br/>                        |
| <span id="COPP_ProtectionType_CGMSA"></span><span id="copp_protectiontype_cgmsa"></span><span id="COPP_PROTECTIONTYPE_CGMSA"></span><dl> <dt>**COPP \_Set-protectiontype \_ CGMSA**</dt> <dt>0x00000004</dt> </dl>             | 複製世代管理系統類比 (CGMS-A) 。<br/> |
| <span id="COPP_ProtectionType_Mask"></span><span id="copp_protectiontype_mask"></span><span id="COPP_PROTECTIONTYPE_MASK"></span><dl> <dt>**COPP \_Set-protectiontype \_ Mask**</dt> <dt>0x80000007</dt> </dl>                 | 用來隔離有效旗標的位元遮罩。<br/>                      |
| <span id="COPP_ProtectionType_Reserved"></span><span id="copp_protectiontype_reserved"></span><span id="COPP_PROTECTIONTYPE_RESERVED"></span><dl> <dt>**COPP \_Set-protectiontype \_ 保留**</dt>的 <dt>0x7FFFFFF8</dt> </dl> | 保留的。 必須為零。<br/>                              |



## <a name="remarks"></a>備註

某些方法會從這個列舉型別傳回單一旗標，而某些方法會傳回一或多個旗標的位 **or** 。

下列 COPP 查詢和命令會使用這些旗標。

-   全域保護等級
-   本機保護層級
-   保護類型
-   設定保護層級

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Dxva。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[常數和 Guid](constants-and-guids.md)
</dt> <dt>

[使用認證輸出保護通訊協定 (COPP) ](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 




