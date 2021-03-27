---
description: 示範如何定義、註冊、列舉和尋找目前系統上所有已知資料夾的路徑。
title: 已知資料夾範例
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 49799A9E-BA86-4977-B5F3-590BE1E5FBF6
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8d3784e64986a338f6554534199852191bd06ca7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944492"
---
# <a name="known-folders-sample"></a><span data-ttu-id="a7f7d-103">已知資料夾範例</span><span class="sxs-lookup"><span data-stu-id="a7f7d-103">Known Folders Sample</span></span>

<span data-ttu-id="a7f7d-104">示範如何定義、註冊、列舉和尋找目前系統上所有已知資料夾的路徑。</span><span class="sxs-lookup"><span data-stu-id="a7f7d-104">Demonstrates how to define, register, enumerate and find the path for all known folders on the current system.</span></span>

<span data-ttu-id="a7f7d-105">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="a7f7d-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="a7f7d-106">說明</span><span class="sxs-lookup"><span data-stu-id="a7f7d-106">Description</span></span>](#description)
-   [<span data-ttu-id="a7f7d-107">需求</span><span class="sxs-lookup"><span data-stu-id="a7f7d-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="a7f7d-108">下載範例</span><span class="sxs-lookup"><span data-stu-id="a7f7d-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="a7f7d-109">建立範例</span><span class="sxs-lookup"><span data-stu-id="a7f7d-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="a7f7d-110">執行範例</span><span class="sxs-lookup"><span data-stu-id="a7f7d-110">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="a7f7d-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="a7f7d-111">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="a7f7d-112">Description</span><span class="sxs-lookup"><span data-stu-id="a7f7d-112">Description</span></span>

<span data-ttu-id="a7f7d-113">此範例包含一個登錄檔案，示範如何為偏好登錄存取的開發人員撰寫一些常見的登錄機碼和值，以註冊已知的資料夾。</span><span class="sxs-lookup"><span data-stu-id="a7f7d-113">This sample includes a registry file that demonstrates how to register a known folder by writing some common registry keys and values for developers who prefer registry access.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7f7d-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="a7f7d-114">Requirements</span></span>



| <span data-ttu-id="a7f7d-115">產品</span><span class="sxs-lookup"><span data-stu-id="a7f7d-115">Product</span></span>                                | <span data-ttu-id="a7f7d-116">最小產品版本</span><span class="sxs-lookup"><span data-stu-id="a7f7d-116">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="a7f7d-117">Windows</span><span class="sxs-lookup"><span data-stu-id="a7f7d-117">Windows</span></span>                                | <span data-ttu-id="a7f7d-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a7f7d-118">Windows Vista</span></span>           |
| <span data-ttu-id="a7f7d-119">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="a7f7d-119">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="a7f7d-120">6.1</span><span class="sxs-lookup"><span data-stu-id="a7f7d-120">6.1</span></span>                     |



 

<span data-ttu-id="a7f7d-121">如需其他需求，請參閱範例隨附的讀我檔案。</span><span class="sxs-lookup"><span data-stu-id="a7f7d-121">For additional requirements, see the Readme file included with the sample.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="a7f7d-122">下載範例</span><span class="sxs-lookup"><span data-stu-id="a7f7d-122">Downloading the Sample</span></span>

| <span data-ttu-id="a7f7d-123">Location</span><span class="sxs-lookup"><span data-stu-id="a7f7d-123">Location</span></span>      | <span data-ttu-id="a7f7d-124">路徑 URL</span><span class="sxs-lookup"><span data-stu-id="a7f7d-124">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7f7d-125">GitHub</span><span class="sxs-lookup"><span data-stu-id="a7f7d-125">GitHub</span></span>  | [<span data-ttu-id="a7f7d-126">KnownFolders 範例</span><span class="sxs-lookup"><span data-stu-id="a7f7d-126">KnownFolders sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/knownfolders) |

## <a name="building-the-sample"></a><span data-ttu-id="a7f7d-127">建立範例</span><span class="sxs-lookup"><span data-stu-id="a7f7d-127">Building the Sample</span></span>

<span data-ttu-id="a7f7d-128">如需有關如何建立範例的指示，請參閱範例隨附的讀我檔案。</span><span class="sxs-lookup"><span data-stu-id="a7f7d-128">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="a7f7d-129">執行範例</span><span class="sxs-lookup"><span data-stu-id="a7f7d-129">Running the Sample</span></span>

<span data-ttu-id="a7f7d-130">如需有關如何建立範例的指示，請參閱範例隨附的讀我檔案。</span><span class="sxs-lookup"><span data-stu-id="a7f7d-130">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7f7d-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="a7f7d-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7f7d-132">已知的資料夾</span><span class="sxs-lookup"><span data-stu-id="a7f7d-132">Known Folders</span></span>](known-folders.md)
</dt> </dl>

 

 



