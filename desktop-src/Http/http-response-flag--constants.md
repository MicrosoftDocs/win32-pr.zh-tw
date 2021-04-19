---
title: 'HTTP_RESPONSE_FLAG_ 常數 (Http.sys) '
description: 定義在 HTTP 伺服器 API 中設定回應的選項。
ms.assetid: bcb59457-fd22-4166-8a72-ba85209ec8c7
topic_type:
- apiref
api_name:
- HTTP_RESPONSE_FLAG_MULTIPLE_ENCODINGS_AVAILABLE
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96b7c34d453c1b9bbe45cf2c85ad268b414f3439
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966918"
---
# <a name="http_response_flag_-constants"></a>HTTP \_ 回應 \_ 旗標 \_ 常數

**Http \_ 回應 \_ 旗 \_** 標常數定義了在 HTTP 伺服器 API 中設定回應的選項。

這些常數會在 [**HTTP \_ 回應 \_ V1**](/windows/desktop/api/Http/ns-http-http_response_v1)結構的 **旗標** 成員中使用。

<dl> <dt>

<span id="HTTP_RESPONSE_FLAG_MULTIPLE_ENCODINGS_AVAILABLE"></span><span id="http_response_flag_multiple_encodings_available"></span>**HTTP \_ 回應 \_ 旗 \_ 標 \_ 有多個可用的編碼 \_**
</dt> <dd> <dl> <dt>



身分識別表單以外的編碼可用於此資源。 如果應用程式未要求快取回應，則會忽略此旗標。 從核心回應快取提供服務時，它會用來做為 HTTP 伺服器 API 的提示，以進行內容協商。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>Http.sys</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[HTTP 伺服器 API 版本2.0 常數](http-server-api-version-2-0-constants.md)
</dt> <dt>

[**HTTP \_ 回應 \_ V1**](/windows/desktop/api/Http/ns-http-http_response_v1)
</dt> </dl>

 

 





