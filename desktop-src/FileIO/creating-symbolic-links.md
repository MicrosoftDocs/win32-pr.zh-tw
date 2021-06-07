---
description: 使用 CreateSymbolicLink 函數建立使用絕對或相對路徑的符號連結。
ms.assetid: 3821478d-87bb-4e47-8263-d977cf665503
title: 建立符號連結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 252b999b05004fd7735b16582783ef0c3afb0013
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387704"
---
# <a name="creating-symbolic-links"></a><span data-ttu-id="23adb-103">建立符號連結</span><span class="sxs-lookup"><span data-stu-id="23adb-103">Creating Symbolic Links</span></span>

<span data-ttu-id="23adb-104">函數 [**CreateSymbolicLink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) 可讓您使用絕對或相對路徑來建立符號連結。</span><span class="sxs-lookup"><span data-stu-id="23adb-104">The function [**CreateSymbolicLink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) allows you to create symbolic links using either an absolute or relative path.</span></span>

<span data-ttu-id="23adb-105">符號連結可以是絕對或相對連結。</span><span class="sxs-lookup"><span data-stu-id="23adb-105">Symbolic links can either be absolute or relative links.</span></span> <span data-ttu-id="23adb-106">絕對連結是指定路徑名稱的每個部分的連結;相對連結與指定路徑中的相對連結指定名稱，會決定相對連結。</span><span class="sxs-lookup"><span data-stu-id="23adb-106">Absolute links are links that specify each portion of the path name; relative links are determined relative to where relative–link specifiers are in a specified path.</span></span> <span data-ttu-id="23adb-107">相對連結會使用下列慣例來指定：</span><span class="sxs-lookup"><span data-stu-id="23adb-107">Relative links are specified using the following conventions:</span></span>

-   <span data-ttu-id="23adb-108">點 (。</span><span class="sxs-lookup"><span data-stu-id="23adb-108">Dot (.</span></span> <span data-ttu-id="23adb-109">和。。) 慣例，例如 \\ 「...」解析相對於上層目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="23adb-109">and ..) conventions—for example, "..\\" resolves the path relative to the parent directory.</span></span>
-   <span data-ttu-id="23adb-110">沒有斜線的名稱 (\\) ，例如 "tmp" 會解析相對於目前的目錄的路徑。</span><span class="sxs-lookup"><span data-stu-id="23adb-110">Names with no slashes (\\)—for example, "tmp" resolves the path relative to the current directory.</span></span>
-   <span data-ttu-id="23adb-111">根目錄相對，例如「 \\ windows system32」會 \\ 解析為「*目前磁片磁碟機*： \\ windows system32」 \\ 。</span><span class="sxs-lookup"><span data-stu-id="23adb-111">Root relative—for example, "\\Windows\\System32" resolves to the "*current drive*:\\Windows\\System32".</span></span> <span data-ttu-id="23adb-112">directory</span><span class="sxs-lookup"><span data-stu-id="23adb-112">directory</span></span>
-   <span data-ttu-id="23adb-113">目前的工作目錄相對，例如，如果目前的工作目錄是 "C： \\ windows \\ system32"，"C:File.txt" 會解析為 "c： \\ windows \\ system32 \\File.txt"。</span><span class="sxs-lookup"><span data-stu-id="23adb-113">Current working directory-relative—for example, if the current working directory is "C:\\Windows\\System32", "C:File.txt" resolves to "C:\\Windows\\System32\\File.txt".</span></span>

    <span data-ttu-id="23adb-114">**注意**  如果您指定目前的工作目錄相對連結，則會建立為絕對連結，因為根據使用者和執行緒目前工作目錄的方式。</span><span class="sxs-lookup"><span data-stu-id="23adb-114">**Note**  If you specify a current working directory–relative link, it is created as an absolute link, due to the way the current working directory is processed based on the user and the thread.</span></span>

<span data-ttu-id="23adb-115">符號連結也可以同時包含連接點和裝載的資料夾，作為路徑名稱的一部分。</span><span class="sxs-lookup"><span data-stu-id="23adb-115">A symbolic link can also contain both junction points and mounted folders as a part of the path name.</span></span>

<span data-ttu-id="23adb-116">符號連結可以直接指向使用 UNC 路徑的遠端檔案或目錄。</span><span class="sxs-lookup"><span data-stu-id="23adb-116">Symbolic links can point directly to a remote file or directory using the UNC path.</span></span>

<span data-ttu-id="23adb-117">相對符號連結會限制為單一磁片區。</span><span class="sxs-lookup"><span data-stu-id="23adb-117">Relative symbolic links are restricted to a single volume.</span></span>

## <a name="example-of-an-absolute-symbolic-link"></a><span data-ttu-id="23adb-118">絕對符號連結的範例</span><span class="sxs-lookup"><span data-stu-id="23adb-118">Example of an Absolute Symbolic Link</span></span>

