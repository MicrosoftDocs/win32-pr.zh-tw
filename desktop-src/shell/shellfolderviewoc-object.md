---
description: 將指定之 ShellFolderView 物件所引發的事件轉送到對應的 ShellFolderViewOC 事件處理常式。
title: 'ShellFolderViewOC 物件 (Shldisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderViewOC
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b50f549c-a79d-4411-a18e-a181b4b924e3
ms.openlocfilehash: 2670578417dc616d30f319887f5281fa5d0615f5
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840869"
---
# <a name="shellfolderviewoc-object"></a>ShellFolderViewOC 物件

將指定之 [**ShellFolderView**](shellfolderview.md) 物件所引發的事件轉送到對應的 **ShellFolderViewOC** 事件處理常式。

## <a name="members"></a>成員

**ShellFolderViewOC** 物件具有下列類型的成員：

-   [事件](#events)
-   [方法](#methods)

### <a name="events"></a>事件

**ShellFolderViewOC** 物件具有這些事件。



| 事件                                                          | 描述                                                                                                                     |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [**EnumDone**](shellfolderviewoc-enumdone.md)                 | 指出 [**ShellFolderView**](shellfolderview.md) 物件已完成資料夾內容的列舉。<br/> |
| [**SelectionChanged**](shellfolderviewoc-selectionchanged.md) | 指出視圖中一個或多個專案的選取狀態已變更。<br/>                                     |



 

### <a name="methods"></a>方法

**ShellFolderViewOC** 物件有這些方法。



| 方法                                                   | 描述                                                                                                                                                 |
|:---------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetFolderView**](shellfolderviewoc-setfolderview.md) | 將指定之 [**ShellFolderView**](shellfolderview.md) 物件的事件轉送至對應的 **ShellFolderViewOC** 事件處理常式。<br/> |



 

## <a name="remarks"></a>備註

[**ShellFolderView**](shellfolderview.md)物件會引發兩個 [**EnumDone**](shellfolderviewoc-enumdone.md)和 [**SelectionChanged**](shellfolderviewoc-selectionchanged.md)這兩個事件，通常是由應用程式處理。 不過，有些應用程式必須處理來自一系列 **ShellFolderView** 物件的事件。 例如，應用程式可能會裝載 WebBrowser 控制項，讓使用者能夠流覽一系列的資料夾。 每個資料夾都有自己的 **ShellFolderView** 物件及其相關聯的事件。 處理這些事件可能很困難。

**ShellFolderViewOC** 物件可簡化這類案例的事件處理。 它可讓應用程式使用一對 **ShellFolderViewOC** 事件處理常式來處理所有 [**ShellFolderView**](shellfolderview.md)物件的事件。 每次使用者流覽至新資料夾時，應用程式會藉由呼叫 [**SetFolderView**](shellfolderviewoc-setfolderview.md)將相關聯的 **ShellFolderView** 物件傳遞至 **ShellFolderViewOC** 物件。 然後，當引發 [**EnumDone**](shellfolderviewoc-enumdone.md) 或 [**SelectionChanged**](shellfolderviewoc-selectionchanged.md) 事件時， **ShellFolderViewOC** 物件會將事件轉送至它自己的處理常式以進行處理。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (5.0 版或更新版本) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ShellFolderView**](shellfolderview.md)
</dt> </dl>

 

 




