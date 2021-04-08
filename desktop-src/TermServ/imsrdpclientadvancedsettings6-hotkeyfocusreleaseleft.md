---
title: IMsRdpClientAdvancedSettings6 HotKeyFocusReleaseLeft 屬性
description: 指定要新增至 Ctrl + Alt 的虛擬按鍵程式碼，以決定 Ctrl + Alt + 向左鍵的替換熱鍵。
ms.assetid: 9F2942BD-9F5C-4E02-A330-42C30C6C8F87
ms.tgt_platform: multiple
keywords:
- HotKeyFocusReleaseLeft 屬性遠端桌面服務
- HotKeyFocusReleaseLeft 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，HotKeyFocusReleaseLeft 屬性
- HotKeyFocusReleaseLeft 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，HotKeyFocusReleaseLeft 屬性
- HotKeyFocusReleaseLeft 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，HotKeyFocusReleaseLeft 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings6.get_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings6.put_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings7.HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings7.get_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings7.put_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings8.HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings8.get_HotKeyFocusReleaseLeft
- IMsRdpClientAdvancedSettings8.put_HotKeyFocusReleaseLeft
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27e0e6d4e334edeffbf0ef025e59454e0f26c34c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685534"
---
# <a name="imsrdpclientadvancedsettings6hotkeyfocusreleaseleft-property"></a>IMsRdpClientAdvancedSettings6：： HotKeyFocusReleaseLeft 屬性

指定要新增至 Ctrl + Alt 的虛擬按鍵程式碼，以決定 Ctrl + Alt + 向左鍵的替換熱鍵。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_HotKeyFocusReleaseLeft(
  [in]  LONG hotKeyFocusReleaseLeft
);

HRESULT get_HotKeyFocusReleaseLeft(
  [out] LONG *hotKeyFocusReleaseLeft
);
```



## <a name="property-value"></a>屬性值

新的虛擬金鑰程式碼。

## <a name="remarks"></a>備註

只有遠端桌面連線6.1 和7.0 用戶端支援此屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                         |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                                   |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings6 定義為222c4b5d-45d9-4df0-a7c6-60cf9089d285<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





