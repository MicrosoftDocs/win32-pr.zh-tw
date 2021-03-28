---
description: 示範如何從 Windows 檔案總管進程呼叫 ShellExecute 函數。
title: 在 Explorer 中執行範例
ms.topic: article
ms.date: 05/31/2018
ms.assetid: D307B22A-E4A3-4215-B28E-F48A721260A1
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7a511f7ccc7edd218edd405de163501afd530f46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973297"
---
# <a name="execute-in-explorer-sample"></a><span data-ttu-id="b24bc-103">在 Explorer 中執行範例</span><span class="sxs-lookup"><span data-stu-id="b24bc-103">Execute In Explorer Sample</span></span>

<span data-ttu-id="b24bc-104">示範如何從 Windows 檔案總管進程呼叫 [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) 函數。</span><span class="sxs-lookup"><span data-stu-id="b24bc-104">Demonstrates how to call the [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) function from the Windows Explorer process.</span></span> <span data-ttu-id="b24bc-105">從提升許可權的進程啟動停權一致程式時，這非常有用。</span><span class="sxs-lookup"><span data-stu-id="b24bc-105">This is useful when launching an unelevated process from an elevated process.</span></span>

<span data-ttu-id="b24bc-106">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="b24bc-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="b24bc-107">需求</span><span class="sxs-lookup"><span data-stu-id="b24bc-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="b24bc-108">下載範例</span><span class="sxs-lookup"><span data-stu-id="b24bc-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="b24bc-109">建立範例</span><span class="sxs-lookup"><span data-stu-id="b24bc-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="b24bc-110">執行範例</span><span class="sxs-lookup"><span data-stu-id="b24bc-110">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="b24bc-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="b24bc-111">Requirements</span></span>



| <span data-ttu-id="b24bc-112">產品</span><span class="sxs-lookup"><span data-stu-id="b24bc-112">Product</span></span>                                | <span data-ttu-id="b24bc-113">最小產品版本</span><span class="sxs-lookup"><span data-stu-id="b24bc-113">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="b24bc-114">Windows</span><span class="sxs-lookup"><span data-stu-id="b24bc-114">Windows</span></span>                                | <span data-ttu-id="b24bc-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b24bc-115">Windows Vista</span></span>           |
| <span data-ttu-id="b24bc-116">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="b24bc-116">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="b24bc-117">7.0</span><span class="sxs-lookup"><span data-stu-id="b24bc-117">7.0</span></span>                     |



 

<span data-ttu-id="b24bc-118">如需其他需求，請參閱範例隨附的讀我檔案。</span><span class="sxs-lookup"><span data-stu-id="b24bc-118">For additional requirements, see the Readme file included with the sample.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="b24bc-119">下載範例</span><span class="sxs-lookup"><span data-stu-id="b24bc-119">Downloading the Sample</span></span>

| <span data-ttu-id="b24bc-120">Location</span><span class="sxs-lookup"><span data-stu-id="b24bc-120">Location</span></span>      | <span data-ttu-id="b24bc-121">路徑 URL</span><span class="sxs-lookup"><span data-stu-id="b24bc-121">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b24bc-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="b24bc-122">GitHub</span></span>  | [<span data-ttu-id="b24bc-123">ExecInExplorer 範例</span><span class="sxs-lookup"><span data-stu-id="b24bc-123">ExecInExplorer sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/ExecInExplorer) |

## <a name="building-the-sample"></a><span data-ttu-id="b24bc-124">建立範例</span><span class="sxs-lookup"><span data-stu-id="b24bc-124">Building the Sample</span></span>

<span data-ttu-id="b24bc-125">如需有關如何建立範例的指示，請參閱範例隨附的讀我檔案。</span><span class="sxs-lookup"><span data-stu-id="b24bc-125">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="b24bc-126">執行範例</span><span class="sxs-lookup"><span data-stu-id="b24bc-126">Running the Sample</span></span>

<span data-ttu-id="b24bc-127">如需有關如何建立範例的指示，請參閱範例隨附的讀我檔案。</span><span class="sxs-lookup"><span data-stu-id="b24bc-127">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

 

 



