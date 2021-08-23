---
title: IMsRdpClientAdvancedSettings5 ConnectionBarShowPinButton 屬性
description: 設定或抓取連接列中 [釘選] 按鈕的設定。
ms.assetid: fbb2c19b-88a7-435b-86ef-4856e194b383
ms.tgt_platform: multiple
keywords:
- ConnectionBarShowPinButton 屬性遠端桌面服務
- ConnectionBarShowPinButton 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，ConnectionBarShowPinButton 屬性
- ConnectionBarShowPinButton 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，ConnectionBarShowPinButton 屬性
- ConnectionBarShowPinButton 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，ConnectionBarShowPinButton 屬性
- ConnectionBarShowPinButton 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，ConnectionBarShowPinButton 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings5.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings5.put_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings6.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings6.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings6.put_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings7.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings7.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings7.put_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings8.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings8.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings8.put_ConnectionBarShowPinButton
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a978f6d1b6a26fe84f5ad590cfc41ab384d6ba49f1e265eecc0ea408b67b59c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001386"
---
# <a name="imsrdpclientadvancedsettings5connectionbarshowpinbutton-property"></a>IMsRdpClientAdvancedSettings5：： ConnectionBarShowPinButton 屬性

設定或抓取連接列中 [釘選] 按鈕的設定。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ConnectionBarShowPinButton(
  [in]  VARIANT_BOOL fShowPin
);

HRESULT get_ConnectionBarShowPinButton(
  [out] VARIANT_BOOL *pfShowPin
);
```



## <a name="property-value"></a>屬性值

**TRUE** 或 **FALSE** 的布林值。 值為 **TRUE** 時，會顯示連接列中的 [釘選] 按鈕。 值為 **FALSE** 時，會隱藏連接列中的 [釘選] 按鈕。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                         |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                   |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings5 定義為 FBA7F64E-6783-4405-DA45-FA4A763DABD0<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





