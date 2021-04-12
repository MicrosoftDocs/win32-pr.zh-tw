---
title: 'HTTP_RESPONSE (Http.sys) '
description: HTTP 回應結構的版本 \_ 取決於所使用的要求佇列版本，如下所示： Http SERVER API 1.0 版要求佇列，這是 HTTP \_ 要求 V1 的 \_ 結構。HTTP 伺服器 API 2.0 版要求佇列這是 HTTP \_ 要求 \_ V2 結構。
ms.assetid: F94646C0-7293-4543-842B-F08D8C7E2247
keywords:
- HTTP_RESPONSE
- HTTP_RESPONSE
- PHTTP_RESPONSE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a8445021aa61b94ae83a55937b1db5ca4e3c577
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384398"
---
# <a name="http_response"></a>HTTP \_ 回應

**HTTP \_ 回應** 結構的版本取決於所使用的要求佇列版本，如下所示：

-   HTTP 伺服器 API 1.0 版要求佇列：這是 [**HTTP \_ 要求 \_ V1**](/windows/desktop/api/Http/ns-http-http_request_v1) 結構。
-   HTTP 伺服器 API 2.0 版要求佇列：這是 [**HTTP \_ 要求 \_ V2**](/windows/desktop/api/Http/ns-http-http_request_v2) 結構。

請勿直接在您的程式碼中使用 [**HTTP \_ 要求 \_ V1**](/windows/desktop/api/Http/ns-http-http_request_v1) 和 [**HTTP \_ 要求 \_ V2**](/windows/desktop/api/Http/ns-http-http_request_v2) ，改為使用 **HTTP \_ 回應** ，根據要求佇列的版本，確保使用正確的結構版本。


```C++
typedef HTTP_REQUEST_V1 HTTP_RESPONSE;
typedef HTTP_REQUEST_V2 HTTP_RESPONSE;
typedef HTTP_RESPONSE* PHTTP_RESPONSE;
```



<dl> <dt>

**HTTP \_ 回應**
</dt> <dd>

來自 v1 要求佇列的要求。

</dd> <dt>

**HTTP \_ 回應**
</dt> <dd>

來自 v2 要求佇列的要求。

</dd> <dt>

**PHTTP \_ 回應**
</dt> <dd>

**HTTP \_ 回應** 結構的指標。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                    |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                              |
| 標頭<br/>                   | <dl> <dt>Http.sys</dt> </dl> |



 

 





