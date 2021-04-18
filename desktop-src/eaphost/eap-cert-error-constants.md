---
title: 'EAP 憑證 \_ 錯誤常數 (Eaphosterror .h) '
description: 定義所有 EAPHost API 技術通用的憑證相關錯誤。
ms.assetid: 12f626e1-520a-4aba-954b-769c3062a38c
topic_type:
- apiref
api_name:
- _EAP_CERT_FIRST
- _EAP_CERT_LAST
- _EAP_CERT_NOT_FOUND
- _EAP_CERT_INVALID
- _EAP_CERT_EXPIRED
- _EAP_CERT_REVOKED
- _EAP_CERT_OTHER_ERROR
- _EAP_CERT_REJECTED
- _EAP_CERT_NAME_REQUIRED
- _EAP_GENERAL_FIRST
- _EAP_GENERAL_LAST
api_location:
- eaphosterror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0543636f36d823b5557ad2f5a5f7cb000d93259a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508400"
---
# <a name="eap_cert-error-constants"></a>EAP 憑證 \_ 錯誤常數

這些常數會定義所有 EAPHost API 技術通用的憑證相關錯誤。

<dl> <dt>

<span id="_EAP_CERT_FIRST"></span><span id="_eap_cert_first"></span>**\_EAP \_ 憑證 \_ 優先**
</dt> <dd> <dl> <dt>

0x0
</dt> <dt>



定義錯誤報表的界限;**\_ eap 憑證 \_ \_ FIRST** 和 **\_ eap \_ \_** 憑證之間會發生任何憑證錯誤。


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_LAST"></span><span id="_eap_cert_last"></span>**\_EAP \_ 憑證 \_ LAST**
</dt> <dd> <dl> <dt>

0xF
</dt> <dt>



定義錯誤報表的界限;**\_ eap 憑證 \_ \_ FIRST** 和 **\_ eap \_ \_** 憑證之間會發生任何憑證錯誤。


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_NOT_FOUND"></span><span id="_eap_cert_not_found"></span>**\_\_ \_ \_ 找不到 EAP 憑證**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>



找不到任何使用者憑證。


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_INVALID"></span><span id="_eap_cert_invalid"></span>**\_EAP \_ 憑證 \_ 無效**
</dt> <dd> <dl> <dt>

0x2
</dt> <dt>



使用者憑證無效。


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_EXPIRED"></span><span id="_eap_cert_expired"></span>**\_EAP 憑證已 \_ \_ 過期**
</dt> <dd> <dl> <dt>

0x3
</dt> <dt>



使用者憑證已過期。


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_REVOKED"></span><span id="_eap_cert_revoked"></span>**\_已 \_ 撤銷 EAP 憑證 \_**
</dt> <dd> <dl> <dt>

0x4
</dt> <dt>



使用者憑證已撤銷。


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_OTHER_ERROR"></span><span id="_eap_cert_other_error"></span>**\_EAP \_ 憑證 \_ 其他 \_ 錯誤**
</dt> <dd> <dl> <dt>

0x5
</dt> <dt>



有未知的憑證相關錯誤。


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_REJECTED"></span><span id="_eap_cert_rejected"></span>**\_已 \_ 拒絕 EAP 憑證 \_**
</dt> <dd> <dl> <dt>

0x6
</dt> <dt>



使用者憑證遭到拒絕。


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_NAME_REQUIRED"></span><span id="_eap_cert_name_required"></span>**\_需要 EAP 憑證 \_ \_ 名稱 \_**
</dt> <dd> <dl> <dt>

0x7
</dt> <dt>



使用者憑證需要名稱。


</dt> </dl> </dd> <dt>

<span id="_EAP_GENERAL_FIRST"></span><span id="_eap_general_first"></span>**\_EAP \_ 一般 \_ 優先**
</dt> <dd> <dl> <dt>

0x10
</dt> <dt>



定義錯誤報表的界限;任何一般 EAP 錯誤都會在 **\_ eap \_ 一般 \_ 優先** 和 **\_ eap \_ 一般 \_** 之間發生。


</dt> </dl> </dd> <dt>

<span id="_EAP_GENERAL_LAST"></span><span id="_eap_general_last"></span>**\_EAP \_ 一般 \_ 最後**
</dt> <dd> <dl> <dt>

0x3F
</dt> <dt>



定義錯誤報表的界限;任何一般 EAP 錯誤都會在 **\_ eap \_ 一般 \_ 優先** 和 **\_ eap \_ 一般 \_** 之間發生。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                      |
| 標頭<br/>                   | <dl> <dt>Eaphosterror。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[常見的 EAPHost 常數](common-eap-host-error-constants.md)
</dt> </dl>

 

 





