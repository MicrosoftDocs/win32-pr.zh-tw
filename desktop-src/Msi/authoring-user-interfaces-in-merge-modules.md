---
description: 合併模組很少需要使用者介面。
ms.assetid: 53bd2064-09dd-406f-a8ff-7b04f3525b9f
title: 在合併模組中撰寫使用者介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2df8781efea35ddd854ef76c2155d4a2ded7f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997521"
---
# <a name="authoring-user-interfaces-in-merge-modules"></a><span data-ttu-id="81aa7-103">在合併模組中撰寫使用者介面</span><span class="sxs-lookup"><span data-stu-id="81aa7-103">Authoring User Interfaces in Merge Modules</span></span>

<span data-ttu-id="81aa7-104">合併模組很少需要使用者介面。</span><span class="sxs-lookup"><span data-stu-id="81aa7-104">Merge modules rarely require a user interface.</span></span> <span data-ttu-id="81aa7-105">釋放包含可安裝元件和使用者介面的合併模組，最終會限制模組使用者的彈性。</span><span class="sxs-lookup"><span data-stu-id="81aa7-105">Releasing a merge module that contains both installable components and a user interface ultimately restricts the flexibility of the module user.</span></span> <span data-ttu-id="81aa7-106">將元件和 UI 結合成一個模組，可防止開發人員使用自己的 UI 或提供無訊息安裝。</span><span class="sxs-lookup"><span data-stu-id="81aa7-106">Combining both components and UI into one module can prevent developers from using their own UI or from providing silent installations.</span></span> <span data-ttu-id="81aa7-107">更好的替代方式是釋放兩個合併模組，一個是以無訊息方式安裝元件，另一個則是包含 UI 的選擇性模組。</span><span class="sxs-lookup"><span data-stu-id="81aa7-107">A better alternative is to release two merge modules, one that silently installs the components and a second optional module that contains the UI.</span></span> <span data-ttu-id="81aa7-108">具有 UI 的模組應該會列出其 [ModuleDependency 資料表](moduledependency-table.md)中的元件模組。</span><span class="sxs-lookup"><span data-stu-id="81aa7-108">The module with the UI should list the component module in its [ModuleDependency table](moduledependency-table.md).</span></span> <span data-ttu-id="81aa7-109">此方法可讓模組作者提供 UI，而不需要在開發人員上強制執行。</span><span class="sxs-lookup"><span data-stu-id="81aa7-109">This method enables module authors to provide a UI without forcing it on developers.</span></span>

<span data-ttu-id="81aa7-110">當在合併模組中使用 UI 資料表時，可以使用與任何其他資料表相同的方式進行合併。</span><span class="sxs-lookup"><span data-stu-id="81aa7-110">When UI tables are used in merge modules they can be merged in the same way as any other tables.</span></span>

 

 



