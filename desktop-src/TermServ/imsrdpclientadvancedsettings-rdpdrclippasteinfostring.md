---
title: IMsRdpClientAdvancedSettings RdpdrClipPasteInfoString 屬性
description: 不支援這個屬性。 |IMsRdpClientAdvancedSettings RdpdrClipPasteInfoString 屬性
ms.assetid: 1ee39a2d-1d99-4052-8d47-ee6f46cacefd
ms.tgt_platform: multiple
keywords:
- RdpdrClipPasteInfoString 屬性遠端桌面服務
- RdpdrClipPasteInfoString 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，RdpdrClipPasteInfoString 屬性
- RdpdrClipPasteInfoString 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，RdpdrClipPasteInfoString 屬性
- RdpdrClipPasteInfoString 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，RdpdrClipPasteInfoString 屬性
- RdpdrClipPasteInfoString 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，RdpdrClipPasteInfoString 屬性
- RdpdrClipPasteInfoString 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，RdpdrClipPasteInfoString 屬性
- RdpdrClipPasteInfoString 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，RdpdrClipPasteInfoString 屬性
- RdpdrClipPasteInfoString 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，RdpdrClipPasteInfoString 屬性
- RdpdrClipPasteInfoString 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，RdpdrClipPasteInfoString 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.RdpdrClipPasteInfoString
- IMsRdpClientAdvancedSettings.get_RdpdrClipPasteInfoString
- IMsRdpClientAdvancedSettings.put_RdpdrClipPasteInfoString
- IMsRdpClientAdvancedSettings2.RdpdrClipPasteInfoString
- IMsRdpClientAdvancedSettings2.get_RdpdrClipPasteInfoString
- IMsRdpClientAdvancedSettings2.put_RdpdrClipPasteInfoString
- IMsRdpClientAdvancedSettings3.RdpdrClipPasteInfoString
- IMsRdpClientAdvancedSettings3.get_RdpdrClipPasteInfoString
- IMsRdpClientAdvancedSettings3.put_RdpdrClipPasteInfoString
- IMsRdpClientAdvancedSettings4.RdpdrClipPasteInfoString
- IMsRdpClientAdvancedSettings4.get_RdpdrClipPasteInfoString
- IMsRdpClientAdvancedSettings4.put_RdpdrClipPasteInfoString
- IMsRdpClientAdvancedSettings5.RdpdrClipPasteInfoString
- IMsRdpClientAdvancedSettings5.get_RdpdrClipPasteInfoString
- IMsRdpClientAdvancedSettings5.put_RdpdrClipPasteInfoString
- IMsRdpClientAdvancedSettings6.RdpdrClipPasteInfoString
- IMsRdpClientAdvancedSettings6.get_RdpdrClipPasteInfoString
- IMsRdpClientAdvancedSettings6.put_RdpdrClipPasteInfoString
- IMsRdpClientAdvancedSettings7.RdpdrClipPasteInfoString
- IMsRdpClientAdvancedSettings7.get_RdpdrClipPasteInfoString
- IMsRdpClientAdvancedSettings7.put_RdpdrClipPasteInfoString
- IMsRdpClientAdvancedSettings8.RdpdrClipPasteInfoString
- IMsRdpClientAdvancedSettings8.get_RdpdrClipPasteInfoString
- IMsRdpClientAdvancedSettings8.put_RdpdrClipPasteInfoString
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e830d4875f43a887d7fd8dfe51bf3e70921dd309
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103853659"
---
# <a name="imsrdpclientadvancedsettingsrdpdrclippasteinfostring-property"></a>IMsRdpClientAdvancedSettings：： RdpdrClipPasteInfoString 屬性

不支援這個屬性。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_RdpdrClipPasteInfoString(
  [in]  BSTR clipPasteInfoString
);

HRESULT get_RdpdrClipPasteInfoString(
  [out] BSTR *pclipPasteInfoString
);
```



## <a name="property-value"></a>屬性值

新訊息。

## <a name="error-codes"></a>錯誤碼

傳回 **\_ FALSE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                       |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                       |
| 用戶端支援結束<br/>    | 都不支援<br/>                                                                       |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imstscadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





