---
description: Component 物件代表可供列舉之元件的唯一實例。
ms.assetid: cdc99bc3-9e2a-49db-8c01-b9634aefac38
title: 元件物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Component
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5e31d6a7c3d2422111d0d8c3247e022fa35bdc43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994290"
---
# <a name="component-object"></a>元件物件

Component 物件代表可供列舉之元件的唯一實例。

**[Windows Installer 4.5 或更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。 從 Windows Installer 5.0 開始，可以使用這個物件。

## <a name="members"></a>成員

**元件** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**元件** 物件具有這些屬性。



| 屬性                                                    | 描述                                                                               |
|:------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**ComponentCode**](component-componentcode.md)<br/> | 有問題之元件的元件代碼。<br/>                               |
| [**Context**](component-context.md)<br/>             | 判斷為適用于問題元件的內容。<br/> |
| [**UserSID**](component-usersid.md)<br/>             | 列舉元件的使用者 SID。<br/>                                     |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Installer 5.0 或更新版本。<br/>                                         |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl> |
| IID<br/>     | IID \_ IComponent 定義為000C1097-0000-0000-C000-000000000046<br/>      |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用 Automation 介面](using-the-automation-interface.md)
</dt> <dt>

[Windows Installer 腳本範例](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




