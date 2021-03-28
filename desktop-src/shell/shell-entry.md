---
description: Windows UI 可讓使用者存取執行應用程式和管理作業系統所需的各種物件。
title: Windows Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 1d0d4ed7-9b85-4d70-bf1f-82567a1687fb
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 448e1d5265ec34ce1889ca36f234622e2b082553
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973324"
---
# <a name="windows-shell"></a><span data-ttu-id="e1286-103">Windows Shell</span><span class="sxs-lookup"><span data-stu-id="e1286-103">Windows Shell</span></span>

<span data-ttu-id="e1286-104">Windows UI 可讓使用者存取執行應用程式和管理作業系統所需的各種物件。</span><span class="sxs-lookup"><span data-stu-id="e1286-104">The Windows UI provides users with access to a wide variety of objects necessary for running applications and managing the operating system.</span></span> <span data-ttu-id="e1286-105">這些物件最多與熟悉的是位於電腦磁片磁碟機上的資料夾和檔案。</span><span class="sxs-lookup"><span data-stu-id="e1286-105">The most numerous and familiar of these objects are the folders and files that reside on computer disk drives.</span></span> <span data-ttu-id="e1286-106">另外還有一些虛擬物件，可讓使用者執行工作，例如將檔案傳送至遠端印表機或存取資源回收筒。</span><span class="sxs-lookup"><span data-stu-id="e1286-106">There are also a number of virtual objects that allow the user to perform tasks such as sending files to remote printers or accessing the Recycle Bin.</span></span> <span data-ttu-id="e1286-107">Shell 會將這些物件組織成階層命名空間，並為使用者和應用程式提供一致且有效率的方式來存取和管理物件。</span><span class="sxs-lookup"><span data-stu-id="e1286-107">The Shell organizes these objects into a hierarchical namespace and provides users and applications with a consistent and efficient way to access and manage objects.</span></span>

## <a name="shell-development-scenarios"></a><span data-ttu-id="e1286-108">Shell 開發案例</span><span class="sxs-lookup"><span data-stu-id="e1286-108">Shell Development Scenarios</span></span>

<span data-ttu-id="e1286-109">下列開發案例與應用程式開發有關：</span><span class="sxs-lookup"><span data-stu-id="e1286-109">The following development scenarios relate to application development:</span></span>

-   <span data-ttu-id="e1286-110">擴充 Shell，其包含建立資料來源 (與取用 Shell 資料模型) </span><span class="sxs-lookup"><span data-stu-id="e1286-110">Extending the Shell, which consists of creating a data source (versus consuming the Shell data model)</span></span>
-   <span data-ttu-id="e1286-111">執行 Shell 資料來源工作的子集</span><span class="sxs-lookup"><span data-stu-id="e1286-111">Implementing a subset of the Shell data source tasks</span></span>
-   <span data-ttu-id="e1286-112">支援 Windows 檔案總管中的程式庫和專案視圖</span><span class="sxs-lookup"><span data-stu-id="e1286-112">Supporting libraries and item views in Windows Explorer</span></span>
-   <span data-ttu-id="e1286-113">使用一般檔案對話方塊</span><span class="sxs-lookup"><span data-stu-id="e1286-113">Using the common file dialog</span></span>
-   <span data-ttu-id="e1286-114">執行主控台專案</span><span class="sxs-lookup"><span data-stu-id="e1286-114">Implementing Control Panel items</span></span>
-   <span data-ttu-id="e1286-115">管理通知</span><span class="sxs-lookup"><span data-stu-id="e1286-115">Managing notifications</span></span>

<span data-ttu-id="e1286-116">下列開發案例與檔案格式擁有權有關：</span><span class="sxs-lookup"><span data-stu-id="e1286-116">The following development scenarios relate to file format ownership:</span></span>

-   <span data-ttu-id="e1286-117">執行 Shell 資料來源工作的子集</span><span class="sxs-lookup"><span data-stu-id="e1286-117">Implementing a subset of the Shell data source tasks</span></span>
-   <span data-ttu-id="e1286-118">執行任何處理程式</span><span class="sxs-lookup"><span data-stu-id="e1286-118">Implementing any handler</span></span>
-   <span data-ttu-id="e1286-119">支援桌面搜尋</span><span class="sxs-lookup"><span data-stu-id="e1286-119">Supporting desktop search</span></span>

<span data-ttu-id="e1286-120">下列開發案例與資料儲存體擁有權有關：</span><span class="sxs-lookup"><span data-stu-id="e1286-120">The following development scenarios relate to data storage ownership:</span></span>

