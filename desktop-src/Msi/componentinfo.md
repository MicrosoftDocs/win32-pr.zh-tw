---
description: ComponentInfo 物件代表可透過從 MsiGetComponentPathEx 呼叫取得之元件的其他詳細資料。
ms.assetid: 9b0ad0a1-c49f-4b14-817b-0cfc9b228d77
title: ComponentInfo 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ComponentInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a59aa1d9f7bdc5babc29461ca90c01b6fe604482cb78ba6549e782b1e34d54b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119251998"
---
# <a name="componentinfo-object"></a>ComponentInfo 物件

ComponentInfo 物件代表可透過從 MsiGetComponentPathEx 呼叫取得之元件的其他詳細資料。

**[Windows Installer 4.5 或更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。 從 Windows Installer 5.0 開始，可以使用這個物件。

## <a name="members"></a>成員

**ComponentInfo** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**ComponentInfo** 物件具有這些屬性。



| 屬性                                                        | 描述                                                 |
|:----------------------------------------------------------------|:------------------------------------------------------------|
| [**ComponentCode**](componentinfo-componentcode.md)<br/> | 有問題之元件的元件代碼。<br/> |
| [**路徑**](componentinfo-componentcode.md)<br/>          | 元件的路徑。<br/>                       |
| [**狀態**](componentinfo-state.md)<br/>                 | 元件的狀態。<br/>                      |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows安裝程式5.0 或更新版本。<br/>                                         |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl> |
| IID<br/>     | IID \_ IComponentInfo 定義為000C1099-0000-0000-C000-000000000046<br/>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用 Automation 介面](using-the-automation-interface.md)
</dt> <dt>

[Windows安裝程式腳本範例](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




