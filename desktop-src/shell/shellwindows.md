---
description: 表示屬於 Shell 之開啟視窗的集合。 與這個物件相關聯的方法可以控制和執行 Shell 內的命令，以及取得其他與 Shell 相關的物件。
ms.assetid: cad1f961-7fb4-4ba1-be48-b664d3de2c60
title: 'ShellWindows 物件 (Exdisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b558bf4df33e84fabae7e70c1722d78647514a52df8f62d05f8ecba8916c488a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857087"
---
# <a name="shellwindows-object"></a>ShellWindows 物件

表示屬於 Shell 之開啟視窗的集合。 與這個物件相關聯的方法可以控制和執行 Shell 內的命令，以及取得其他與 Shell 相關的物件。

## <a name="members"></a>成員

**ShellWindows** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**ShellWindows** 物件有這些方法。



| 方法                                                 | 描述                                                                                                         |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](shellwindows--newenum-method-7ral.md) | 建立並傳回新的 **ShellWindows** 物件，該物件為這個 **ShellWindows** 物件的複本。<br/>        |
| [**項目**](shellwindows-item.md)                      | 捕獲代表 Shell 視窗的 [**microsoft-windows-ie-internetexplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) 物件。<br/> |



 

### <a name="properties"></a>屬性

**ShellWindows** 物件具有這些屬性。



| 屬性                                       | 存取類型          | 描述                                                |
|:-----------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [**計數**](shellwindows-count.md)<br/> | 唯讀<br/> | 包含集合中的專案數。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional，僅 Windows XP \[ desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>Exdisp。h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (4.71 版或更新版本) </dt> </dl> |



 

 
