---
description: 示範如何使用 IShellLibrary 介面建立命令列應用程式，以提供程式設計的方式來檢查和操作程式庫和程式庫檔案。
title: Shell 程式庫命令列範例
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 5EC06E69-8AC8-4d9e-BAFC-C1AFC1294023
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c9db182498791fee344061c91ea570ed770f3a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104469472"
---
# <a name="shell-library-command-line-sample"></a><span data-ttu-id="6a7c5-103">Shell 程式庫命令列範例</span><span class="sxs-lookup"><span data-stu-id="6a7c5-103">Shell Library Command Line Sample</span></span>

<span data-ttu-id="6a7c5-104">示範如何使用 [**IShellLibrary**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) 介面建立命令列應用程式，以提供程式設計的方式來檢查和操作程式庫和程式庫檔案。</span><span class="sxs-lookup"><span data-stu-id="6a7c5-104">Demonstrates how to use the [**IShellLibrary**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) interface to create a command-line application that provides programmatic access for inspecting and manipulating libraries and library files.</span></span>

<span data-ttu-id="6a7c5-105">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="6a7c5-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="6a7c5-106">需求</span><span class="sxs-lookup"><span data-stu-id="6a7c5-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="6a7c5-107">下載範例</span><span class="sxs-lookup"><span data-stu-id="6a7c5-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="6a7c5-108">建立範例</span><span class="sxs-lookup"><span data-stu-id="6a7c5-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="6a7c5-109">執行範例</span><span class="sxs-lookup"><span data-stu-id="6a7c5-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="6a7c5-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="6a7c5-110">Requirements</span></span>



| <span data-ttu-id="6a7c5-111">產品</span><span class="sxs-lookup"><span data-stu-id="6a7c5-111">Product</span></span>                                | <span data-ttu-id="6a7c5-112">最小產品版本</span><span class="sxs-lookup"><span data-stu-id="6a7c5-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="6a7c5-113">Windows</span><span class="sxs-lookup"><span data-stu-id="6a7c5-113">Windows</span></span>                                | <span data-ttu-id="6a7c5-114">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6a7c5-114">Windows 7</span></span>               |
| <span data-ttu-id="6a7c5-115">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="6a7c5-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="6a7c5-116">7.0</span><span class="sxs-lookup"><span data-stu-id="6a7c5-116">7.0</span></span>                     |



 

<span data-ttu-id="6a7c5-117">如需其他需求，請參閱範例隨附的讀我檔案。</span><span class="sxs-lookup"><span data-stu-id="6a7c5-117">For additional requirements, see the Readme file included with the sample.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="6a7c5-118">下載範例</span><span class="sxs-lookup"><span data-stu-id="6a7c5-118">Downloading the Sample</span></span>

| <span data-ttu-id="6a7c5-119">Location</span><span class="sxs-lookup"><span data-stu-id="6a7c5-119">Location</span></span>      | <span data-ttu-id="6a7c5-120">路徑 URL</span><span class="sxs-lookup"><span data-stu-id="6a7c5-120">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a7c5-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="6a7c5-121">GitHub</span></span>  | [<span data-ttu-id="6a7c5-122">ShellLibraryCommandLine 範例</span><span class="sxs-lookup"><span data-stu-id="6a7c5-122">ShellLibraryCommandLine sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/ShellLibraryCommandLine) |

## <a name="building-the-sample"></a><span data-ttu-id="6a7c5-123">建立範例</span><span class="sxs-lookup"><span data-stu-id="6a7c5-123">Building the Sample</span></span>

<span data-ttu-id="6a7c5-124">如需有關如何建立範例的指示，請參閱範例隨附的讀我檔案。</span><span class="sxs-lookup"><span data-stu-id="6a7c5-124">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="6a7c5-125">執行範例</span><span class="sxs-lookup"><span data-stu-id="6a7c5-125">Running the Sample</span></span>

<span data-ttu-id="6a7c5-126">如需有關如何建立範例的指示，請參閱範例隨附的讀我檔案。</span><span class="sxs-lookup"><span data-stu-id="6a7c5-126">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

 

 



