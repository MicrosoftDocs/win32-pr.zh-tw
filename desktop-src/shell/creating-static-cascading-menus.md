---
description: 從 Windows 7，串聯功能表是透過子命令登錄專案、ExtendedSubCommandsKey 登錄專案或 IExplorerCommand 介面建立。
title: 建立靜態串聯功能表
ms.topic: article
ms.date: 05/31/2018
ms.assetid: E3A6F174-BE53-48EF-AE9B-A3F297E91B95
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 22fdc261012697affd99b5a1491ef5829fcc5329d5570ae4e3c37dcd111b457f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456328"
---
# <a name="creating-static-cascading-menus"></a>建立靜態串聯功能表

在 Windows 7 和更新版本中，透過登錄設定可支援串聯式功能表的執行。 在 Windows 7 之前，只能透過 [**ICoNtextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)介面的執行來建立串聯功能表。 在 Windows 7 和更新版本中，只有在靜態方法不足時，您才應該將元件物件模型 (COM) 以程式碼為基礎的解決方案。

下列螢幕擷取畫面提供串聯功能表的範例。

![顯示級聯功能表範例的螢幕擷取畫面](images/file-assoc/filecascademenu2ndex.png)

在 Windows 7 和更新版本中，有三種方式可建立串聯功能表，如下列各節所述。

-   [如何使用子命令登錄專案建立串聯功能表](how-to--create-cascading-menus-with-the-subcommands-registry-entry.md)
-   [如何使用 ExtendedSubCommandsKey 登錄專案建立串聯功能表](how-to-create-cascading-menus-with-the-extendedsubcommandskey-registry-entry.md)
-   [如何使用 IExplorerCommand 介面建立串聯功能表](how-to-create-cascading-menus-with-the-iexplorercommand-interface.md)

 

 
