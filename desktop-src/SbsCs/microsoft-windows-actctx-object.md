---
description: Microsoft。Windows。ActCtx 物件參考資訊清單，並提供一種方法讓腳本引擎存取並存元件。 Microsoft。Windows。ActCtx 物件可以用來建立與 COM 元件並存元件的實例。
ms.assetid: 818e175e-2c58-4c44-87ce-4e97352fc3f3
title: 微軟。Windows。ActCtx 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Microsoft.Windows.ActCtx
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7e84eadbc7489ddd91c34c0c9494515e89205849829625e850ad31dce3e92fc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142001"
---
# <a name="microsoftwindowsactctx-object"></a>微軟。Windows。ActCtx 物件

**Windows。ActCtx** 物件參考資訊清單，並提供一種方法讓腳本引擎存取並存元件。 **Windows。ActCtx** 物件可以用來建立與 COM 元件並存元件的實例。

**Windows。ActCtx** 物件是 Windows Server 2003 中的元件。 它也可以由使用 Windows Installer 進行安裝程式的應用程式安裝，並在其安裝套件中包含為合併模組。

## <a name="members"></a>成員

**Windows。ActCtx** 物件有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Windows。ActCtx** 物件有這些方法。



| 方法                               | 描述                                                                     |
|:-------------------------------------|:--------------------------------------------------------------------------------|
| [**CreateObject**](createobject.md) | 在目前資訊清單的內容中建立物件。<br/>            |
| [**GetObject**](getobject.md)       | 取得現有 Microsoft Windows 的實例 **。ActCtx** 物件。<br/> |



 

### <a name="properties"></a>屬性

**Windows。ActCtx** 物件具有這些屬性。



| 屬性                                | 存取類型          | 描述                                    |
|:----------------------------------------|:---------------------|:-----------------------------------------------|
| [**清單**](manifest.md)<br/> | 唯讀<br/> | 取得有效的啟用內容。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/> |



 

 




