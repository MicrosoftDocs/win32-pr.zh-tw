---
title: IMsRdpClientAdvancedSettings3 ConnectionBarShowRestoreButton 屬性
description: 指定是否要在連接列上顯示 [還原] 按鈕。
ms.assetid: a56c3c05-d253-404a-bf49-9c1d804802e0
ms.tgt_platform: multiple
keywords:
- ConnectionBarShowRestoreButton 屬性遠端桌面服務
- ConnectionBarShowRestoreButton 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，ConnectionBarShowRestoreButton 屬性
- ConnectionBarShowRestoreButton 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，ConnectionBarShowRestoreButton 屬性
- ConnectionBarShowRestoreButton 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，ConnectionBarShowRestoreButton 屬性
- ConnectionBarShowRestoreButton 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，ConnectionBarShowRestoreButton 屬性
- ConnectionBarShowRestoreButton 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，ConnectionBarShowRestoreButton 屬性
- ConnectionBarShowRestoreButton 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，ConnectionBarShowRestoreButton 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings3.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings3.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings3.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings4.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings4.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings4.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings5.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings5.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings5.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings6.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings6.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings6.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings7.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings7.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings7.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings8.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings8.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings8.put_ConnectionBarShowRestoreButton
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81bcdefbd7cc41a0a1771705482cc67da028bf6dd349e473c02249284dcfcfe3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118608417"
---
# <a name="imsrdpclientadvancedsettings3connectionbarshowrestorebutton-property"></a>IMsRdpClientAdvancedSettings3：： ConnectionBarShowRestoreButton 屬性

指定是否要在連接列上顯示 [ **還原** ] 按鈕。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ConnectionBarShowRestoreButton(
  [in]  VARIANT_BOOL fShowRestore
);

HRESULT get_ConnectionBarShowRestoreButton(
  [out] VARIANT_BOOL *pfShowRestore
);
```



## <a name="property-value"></a>屬性值

設定為 **[ \_ variant TRUE** ] 以顯示 [ **還原** ] 按鈕，並將設為 [ **variant \_ FALSE** ] 以停用 [ **還原** ] 按鈕的顯示。

## <a name="error-codes"></a>錯誤碼

如果成功，則傳回 **S \_ OK** 。

## <a name="remarks"></a>備註

連接控制項時無法設定這個屬性。

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                         |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                   |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings3 定義為19cd856b-c542-4c53-acee-f127e3be1a59<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

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

[**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
</dt> </dl>

 

 





