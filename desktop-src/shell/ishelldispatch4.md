---
description: 擴充 IShellDispatch3 物件。
title: 'IShellDispatch4 物件 (Shldisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 4fe37e38-ee71-41f0-b620-35fdc18f9dbb
ms.openlocfilehash: 057ef4082bac8d04c006d951db7d2d251be2f8c62e88af65bc1a69678514af81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969007"
---
# <a name="ishelldispatch4-object"></a>IShellDispatch4 物件

擴充 [**IShellDispatch3**](ishelldispatch3.md) 物件。 除了 **IShellDispatch3** 支援的屬性和方法之外， **IShellDispatch4** 還支援四個額外的方法。

> [!Note]  
> **IShellDispatch4** 是透過 [**Shell**](shell.md) 物件來執行和存取。

 

## <a name="members"></a>成員

**IShellDispatch4** 物件具有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IShellDispatch4** 物件有這些方法。



| 方法                                                     | 描述                                                         |
|:-----------------------------------------------------------|:--------------------------------------------------------------------|
| [**ExplorerPolicy**](ishelldispatch4-explorerpolicy.md)   | 取得指定 Internet Explorer 原則的值。<br/> |
| [**GetSetting**](ishelldispatch4-getsetting.md)           | 捕獲全域 Shell 設定。<br/>                        |
| [**ToggleDesktop**](ishelldispatch4-toggledesktop.md)     | 顯示或隱藏桌面。<br/>                           |
| [**WindowsSecurity**](ishelldispatch4-windowssecurity.md) | 顯示 [ **Windows 安全性**] 對話方塊。<br/>            |



 

## <a name="remarks"></a>備註

如需 Windows 服務的討論，請參閱[服務](../services/services.md)檔。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (6.0 版或更新版本) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**Shell 物件**](shell.md)
</dt> <dt>

[**IShellDispatch**](ishelldispatch.md)
</dt> <dt>

[**IShellDispatch2**](ishelldispatch2-object.md)
</dt> <dt>

[**IShellDispatch3**](ishelldispatch3.md)
</dt> </dl>

 

 
