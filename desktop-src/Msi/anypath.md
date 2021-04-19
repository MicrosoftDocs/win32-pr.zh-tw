---
description: AnyPath 資料類型是一種文字字串，其中包含完整路徑或相對路徑。
ms.assetid: fe8a4d2a-1960-40af-a0e4-4d65accdd388
title: AnyPath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ab6265874616bb0bb1a2f61098cdbabfa8ea24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993096"
---
# <a name="anypath"></a><span data-ttu-id="c269c-103">AnyPath</span><span class="sxs-lookup"><span data-stu-id="c269c-103">AnyPath</span></span>

<span data-ttu-id="c269c-104">AnyPath 資料類型是一種文字字串，其中包含完整路徑或相對路徑。</span><span class="sxs-lookup"><span data-stu-id="c269c-104">The AnyPath data type is a text string containing either a full path or a relative path.</span></span> <span data-ttu-id="c269c-105">指定相對路徑時，您可以將簡短名稱和長名稱分隔 () ，以包含簡短檔案名的長檔名 \| 。</span><span class="sxs-lookup"><span data-stu-id="c269c-105">When specifying a relative path, you can include a long file name with the short file name by separating the short and long names with a vertical bar (\|).</span></span> <span data-ttu-id="c269c-106">請注意，您不能以這種方式指定目錄或完整路徑的多個層級。</span><span class="sxs-lookup"><span data-stu-id="c269c-106">Note that you cannot specify multiple levels of a directory or fully qualified paths in this way.</span></span> <span data-ttu-id="c269c-107">路徑中可能包含以方括弧括住的屬性 (\[ \]) 。</span><span class="sxs-lookup"><span data-stu-id="c269c-107">The path may contain properties enclosed within square brackets (\[ \]).</span></span>

<span data-ttu-id="c269c-108">有效 AnyPath 資料的範例：</span><span class="sxs-lookup"><span data-stu-id="c269c-108">Examples of valid AnyPath data:</span></span>

-   <span data-ttu-id="c269c-109">\\\\伺服器 \\ 共用 \\ 暫存</span><span class="sxs-lookup"><span data-stu-id="c269c-109">\\\\server\\share\\temp</span></span>
-   <span data-ttu-id="c269c-110">c： \\ temp</span><span class="sxs-lookup"><span data-stu-id="c269c-110">c:\\temp</span></span>
-   <span data-ttu-id="c269c-111">\\臨時</span><span class="sxs-lookup"><span data-stu-id="c269c-111">\\temp</span></span>
-   <span data-ttu-id="c269c-112">project ~ 1 個 \| 專案狀態</span><span class="sxs-lookup"><span data-stu-id="c269c-112">projec~1\|Project Status</span></span>

<span data-ttu-id="c269c-113">不正確 AnyPath 資料範例：</span><span class="sxs-lookup"><span data-stu-id="c269c-113">Examples of invalid AnyPath data:</span></span>

-   <span data-ttu-id="c269c-114">c： \\ temp \\ project ~ 1 \| c： \\ 暫存一個 \\ 專案狀態</span><span class="sxs-lookup"><span data-stu-id="c269c-114">c:\\temp\\projec~1\|c:\\temp one\\Project Status</span></span>
-   <span data-ttu-id="c269c-115">\\temp \\ project ~ 1 \| \\ Temp 一個 \\ 專案狀態</span><span class="sxs-lookup"><span data-stu-id="c269c-115">\\temp\\projec~1\|\\temp one\\Project Status</span></span>

 

 



