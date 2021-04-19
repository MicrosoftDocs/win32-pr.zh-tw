---
description: 用戶端物件代表元件和用戶端產品之間的關聯性。
ms.assetid: ac1fbd74-fbc4-4f76-8e14-af48443a8528
title: 用戶端物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Client
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 75cb21a4149d8e6758ab24796949777b8052b120
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993357"
---
# <a name="client-object"></a>用戶端物件

用戶端物件代表元件和用戶端產品之間的關聯性。

**[Windows Installer 4.5 或更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。 從 Windows Installer 5.0 開始，可以使用這個物件。

## <a name="members"></a>成員

**用戶端** 物件有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**用戶端** 物件具有這些屬性。



| 屬性                                                 | 描述                                                 |
|:---------------------------------------------------------|:------------------------------------------------------------|
| [**ComponentCode**](client-componentcode.md)<br/> | 有問題之元件的元件代碼。<br/> |
| [**Context**](client-context.md)<br/>             | 產品的內容。<br/>                      |
| [**ProductCode**](client-productcode.md)<br/>     | 有問題之元件的用戶端產品。<br/> |
| [**UserSID**](client-usersid.md)<br/>             | 元件的使用者 SID。<br/>                  |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Installer 5.0 或更新版本。<br/>                                         |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl> |
| IID<br/>     | IID \_ IClient 定義為000C1098-0000-0000-C000-000000000046<br/>         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用 Automation 介面](using-the-automation-interface.md)
</dt> <dt>

[Windows Installer 腳本範例](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




