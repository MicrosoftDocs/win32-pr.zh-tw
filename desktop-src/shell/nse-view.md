---
description: 大部分的命名空間延伸是 Shell 命名空間的子集。
ms.assetid: 00b6b281-b157-4a61-9852-8aafd9ba68d3
title: 顯示命名空間延伸模組的 Self-Contained 視圖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b6f8555cfb8cdac6248c5ea1c70ce8af29bfd16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973376"
---
# <a name="displaying-a-self-contained-view-of-a-namespace-extension"></a><span data-ttu-id="caecb-103">顯示命名空間延伸模組的 Self-Contained 視圖</span><span class="sxs-lookup"><span data-stu-id="caecb-103">Displaying a Self-Contained View of a Namespace Extension</span></span>

<span data-ttu-id="caecb-104">大部分的命名空間延伸是 Shell 命名空間的子集。</span><span class="sxs-lookup"><span data-stu-id="caecb-104">Most namespace extensions are a subset of the Shell namespace.</span></span> <span data-ttu-id="caecb-105">當您建立連接點時，如 [指定命名空間延伸模組的位置](nse-junction.md)所述，Windows 檔案總管可讓使用者流覽至您的命名空間延伸模組，就像任何其他資料夾一樣。</span><span class="sxs-lookup"><span data-stu-id="caecb-105">When you create a junction point, as described in [Specifying a Namespace Extension's Location](nse-junction.md), Windows Explorer allows users to navigate into and out of your namespace extension just like any other folder.</span></span> <span data-ttu-id="caecb-106">不過，您也可以使用 Windows 檔案總管，只顯示命名空間延伸模組的內容。</span><span class="sxs-lookup"><span data-stu-id="caecb-106">However, it is also possible to use Windows Explorer to display only the contents of your namespace extension.</span></span> <span data-ttu-id="caecb-107">此顯示選項有時稱為 *根視圖*。</span><span class="sxs-lookup"><span data-stu-id="caecb-107">This display option is sometimes referred to as a *rooted view*.</span></span> <span data-ttu-id="caecb-108">雖然不常用，但在某些類型的延伸模組中，根視圖可能較適合一般的視圖。</span><span class="sxs-lookup"><span data-stu-id="caecb-108">Although not commonly used, rooted views might be preferable to normal views for some types of extensions.</span></span>

<span data-ttu-id="caecb-109">使用根視圖時，會建立 Windows 檔案總管的新實例，將延伸模組的內容顯示為個別的命名空間。</span><span class="sxs-lookup"><span data-stu-id="caecb-109">With a rooted view, a new instance of Windows Explorer is created that displays the contents of the extension as a separate namespace.</span></span> <span data-ttu-id="caecb-110">根目錄檢視的樹狀檢視只會顯示屬於延伸模組一部分的資料夾。</span><span class="sxs-lookup"><span data-stu-id="caecb-110">The tree view of a rooted view shows only those folders that are part of the extension.</span></span> <span data-ttu-id="caecb-111">使用者無法從根視圖流覽至 Shell 命名空間的其他部分。</span><span class="sxs-lookup"><span data-stu-id="caecb-111">Users cannot navigate from a rooted view to other parts of the Shell namespace.</span></span>

<span data-ttu-id="caecb-112">針對根視圖，擴充功能的執行方式就如同一般的視圖一樣。</span><span class="sxs-lookup"><span data-stu-id="caecb-112">Extensions are implemented in the same way for rooted views as they are for normal views.</span></span> <span data-ttu-id="caecb-113">唯一的差別在於，Windows 檔案總管會顯示延伸模組內容的方式。</span><span class="sxs-lookup"><span data-stu-id="caecb-113">The only difference is in the way the contents of the extension are displayed by Windows Explorer.</span></span> <span data-ttu-id="caecb-114">您甚至可以讓相同的延伸模組具有一般和根目錄的觀點。</span><span class="sxs-lookup"><span data-stu-id="caecb-114">It is even possible to have normal and rooted views of the same extension.</span></span>

<span data-ttu-id="caecb-115">若要開啟延伸模組的視圖，您必須使用/root 旗標啟動 Explorer.exe 的實例。</span><span class="sxs-lookup"><span data-stu-id="caecb-115">To open a view of an extension, you must launch an instance of Explorer.exe with a /root flag.</span></span> <span data-ttu-id="caecb-116">有幾種不同的方式可以啟動根目錄檢視，視擴充功能的本質而定。</span><span class="sxs-lookup"><span data-stu-id="caecb-116">There are several different ways to launch a rooted view, depending on the nature of your extension.</span></span>

-   [<span data-ttu-id="caecb-117">如何使用連接點開啟根視圖</span><span class="sxs-lookup"><span data-stu-id="caecb-117">How To Use a Junction Point to Open a Rooted View</span></span>](how-to-use-a-junction-point-to-open-a-rooted-view.md)
-   [<span data-ttu-id="caecb-118">如何使用快捷方式檔案開啟根視圖</span><span class="sxs-lookup"><span data-stu-id="caecb-118">How To Use a Shortcut File to Open a Rooted View</span></span>](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
-   [<span data-ttu-id="caecb-119">如何顯示檔案的根目錄檢視</span><span class="sxs-lookup"><span data-stu-id="caecb-119">How To Display a Rooted View of a File</span></span>](how-to-display-a-rooted-view-of-a-file.md)

 

 



