---
description: 擴充 IShellDispatch4 物件。
title: 'IShellDispatch5 物件 (Shldisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch5
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9170340a-0f11-4ec9-877d-fb7fef9888b2
ms.openlocfilehash: cbf3e960d7bfb9cd15411142cc036a21a9995ff9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972356"
---
# <a name="ishelldispatch5-object"></a>IShellDispatch5 物件

擴充 [**IShellDispatch4**](ishelldispatch4.md) 物件。 除了 **IShellDispatch4** 所支援的屬性和方法之外， **IShellDispatch5** 還新增了在3d 堆疊中顯示開啟視窗的方法。

> [!Note]  
> **IShellDispatch5** 是透過 [**Shell**](shell.md) 物件來執行和存取。

 

## <a name="members"></a>成員

**IShellDispatch5** 物件具有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IShellDispatch5** 物件有這些方法。



| 方法                                                   | 描述                                                                    |
|:---------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**WindowSwitcher**](ishelldispatch5-windowswitcher.md) | 將開啟的視窗顯示在您可以切換的3D 堆疊中。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                                                   |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                        |
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
</dt> <dt>

[**IShellDispatch4**](ishelldispatch4.md)
</dt> </dl>

 

 
