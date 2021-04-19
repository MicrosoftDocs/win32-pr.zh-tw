---
title: IMsRdpClientNonScriptable3 NegotiateSecurityLayer 屬性
description: 指定或抓取是否已啟用連線的協商安全性層級。
ms.assetid: 7fc9e3c7-0723-48c4-8d29-5f68a24a522c
ms.tgt_platform: multiple
keywords:
- NegotiateSecurityLayer 屬性遠端桌面服務
- NegotiateSecurityLayer 屬性遠端桌面服務，IMsRdpClientNonScriptable3 介面
- IMsRdpClientNonScriptable3 介面遠端桌面服務，NegotiateSecurityLayer 屬性
- NegotiateSecurityLayer 屬性遠端桌面服務，IMsRdpClientNonScriptable4 介面
- IMsRdpClientNonScriptable4 介面遠端桌面服務，NegotiateSecurityLayer 屬性
- NegotiateSecurityLayer 屬性遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，NegotiateSecurityLayer 屬性
- NegotiateSecurityLayer 屬性遠端桌面服務，MsRdpClient5 物件
- MsRdpClient5 物件遠端桌面服務、NegotiateSecurityLayer 屬性
- NegotiateSecurityLayer 屬性遠端桌面服務，MsRdpClient6 物件
- MsRdpClient6 物件遠端桌面服務、NegotiateSecurityLayer 屬性
- NegotiateSecurityLayer 屬性遠端桌面服務，MsRdpClient7 物件
- MsRdpClient7 物件遠端桌面服務、NegotiateSecurityLayer 屬性
- NegotiateSecurityLayer 屬性遠端桌面服務，MsRdpClient8 物件
- MsRdpClient8 物件遠端桌面服務、NegotiateSecurityLayer 屬性
- NegotiateSecurityLayer 屬性遠端桌面服務，MsRdpClient9 物件
- MsRdpClient9 物件遠端桌面服務、NegotiateSecurityLayer 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.NegotiateSecurityLayer
- IMsRdpClientNonScriptable3.get_NegotiateSecurityLayer
- IMsRdpClientNonScriptable3.put_NegotiateSecurityLayer
- IMsRdpClientNonScriptable4.NegotiateSecurityLayer
- IMsRdpClientNonScriptable4.get_NegotiateSecurityLayer
- IMsRdpClientNonScriptable4.put_NegotiateSecurityLayer
- IMsRdpClientNonScriptable5.NegotiateSecurityLayer
- IMsRdpClientNonScriptable5.get_NegotiateSecurityLayer
- IMsRdpClientNonScriptable5.put_NegotiateSecurityLayer
- MsRdpClient5.NegotiateSecurityLayer
- MsRdpClient6.NegotiateSecurityLayer
- MsRdpClient7.NegotiateSecurityLayer
- MsRdpClient8.NegotiateSecurityLayer
- MsRdpClient9.NegotiateSecurityLayer
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64533615c780cd6e3703be85363684e537b784a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967338"
---
# <a name="imsrdpclientnonscriptable3negotiatesecuritylayer-property"></a>IMsRdpClientNonScriptable3：： NegotiateSecurityLayer 屬性

指定或抓取是否已啟用連線的協商安全性層級。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_NegotiateSecurityLayer(
  [in]  VARIANT_BOOL fNegotiate
);

HRESULT get_NegotiateSecurityLayer(
  [out] VARIANT_BOOL *pfNegotiate
);
```



## <a name="property-value"></a>屬性值

指定是否要啟用安全性層的協商。

## <a name="remarks"></a>備註

如果這個屬性設定為 **VARIANT \_ FALSE** ，且網路層級驗證在用戶端作業系統上啟用了 (NLA) ，用戶端將不會協商安全性層級，而是會使用 NLA 來保護 RDP 連接。 如果這個屬性設定為 **VARIANT \_ TRUE**，用戶端就會在 NLA 和基本 RDP 安全性之間進行協調。

> [!Note]  
> 只有在連接到執行 Windows Vista 或更新版本作業系統的遠端桌面工作階段主機 (RD 工作階段主機) 伺服器時，才可以停用安全性層級的協商。 如果已啟用此屬性，且用戶端嘗試連線到執行舊版作業系統的 RD 工作階段主機伺服器，連接將會失敗。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                      |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable3 定義為 b3378d90-0728-45c7-8ed7-b6159fb92219<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





