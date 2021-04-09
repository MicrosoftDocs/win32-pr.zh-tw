---
description: ActCtx 物件參考資訊清單，並提供一種方法讓腳本引擎存取並存元件。 ActCtx 物件可以用來建立與 COM 元件並存元件的實例，以供使用。
ms.assetid: 818e175e-2c58-4c44-87ce-4e97352fc3f3
title: ActCtx 物件
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
ms.openlocfilehash: 58290ec9d36d8e8428000422d0e1014335870149
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848838"
---
# <a name="microsoftwindowsactctx-object"></a>ActCtx 物件

**ActCtx** 物件參考資訊清單，並提供一種方法讓腳本引擎存取並存元件。 **ActCtx** 物件可以用來建立與 COM 元件並存元件的實例，以供使用。

**ActCtx** 物件是 windows Server 2003 中的元件。 它也可以由使用 Windows Installer 進行安裝程式的應用程式安裝，並在其安裝套件中包含為合併模組。

## <a name="members"></a>成員

**ActCtx** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**ActCtx** 物件有這些方法。



| 方法                               | 描述                                                                     |
|:-------------------------------------|:--------------------------------------------------------------------------------|
| [**CreateObject**](createobject.md) | 在目前資訊清單的內容中建立物件。<br/>            |
| [**GetObject**](getobject.md)       | 取得現有 **ActCtx** 物件的實例。<br/> |



 

### <a name="properties"></a>屬性

**ActCtx** 物件具有這些屬性。



| 屬性                                | 存取類型          | Description                                    |
|:----------------------------------------|:---------------------|:-----------------------------------------------|
| [**清單**](manifest.md)<br/> | 唯讀<br/> | 取得有效的啟用內容。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/> |



 

 




