---
title: Help 屬性
description: Help 屬性提供的資訊會告訴使用者物件的功能。
ms.assetid: 3df0cc01-cc99-42a1-9d56-591e6e00e53d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b240475d4583826e08fd6ee43b5839bdfb451d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300740"
---
# <a name="help-property"></a><span data-ttu-id="17d30-103">Help 屬性</span><span class="sxs-lookup"><span data-stu-id="17d30-103">Help Property</span></span>

<span data-ttu-id="17d30-104">**Help** 屬性提供的資訊會告訴使用者物件的功能。</span><span class="sxs-lookup"><span data-stu-id="17d30-104">The **Help** property provides information that tells the user about the function of an object.</span></span>

<span data-ttu-id="17d30-105">藉由呼叫 [**IAccessible：： get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)，即可抓取 **Help** 屬性。</span><span class="sxs-lookup"><span data-stu-id="17d30-105">The **Help** property is retrieved by calling [**IAccessible::get\_accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp).</span></span>

<span data-ttu-id="17d30-106">此屬性包含氣球樣式資訊 (如工具提示) 中所示，可用來描述物件的用途或使用方式。</span><span class="sxs-lookup"><span data-stu-id="17d30-106">This property contains balloon-style information (as found in ToolTips) that is used either to describe what the object does or how to use it.</span></span> <span data-ttu-id="17d30-107">例如，顯示印表機 **的工具列按鈕的 [說明** ] 屬性可能會提供下列文字：「列印目前的檔」。</span><span class="sxs-lookup"><span data-stu-id="17d30-107">For example, the **Help** property for a toolbar button that shows a printer might provide the following text: "Prints the current document."</span></span>

<span data-ttu-id="17d30-108">**Help** 屬性的文字在使用者介面中不一定是唯一的。</span><span class="sxs-lookup"><span data-stu-id="17d30-108">The text for the **Help** property does not have to be unique within the user interface.</span></span>

## <a name="when-to-support-the-help-property"></a><span data-ttu-id="17d30-109">何時支援 Help 屬性</span><span class="sxs-lookup"><span data-stu-id="17d30-109">When to Support the Help Property</span></span>

<span data-ttu-id="17d30-110">如果其他屬性提供物件用途的足夠資訊，以及物件執行的動作，則伺服器不支援 [說明 **] 屬性。**</span><span class="sxs-lookup"><span data-stu-id="17d30-110">Servers do not support the **Help** property if other properties provide sufficient information about the object's purpose and the actions the object performs.</span></span> <span data-ttu-id="17d30-111">公開系統提供之控制項的可存取物件不支援 **Help** 屬性。</span><span class="sxs-lookup"><span data-stu-id="17d30-111">Accessible objects that expose system-provided controls do not support the **Help** property.</span></span>

 

 




