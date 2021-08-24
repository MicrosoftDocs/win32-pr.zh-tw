---
title: IMsRdpClientTransportSettings2 GatewayEncryptedOtpCookie 屬性
description: 指定或抓取加密的一次性密碼 (OTP) cookie。
ms.assetid: 09b90231-ebe5-4165-b0e5-edba18472391
ms.tgt_platform: multiple
keywords:
- GatewayEncryptedOtpCookie 屬性遠端桌面服務
- GatewayEncryptedOtpCookie 屬性遠端桌面服務，IMsRdpClientTransportSettings2 介面
- IMsRdpClientTransportSettings2 介面遠端桌面服務，GatewayEncryptedOtpCookie 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayEncryptedOtpCookie
- IMsRdpClientTransportSettings2.get_GatewayEncryptedOtpCookie
- IMsRdpClientTransportSettings2.put_GatewayEncryptedOtpCookie
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55f7f1cf0d73d6e18a119207e57e0aaf93729d5b25a7184f4a55110d045b189a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770738"
---
# <a name="imsrdpclienttransportsettings2gatewayencryptedotpcookie-property"></a>IMsRdpClientTransportSettings2：： GatewayEncryptedOtpCookie 屬性

指定或抓取加密的一次性密碼 (OTP) cookie。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_GatewayEncryptedOtpCookie(
  [in]  BSTR bstrEncryptedOtpCookie
);

HRESULT get_GatewayEncryptedOtpCookie(
  [out] BSTR *pbstrEncryptedOtpCookie
);
```



## <a name="property-value"></a>屬性值

指定或抓取加密的 OTP cookie。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista SP1<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                    |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings2 定義為 67341688-D606-4c73-A5D2-2E0489009319<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md)
</dt> <dt>

[**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





