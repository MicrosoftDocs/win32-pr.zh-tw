---
description: 示範如何使用 Shell 程式設計模型，建立具有查詢準則約束的搜尋。
title: 搜尋資料夾範例
ms.topic: article
ms.date: 05/31/2018
ms.assetid: DF3432AB-39DF-44c6-9A08-4630408D6B9B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c86a29c4a7d01fad3b91db20035cb84751e0b78a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193730"
---
# <a name="search-folder-sample"></a><span data-ttu-id="a3562-103">搜尋資料夾範例</span><span class="sxs-lookup"><span data-stu-id="a3562-103">Search Folder Sample</span></span>

<span data-ttu-id="a3562-104">示範如何使用 Shell 程式設計模型，建立具有查詢準則約束的搜尋。</span><span class="sxs-lookup"><span data-stu-id="a3562-104">Demonstrates how to create a search with query constraints using the Shell programming model.</span></span>

<span data-ttu-id="a3562-105">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="a3562-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="a3562-106">說明</span><span class="sxs-lookup"><span data-stu-id="a3562-106">Description</span></span>](#description)
-   [<span data-ttu-id="a3562-107">需求</span><span class="sxs-lookup"><span data-stu-id="a3562-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="a3562-108">下載範例</span><span class="sxs-lookup"><span data-stu-id="a3562-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="a3562-109">建立範例</span><span class="sxs-lookup"><span data-stu-id="a3562-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="a3562-110">執行範例</span><span class="sxs-lookup"><span data-stu-id="a3562-110">Running the Sample</span></span>](#running-the-sample)

## <a name="description"></a><span data-ttu-id="a3562-111">Description</span><span class="sxs-lookup"><span data-stu-id="a3562-111">Description</span></span>

<span data-ttu-id="a3562-112">這個範例會示範如何使用 [**ISearchFolderItemFactory**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) 介面來建立受條件約束的搜尋，以 (代表查詢的容器) 來建立資料夾 Shell 專案。</span><span class="sxs-lookup"><span data-stu-id="a3562-112">This sample shows how to create a constrained search by using the [**ISearchFolderItemFactory**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory) interface to construct a folder Shell item (a container) that represents the query.</span></span> <span data-ttu-id="a3562-113">結果會使用 [開啟檔案] 對話方塊來顯示。</span><span class="sxs-lookup"><span data-stu-id="a3562-113">The results are displayed using the file open dialog.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3562-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="a3562-114">Requirements</span></span>



| <span data-ttu-id="a3562-115">產品</span><span class="sxs-lookup"><span data-stu-id="a3562-115">Product</span></span>                                | <span data-ttu-id="a3562-116">最小產品版本</span><span class="sxs-lookup"><span data-stu-id="a3562-116">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="a3562-117">Windows</span><span class="sxs-lookup"><span data-stu-id="a3562-117">Windows</span></span>                                | <span data-ttu-id="a3562-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a3562-118">Windows Vista</span></span>           |
| <span data-ttu-id="a3562-119">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="a3562-119">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="a3562-120">7.0</span><span class="sxs-lookup"><span data-stu-id="a3562-120">7.0</span></span>                     |



 

<span data-ttu-id="a3562-121">如需其他需求，請參閱範例隨附的讀我檔案。</span><span class="sxs-lookup"><span data-stu-id="a3562-121">For additional requirements, see the Readme file included with the sample.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="a3562-122">下載範例</span><span class="sxs-lookup"><span data-stu-id="a3562-122">Downloading the Sample</span></span>

| <span data-ttu-id="a3562-123">Location</span><span class="sxs-lookup"><span data-stu-id="a3562-123">Location</span></span>      | <span data-ttu-id="a3562-124">路徑 URL</span><span class="sxs-lookup"><span data-stu-id="a3562-124">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3562-125">GitHub</span><span class="sxs-lookup"><span data-stu-id="a3562-125">GitHub</span></span>  | [<span data-ttu-id="a3562-126">SearchFolder 範例</span><span class="sxs-lookup"><span data-stu-id="a3562-126">SearchFolder sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/searchfolder) |

## <a name="building-the-sample"></a><span data-ttu-id="a3562-127">建立範例</span><span class="sxs-lookup"><span data-stu-id="a3562-127">Building the Sample</span></span>

<span data-ttu-id="a3562-128">如需有關如何建立範例的指示，請參閱範例隨附的讀我檔案。</span><span class="sxs-lookup"><span data-stu-id="a3562-128">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="a3562-129">執行範例</span><span class="sxs-lookup"><span data-stu-id="a3562-129">Running the Sample</span></span>

<span data-ttu-id="a3562-130">如需有關如何建立範例的指示，請參閱範例隨附的讀我檔案。</span><span class="sxs-lookup"><span data-stu-id="a3562-130">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

 

 



