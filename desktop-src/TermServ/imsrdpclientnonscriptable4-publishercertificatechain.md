---
title: IMsRdpClientNonScriptable4 PublisherCertificateChain 屬性
description: 控制發行者的憑證鏈。 此鏈會儲存在類型為 VT BYREF 的變數中 \_ ，其中包含指向 CERT \_ 鏈 \_ 內容結構的指標。 如需 VT BYREF 結構的詳細資訊 \_ ，請參閱 VARIANT 和 VARIANTARG。
ms.assetid: 27ab0aff-1aef-4701-abe0-849bf32c9773
ms.tgt_platform: multiple
keywords:
- PublisherCertificateChain 屬性遠端桌面服務
- PublisherCertificateChain 屬性遠端桌面服務，IMsRdpClientNonScriptable4 介面
- IMsRdpClientNonScriptable4 介面遠端桌面服務，PublisherCertificateChain 屬性
- PublisherCertificateChain 屬性遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，PublisherCertificateChain 屬性
- PublisherCertificateChain 屬性遠端桌面服務，MsRdpClient6 物件
- MsRdpClient6 物件遠端桌面服務、PublisherCertificateChain 屬性
- PublisherCertificateChain 屬性遠端桌面服務，MsRdpClient7 物件
- MsRdpClient7 物件遠端桌面服務、PublisherCertificateChain 屬性
- PublisherCertificateChain 屬性遠端桌面服務，MsRdpClient8 物件
- MsRdpClient8 物件遠端桌面服務、PublisherCertificateChain 屬性
- PublisherCertificateChain 屬性遠端桌面服務，MsRdpClient9 物件
- MsRdpClient9 物件遠端桌面服務、PublisherCertificateChain 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.PublisherCertificateChain
- IMsRdpClientNonScriptable4.get_PublisherCertificateChain
- IMsRdpClientNonScriptable4.put_PublisherCertificateChain
- IMsRdpClientNonScriptable5.PublisherCertificateChain
- IMsRdpClientNonScriptable5.get_PublisherCertificateChain
- IMsRdpClientNonScriptable5.put_PublisherCertificateChain
- MsRdpClient6.PublisherCertificateChain
- MsRdpClient7.PublisherCertificateChain
- MsRdpClient8.PublisherCertificateChain
- MsRdpClient9.PublisherCertificateChain
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7552483c2fc651ace1a9401e0555f90fb2584423
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843852"
---
# <a name="imsrdpclientnonscriptable4publishercertificatechain-property"></a>IMsRdpClientNonScriptable4：:P ublisherCertificateChain 屬性

控制發行者的憑證鏈。 此鏈會儲存在類型為 **VT \_ BYREF** 的變數中，其中包含指向 [**CERT \_ 鏈 \_ 內容**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) 結構的指標。 如需 **VT \_ BYREF** 結構的詳細資訊，請參閱 [VARIANT 和 VARIANTARG](/windows/win32/api/oaidl/ns-oaidl-variant)。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_PublisherCertificateChain(
  [in]  VARIANT *pVarCert
);

HRESULT get_PublisherCertificateChain(
  [out] VARIANT *pVarCert
);
```



## <a name="property-value"></a>屬性值

設定發行者憑證鏈。 此鏈會儲存在類型為 **VT \_ BYREF** 的變數中，其中包含指向 [**CERT \_ 鏈 \_ 內容**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) 結構的指標。

## <a name="error-codes"></a>錯誤碼

如果成功，則傳回 **S \_ OK** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                           |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IMsRdpClientNonScriptable4 定義為 f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

