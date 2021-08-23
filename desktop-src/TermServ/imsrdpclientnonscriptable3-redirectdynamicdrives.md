---
title: IMsRdpClientNonScriptable3 RedirectDynamicDrives 屬性
description: 指定或抓取是否可重新導向會話中所列舉的隨插即用 (PnP) 磁片磁碟機的動態連接。
ms.assetid: 11eb19fc-9711-4293-8054-f7975dadb492
ms.tgt_platform: multiple
keywords:
- RedirectDynamicDrives 屬性遠端桌面服務
- RedirectDynamicDrives 屬性遠端桌面服務，IMsRdpClientNonScriptable3 介面
- IMsRdpClientNonScriptable3 介面遠端桌面服務，RedirectDynamicDrives 屬性
- RedirectDynamicDrives 屬性遠端桌面服務，IMsRdpClientNonScriptable4 介面
- IMsRdpClientNonScriptable4 介面遠端桌面服務，RedirectDynamicDrives 屬性
- RedirectDynamicDrives 屬性遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，RedirectDynamicDrives 屬性
- RedirectDynamicDrives 屬性遠端桌面服務，MsRdpClient5 物件
- MsRdpClient5 物件遠端桌面服務、RedirectDynamicDrives 屬性
- RedirectDynamicDrives 屬性遠端桌面服務，MsRdpClient6 物件
- MsRdpClient6 物件遠端桌面服務、RedirectDynamicDrives 屬性
- RedirectDynamicDrives 屬性遠端桌面服務，MsRdpClient7 物件
- MsRdpClient7 物件遠端桌面服務、RedirectDynamicDrives 屬性
- RedirectDynamicDrives 屬性遠端桌面服務，MsRdpClient8 物件
- MsRdpClient8 物件遠端桌面服務、RedirectDynamicDrives 屬性
- RedirectDynamicDrives 屬性遠端桌面服務，MsRdpClient9 物件
- MsRdpClient9 物件遠端桌面服務、RedirectDynamicDrives 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.RedirectDynamicDrives
- IMsRdpClientNonScriptable3.get_RedirectDynamicDrives
- IMsRdpClientNonScriptable3.put_RedirectDynamicDrives
- IMsRdpClientNonScriptable4.RedirectDynamicDrives
- IMsRdpClientNonScriptable4.get_RedirectDynamicDrives
- IMsRdpClientNonScriptable4.put_RedirectDynamicDrives
- IMsRdpClientNonScriptable5.RedirectDynamicDrives
- IMsRdpClientNonScriptable5.get_RedirectDynamicDrives
- IMsRdpClientNonScriptable5.put_RedirectDynamicDrives
- MsRdpClient5.RedirectDynamicDrives
- MsRdpClient6.RedirectDynamicDrives
- MsRdpClient7.RedirectDynamicDrives
- MsRdpClient8.RedirectDynamicDrives
- MsRdpClient9.RedirectDynamicDrives
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5199f8fcf8e114cfb8febd05631e49de97aab01a69ca9397bc7d15539ad819d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001100"
---
# <a name="imsrdpclientnonscriptable3redirectdynamicdrives-property"></a>IMsRdpClientNonScriptable3：： RedirectDynamicDrives 屬性

指定或抓取是否可重新導向會話中所列舉的隨插即用 (PnP) 磁片磁碟機的動態連接。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_RedirectDynamicDrives(
  [in]  VARIANT_BOOL fRedirectDynamicDrives
);

HRESULT get_RedirectDynamicDrives(
  [out] VARIANT_BOOL *pfRedirectDynamicDrives
);
```



## <a name="property-value"></a>屬性值

指定在會話中列舉的動態連接 PnP 磁片磁碟機是否可用於重新導向。

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

 

 





