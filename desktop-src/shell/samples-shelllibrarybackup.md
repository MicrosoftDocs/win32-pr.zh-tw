---
description: 示範如何將程式庫列舉為容器。
title: Shell 程式庫備份範例
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 206356B2-3998-4a19-BC4D-F6A043AFDBD3
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7e1b4746d2e559b567adb4cbd2305ea474b03129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973752"
---
# <a name="shell-library-backup-sample"></a><span data-ttu-id="33b46-103">Shell 程式庫備份範例</span><span class="sxs-lookup"><span data-stu-id="33b46-103">Shell Library Backup Sample</span></span>

<span data-ttu-id="33b46-104">示範如何將程式庫列舉為容器。</span><span class="sxs-lookup"><span data-stu-id="33b46-104">Demonstrates how to enumerate libraries as containers.</span></span> <span data-ttu-id="33b46-105">程式庫是使用者檔案的新存放裝置範例，在 Windows 7 中引進。</span><span class="sxs-lookup"><span data-stu-id="33b46-105">Libraries are the new storage paradigm for user files and are introduced in Windows 7.</span></span>

<span data-ttu-id="33b46-106">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="33b46-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="33b46-107">說明</span><span class="sxs-lookup"><span data-stu-id="33b46-107">Description</span></span>](#description)
-   [<span data-ttu-id="33b46-108">需求</span><span class="sxs-lookup"><span data-stu-id="33b46-108">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="33b46-109">下載範例</span><span class="sxs-lookup"><span data-stu-id="33b46-109">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="33b46-110">建立範例</span><span class="sxs-lookup"><span data-stu-id="33b46-110">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="33b46-111">執行範例</span><span class="sxs-lookup"><span data-stu-id="33b46-111">Running the Sample</span></span>](#running-the-sample)

## <a name="description"></a><span data-ttu-id="33b46-112">Description</span><span class="sxs-lookup"><span data-stu-id="33b46-112">Description</span></span>

<span data-ttu-id="33b46-113">此範例是虛構的備份應用程式，示範如何透過 [一般檔案] 對話方塊來挑選程式庫。</span><span class="sxs-lookup"><span data-stu-id="33b46-113">This sample is a fictional backup application that shows how to pick libraries through the common file dialog.</span></span> <span data-ttu-id="33b46-114">它也會示範如何使用 Shell 命名空間檢視器來備份程式庫。</span><span class="sxs-lookup"><span data-stu-id="33b46-114">It also demonstrates how to back up libraries using the Shell namespace walker.</span></span>

## <a name="requirements"></a><span data-ttu-id="33b46-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="33b46-115">Requirements</span></span>



| <span data-ttu-id="33b46-116">產品</span><span class="sxs-lookup"><span data-stu-id="33b46-116">Product</span></span>                                | <span data-ttu-id="33b46-117">最小產品版本</span><span class="sxs-lookup"><span data-stu-id="33b46-117">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="33b46-118">Windows</span><span class="sxs-lookup"><span data-stu-id="33b46-118">Windows</span></span>                                | <span data-ttu-id="33b46-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="33b46-119">Windows 7</span></span>               |
| <span data-ttu-id="33b46-120">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="33b46-120">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="33b46-121">7.0</span><span class="sxs-lookup"><span data-stu-id="33b46-121">7.0</span></span>                     |



 

<span data-ttu-id="33b46-122">如需其他需求，請參閱範例隨附的讀我檔案。</span><span class="sxs-lookup"><span data-stu-id="33b46-122">For additional requirements, see the Readme file included with the sample.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="33b46-123">下載範例</span><span class="sxs-lookup"><span data-stu-id="33b46-123">Downloading the Sample</span></span>

| <span data-ttu-id="33b46-124">Location</span><span class="sxs-lookup"><span data-stu-id="33b46-124">Location</span></span>      | <span data-ttu-id="33b46-125">路徑 URL</span><span class="sxs-lookup"><span data-stu-id="33b46-125">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33b46-126">GitHub</span><span class="sxs-lookup"><span data-stu-id="33b46-126">GitHub</span></span>  | [<span data-ttu-id="33b46-127">ShellLibraryBackup 範例</span><span class="sxs-lookup"><span data-stu-id="33b46-127">ShellLibraryBackup sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/ShellLibraryBackup) |

## <a name="building-the-sample"></a><span data-ttu-id="33b46-128">建立範例</span><span class="sxs-lookup"><span data-stu-id="33b46-128">Building the Sample</span></span>

<span data-ttu-id="33b46-129">如需有關如何建立範例的指示，請參閱範例隨附的讀我檔案。</span><span class="sxs-lookup"><span data-stu-id="33b46-129">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="33b46-130">執行範例</span><span class="sxs-lookup"><span data-stu-id="33b46-130">Running the Sample</span></span>

<span data-ttu-id="33b46-131">如需有關如何建立範例的指示，請參閱範例隨附的讀我檔案。</span><span class="sxs-lookup"><span data-stu-id="33b46-131">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

 

 