-   <span data-ttu-id="e1286-121">支援桌面搜尋和 OpenSearch</span><span class="sxs-lookup"><span data-stu-id="e1286-121">Supporting desktop search and OpenSearch</span></span>
-   <span data-ttu-id="e1286-122"> (虛擬資料夾執行 Shell 資料來源工作的子集) </span><span class="sxs-lookup"><span data-stu-id="e1286-122">Implementing a subset of the Shell data source tasks (virtual folders)</span></span>
-   <span data-ttu-id="e1286-123">Windows 檔案總管中的支援程式庫</span><span class="sxs-lookup"><span data-stu-id="e1286-123">Supporting libraries in Windows Explorer</span></span>

<span data-ttu-id="e1286-124">下列開發案例與裝置支援相關：</span><span class="sxs-lookup"><span data-stu-id="e1286-124">The following development scenario relates to device support:</span></span>

-   <span data-ttu-id="e1286-125">自動執行和自動播放</span><span class="sxs-lookup"><span data-stu-id="e1286-125">Auto run and auto play</span></span>

## <a name="windows-shell-sdk-documentation"></a><span data-ttu-id="e1286-126">Windows Shell SDK 檔</span><span class="sxs-lookup"><span data-stu-id="e1286-126">Windows Shell SDK Documentation</span></span>

<span data-ttu-id="e1286-127">本檔分為三個主要部分：</span><span class="sxs-lookup"><span data-stu-id="e1286-127">This documentation is broken into three major sections:</span></span>