<span data-ttu-id="23adb-119">在此範例中，原始路徑包含元件 '*x*'，這是絕對的符號連結。</span><span class="sxs-lookup"><span data-stu-id="23adb-119">In this example, the original path contains a component, '*x*', which is an absolute symbolic link.</span></span> <span data-ttu-id="23adb-120">當遇到 '*x*' 時，會將原始路徑的片段（最多加上 '*x*'）完全取代為 '*x*' 所指向的路徑。</span><span class="sxs-lookup"><span data-stu-id="23adb-120">When '*x*' is encountered, the fragment of the original path up to and including '*x*' is completely replaced by the path that is pointed to by '*x*'.</span></span> <span data-ttu-id="23adb-121">在 '*x*' 之後，路徑的其餘部分會附加至這個新路徑。</span><span class="sxs-lookup"><span data-stu-id="23adb-121">The remainder of the path after '*x*' is appended to this new path.</span></span> <span data-ttu-id="23adb-122">這現在會變成修改過的路徑。</span><span class="sxs-lookup"><span data-stu-id="23adb-122">This now becomes the modified path.</span></span>

<span data-ttu-id="23adb-123">X： "C： \\ Alpha \\ Beta \\ absLink \\ gamma \\ file"</span><span class="sxs-lookup"><span data-stu-id="23adb-123">X: "C:\\alpha\\beta\\absLink\\gamma\\file"</span></span>

<span data-ttu-id="23adb-124">Link： "absLink" 對應至 " \\ \\ machineB \\ share"</span><span class="sxs-lookup"><span data-stu-id="23adb-124">Link: "absLink" maps to "\\\\machineB\\share"</span></span>

<span data-ttu-id="23adb-125">修改的路徑： " \\ \\ machineB \\ share \\ gamma \\ file"</span><span class="sxs-lookup"><span data-stu-id="23adb-125">Modified Path: "\\\\machineB\\share\\gamma\\file"</span></span>

## <a name="example-of-a-relative-symbolic-links"></a><span data-ttu-id="23adb-126">相對符號連結的範例</span><span class="sxs-lookup"><span data-stu-id="23adb-126">Example of a Relative Symbolic Links</span></span>

<span data-ttu-id="23adb-127">在此範例中，原始路徑包含元件 '*x*'，也就是相對的符號連結。</span><span class="sxs-lookup"><span data-stu-id="23adb-127">In this example, the original path contains a component '*x*', which is a relative symbolic link.</span></span> <span data-ttu-id="23adb-128">當遇到 '*x*' 時 *，' x*' 會完全由 '*x*' 所指向的新片段取代。</span><span class="sxs-lookup"><span data-stu-id="23adb-128">When '*x*' is encountered, '*x*' is completely replaced by the new fragment pointed to by '*x*'.</span></span> <span data-ttu-id="23adb-129">'*X*' 之後路徑的其餘部分會附加至新的路徑。</span><span class="sxs-lookup"><span data-stu-id="23adb-129">The remainder of the path after '*x*', is appended to the new path.</span></span> <span data-ttu-id="23adb-130"> ( 的任何點。) 在這個新路徑中，取代在點 ( 之前出現的元件。) 。</span><span class="sxs-lookup"><span data-stu-id="23adb-130">Any dots (..) in this new path replace components that appear before the dots (..).</span></span> <span data-ttu-id="23adb-131">每一組點都取代上述的元件。</span><span class="sxs-lookup"><span data-stu-id="23adb-131">Each set of dots replace the component preceding.</span></span> <span data-ttu-id="23adb-132">如果 ( 的點數目。) 超過元件的數目，則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="23adb-132">If the number of dots (..) exceed the number of components, an error is returned.</span></span> <span data-ttu-id="23adb-133">否則，當所有元件取代都完成時，會保留最後一個修改過的路徑。</span><span class="sxs-lookup"><span data-stu-id="23adb-133">Otherwise, when all component replacement has finished, the final, modified path remains.</span></span>

<span data-ttu-id="23adb-134">X： C： \\ Alpha \\ Beta \\ 連結 \\ gamma \\ 檔</span><span class="sxs-lookup"><span data-stu-id="23adb-134">X: C:\\alpha\\beta\\link\\gamma\\file</span></span>

<span data-ttu-id="23adb-135">Link： "link" 對應至 ".... \\ \\theta</span><span class="sxs-lookup"><span data-stu-id="23adb-135">Link: "link" maps to "..\\..\\theta"</span></span>

<span data-ttu-id="23adb-136">修改的路徑： "C： \\ Alpha \\ Beta \\ ... \\ . \\theta \\ gamma \\ file "</span><span class="sxs-lookup"><span data-stu-id="23adb-136">Modified Path: "C:\\alpha\\beta\\..\\..\\theta\\gamma\\file"</span></span>

<span data-ttu-id="23adb-137">最終路徑： "C： \\ theta \\ gamma \\ file"</span><span class="sxs-lookup"><span data-stu-id="23adb-137">Final Path: "C:\\theta\\gamma\\file"</span></span>

## <a name="related-topics"></a><span data-ttu-id="23adb-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="23adb-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23adb-139">符號連結</span><span class="sxs-lookup"><span data-stu-id="23adb-139">Symbolic Links</span></span>](symbolic-links.md)
</dt> <dt>

[<span data-ttu-id="23adb-140">永久連結和接合</span><span class="sxs-lookup"><span data-stu-id="23adb-140">Hard Links and Junctions</span></span>](hard-links-and-junctions.md)
</dt> <dt>

[<span data-ttu-id="23adb-141">命名檔案、路徑和命名空間</span><span class="sxs-lookup"><span data-stu-id="23adb-141">Naming Files, Paths, and Namespaces</span></span>](naming-a-file.md)
</dt> </dl>

 

 



