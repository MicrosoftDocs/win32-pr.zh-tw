---
description: UIPreview 物件是用來在撰寫期間，用來查看使用者介面對話方塊和公告欄。 此物件是由 Database 物件的 EnableUIPreview 方法所建立。
ms.assetid: 5df2a4f3-6352-4575-b822-1811150a86be
title: UIPreview 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 82436f21cc3920c2e1f635f8d1612118831e7d29f3fb1202105511f2e61f7a3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118623497"
---
# <a name="uipreview-object"></a>UIPreview 物件

**UIPreview** 物件是用來在撰寫期間，用來查看使用者介面對話方塊和公告欄。 此物件是由 [**Database**](database-object.md)物件的 [**EnableUIPreview**](database-enableuipreview.md)方法所建立。

## <a name="members"></a>成員

**UIPreview** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**UIPreview** 物件有這些方法。



| 方法                                           | 描述                                                                                             |
|:-------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**ViewBillboard**](uipreview-viewbillboard.md) | 使用目前顯示之對話方塊中的主控制項，顯示撰寫的佈告欄。<br/> |
| [**ViewDialog**](uipreview-viewdialog.md)       | 顯示儲存在目前資料庫中的撰寫 UI 對話方塊。<br/>                           |



 

### <a name="properties"></a>屬性

**UIPreview** 物件具有這些屬性。



| 屬性                                          | 存取類型           | 描述                                                                                                                                                                       |
|:--------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**屬性**](uipreview-property.md)<br/> | 讀取/寫入<br/> | 表示指定之安裝程式屬性的字串值，如果前面加上百分比符號 (% ) ，則為目前進程的系統內容變數值。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IUIPreview 定義為 000C109A-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Windows安裝程式腳本範例](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