-   <span data-ttu-id="e1286-128">[Shell 開發人員指南](intro.md)提供有關 Shell 如何運作的概念資料，以及如何在您的應用程式中使用 SHELL 的 API。</span><span class="sxs-lookup"><span data-stu-id="e1286-128">The [Shell Developer's Guide](intro.md) provides conceptual material about how the Shell works and how to use the Shell's API in your application.</span></span>
-   <span data-ttu-id="e1286-129">[ [Shell 參考](shell-reference-bumper.md) ] 區段記錄組成各種 Shell api 的程式設計項目。</span><span class="sxs-lookup"><span data-stu-id="e1286-129">The [Shell Reference](shell-reference-bumper.md) section documents programming elements that make up the various Shell APIs.</span></span>
-   <span data-ttu-id="e1286-130">[Shell 範例](samples-entry.md) 提供相關程式碼範例的連結。</span><span class="sxs-lookup"><span data-stu-id="e1286-130">[Shell Samples](samples-entry.md) provides links to related code samples.</span></span>

<span data-ttu-id="e1286-131">下表提供 [Shell 參考] 區段的大綱。</span><span class="sxs-lookup"><span data-stu-id="e1286-131">The following table provides an outline of the Shell Reference section.</span></span> <span data-ttu-id="e1286-132">除非另有說明，否則所有程式設計項目都會記載在非受控 c + + 中。</span><span class="sxs-lookup"><span data-stu-id="e1286-132">Unless otherwise noted, all programming elements are documented in unmanaged C++.</span></span>



| <span data-ttu-id="e1286-133">區段</span><span class="sxs-lookup"><span data-stu-id="e1286-133">Section</span></span>                                                               | <span data-ttu-id="e1286-134">描述</span><span class="sxs-lookup"><span data-stu-id="e1286-134">Description</span></span>                                                                                                          |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e1286-135">Shell 類別</span><span class="sxs-lookup"><span data-stu-id="e1286-135">Shell Classes</span></span>](classes.md)                                          | <span data-ttu-id="e1286-136">本節說明如何選取 Windows Shell 類別。</span><span class="sxs-lookup"><span data-stu-id="e1286-136">This section describes select Windows Shell classes.</span></span>                                                                 |
| [<span data-ttu-id="e1286-137">Shell 介面</span><span class="sxs-lookup"><span data-stu-id="e1286-137">Shell Interfaces</span></span>](interfaces.md)                                    | <span data-ttu-id="e1286-138">本節說明 (COM) 介面的 Windows Shell 元件物件模型。</span><span class="sxs-lookup"><span data-stu-id="e1286-138">This section describes the Windows Shell Component Object Model (COM) interfaces.</span></span>                                    |
| [<span data-ttu-id="e1286-139">Shell 函數</span><span class="sxs-lookup"><span data-stu-id="e1286-139">Shell Functions</span></span>](functions.md)                                      | <span data-ttu-id="e1286-140">本節說明 Windows Shell 函數。</span><span class="sxs-lookup"><span data-stu-id="e1286-140">This section describes the Windows Shell functions.</span></span>                                                                  |
| [<span data-ttu-id="e1286-141">Shell 回呼函數</span><span class="sxs-lookup"><span data-stu-id="e1286-141">Shell Callback Functions</span></span>](callbacks.md)                             | <span data-ttu-id="e1286-142">本節說明 Windows Shell 回呼函式範本。</span><span class="sxs-lookup"><span data-stu-id="e1286-142">This section describes the Windows Shell callback functions templates.</span></span>                                               |
| [<span data-ttu-id="e1286-143">Shell 常數、列舉和旗標</span><span class="sxs-lookup"><span data-stu-id="e1286-143">Shell Constants, Enumerations, and Flags</span></span>](consts-enums-flags.md)    | <span data-ttu-id="e1286-144">本節說明 Shell Api 中所使用的 Windows Shell 常數、列舉和旗標。</span><span class="sxs-lookup"><span data-stu-id="e1286-144">This section describes the Windows Shell constants, enumerations, and flags used in the Shell APIs.</span></span>                  |
| [<span data-ttu-id="e1286-145">Shell 輕量公用程式函式</span><span class="sxs-lookup"><span data-stu-id="e1286-145">Shell Lightweight Utility Functions</span></span>](shlwapi.md)                    | <span data-ttu-id="e1286-146">本節說明 Shlwapi.dll 中提供的 Windows Shell 輕量公用程式函式。</span><span class="sxs-lookup"><span data-stu-id="e1286-146">This section describes the Windows Shell lightweight utility functions provided in Shlwapi.dll.</span></span>                      |
| [<span data-ttu-id="e1286-147">Shell 宏</span><span class="sxs-lookup"><span data-stu-id="e1286-147">Shell Macros</span></span>](macros.md)                                            | <span data-ttu-id="e1286-148">本節說明 Windows Shell 公用程式宏。</span><span class="sxs-lookup"><span data-stu-id="e1286-148">This section describes the Windows Shell utility macros.</span></span>                                                             |
| [<span data-ttu-id="e1286-149">Shell 訊息和通知</span><span class="sxs-lookup"><span data-stu-id="e1286-149">Shell Messages and Notifications</span></span>](messages.md)                      | <span data-ttu-id="e1286-150">本節說明 Windows Shell 的元素所傳送的訊息和通知。</span><span class="sxs-lookup"><span data-stu-id="e1286-150">This section describes the messages and notifications sent by elements of the Windows Shell.</span></span>                         |
| [<span data-ttu-id="e1286-151">腳本和 Microsoft Visual Basic 的 Shell 物件</span><span class="sxs-lookup"><span data-stu-id="e1286-151">Shell Objects for Scripting and Microsoft Visual Basic</span></span>](objects.md) | <span data-ttu-id="e1286-152">本節描述 Shell 所執行的 Windows 物件，以用於腳本和 Microsoft Visual Basic。</span><span class="sxs-lookup"><span data-stu-id="e1286-152">This section describes the Windows objects implemented by the Shell for use in scripting and Microsoft Visual Basic.</span></span> |
| [<span data-ttu-id="e1286-153">C + + 的 Shell 物件</span><span class="sxs-lookup"><span data-stu-id="e1286-153">Shell Objects for C++</span></span>](objects-cpp.md)                              | <span data-ttu-id="e1286-154">本節說明 Shell 所執行的 c + + Windows 物件。</span><span class="sxs-lookup"><span data-stu-id="e1286-154">This section describes the C++ Windows objects implemented by the Shell.</span></span>                                             |
| [<span data-ttu-id="e1286-155">Shell 架構</span><span class="sxs-lookup"><span data-stu-id="e1286-155">Shell Schemas</span></span>](schemas.md)                                          | <span data-ttu-id="e1286-156">本節說明 Windows Shell 所使用的程式庫、屬性和傳輸資訊清單架構。</span><span class="sxs-lookup"><span data-stu-id="e1286-156">This section describes library, property, and transfer manifest schemas used by the Windows Shell.</span></span>                   |
| [<span data-ttu-id="e1286-157">Shell 結構</span><span class="sxs-lookup"><span data-stu-id="e1286-157">Shell Structures</span></span>](structures.md)                                    | <span data-ttu-id="e1286-158">本節說明 Shell Api 中使用的 Windows Shell 結構。</span><span class="sxs-lookup"><span data-stu-id="e1286-158">This section describes the Windows Shell structures used in the Shell APIs.</span></span>                                          |



 

 

 



