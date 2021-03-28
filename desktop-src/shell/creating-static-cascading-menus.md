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
ms.openlocfilehash: d812b4d3d2fb0754002cb37d72718e4fe861ce15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104555324"
---
# <a name="creating-static-cascading-menus"></a><span data-ttu-id="26256-103">建立靜態串聯功能表</span><span class="sxs-lookup"><span data-stu-id="26256-103">Creating Static Cascading Menus</span></span>

<span data-ttu-id="26256-104">在 Windows 7 （含）以後版本中，透過登錄設定支援串聯功能表的執行。</span><span class="sxs-lookup"><span data-stu-id="26256-104">In Windows 7 and later, cascading menu implementation is supported through registry settings.</span></span> <span data-ttu-id="26256-105">在 Windows 7 之前，只能透過 [**ICoNtextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) 介面的執行來建立串聯功能表。</span><span class="sxs-lookup"><span data-stu-id="26256-105">Prior to Windows 7, the creation of cascading menus was possible only through the implementation of the [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) interface.</span></span> <span data-ttu-id="26256-106">在 Windows 7 和更新版本中，只有在靜態方法不足時，您才應該將元件物件模型 (COM) 以程式碼為基礎的解決方案。</span><span class="sxs-lookup"><span data-stu-id="26256-106">In Windows 7 and later, you should resort to Component Object Model (COM) code-based solutions only when the static methods are insufficient.</span></span>

<span data-ttu-id="26256-107">下列螢幕擷取畫面提供串聯功能表的範例。</span><span class="sxs-lookup"><span data-stu-id="26256-107">The following screen shot provides an example of a cascading menu.</span></span>

![顯示級聯功能表範例的螢幕擷取畫面](images/file-assoc/filecascademenu2ndex.png)

<span data-ttu-id="26256-109">在 Windows 7 和更新版本中，有三種方式可以建立串聯功能表，如下列各節所述。</span><span class="sxs-lookup"><span data-stu-id="26256-109">In Windows 7 and later, there are three ways to create cascading menus, which are described in the following sections.</span></span>

-   [<span data-ttu-id="26256-110">如何使用子命令登錄專案建立串聯功能表</span><span class="sxs-lookup"><span data-stu-id="26256-110">How to Create Cascading Menus with the SubCommands Registry Entry</span></span>](how-to--create-cascading-menus-with-the-subcommands-registry-entry.md)
-   [<span data-ttu-id="26256-111">如何使用 ExtendedSubCommandsKey 登錄專案建立串聯功能表</span><span class="sxs-lookup"><span data-stu-id="26256-111">How to Create Cascading Menus with the ExtendedSubCommandsKey Registry Entry</span></span>](how-to-create-cascading-menus-with-the-extendedsubcommandskey-registry-entry.md)
-   [<span data-ttu-id="26256-112">如何使用 IExplorerCommand 介面建立串聯功能表</span><span class="sxs-lookup"><span data-stu-id="26256-112">How to Create Cascading Menus with the IExplorerCommand Interface</span></span>](how-to-create-cascading-menus-with-the-iexplorercommand-interface.md)

 

 
