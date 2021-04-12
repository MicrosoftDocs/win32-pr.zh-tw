---
description: WSFromScript 程式碼範例會示範如何使用 Microsoft ActiveX Data Objects (ADO) ，從 Microsoft Visual Basic 腳本查詢 Windows Search。
ms.assetid: 93ee63f2-ab05-478a-99d0-4f4d09c11506
title: WSFromScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 99f505872571eeea4c16c0edde5059eafd301ac7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318164"
---
# <a name="wsfromscript"></a><span data-ttu-id="b2d2b-103">WSFromScript</span><span class="sxs-lookup"><span data-stu-id="b2d2b-103">WSFromScript</span></span>

<span data-ttu-id="b2d2b-104">WSFromScript 程式碼範例會示範如何使用 Microsoft ActiveX Data Objects (ADO) ，從 Microsoft Visual Basic 腳本查詢 Windows Search。</span><span class="sxs-lookup"><span data-stu-id="b2d2b-104">The WSFromScript code sample demonstrates how to query Windows Search from a Microsoft Visual Basic script using Microsoft ActiveX Data Objects (ADO).</span></span>

<span data-ttu-id="b2d2b-105">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="b2d2b-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="b2d2b-106">需求</span><span class="sxs-lookup"><span data-stu-id="b2d2b-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="b2d2b-107">下載範例</span><span class="sxs-lookup"><span data-stu-id="b2d2b-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="b2d2b-108">建立範例</span><span class="sxs-lookup"><span data-stu-id="b2d2b-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="b2d2b-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="b2d2b-109">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="b2d2b-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2d2b-110">Requirements</span></span>

| <span data-ttu-id="b2d2b-111">產品</span><span class="sxs-lookup"><span data-stu-id="b2d2b-111">Product</span></span>     | <span data-ttu-id="b2d2b-112">產品版本</span><span class="sxs-lookup"><span data-stu-id="b2d2b-112">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="b2d2b-113">Windows</span><span class="sxs-lookup"><span data-stu-id="b2d2b-113">Windows</span></span>     | <span data-ttu-id="b2d2b-114">Windows 7、8.1 或 10</span><span class="sxs-lookup"><span data-stu-id="b2d2b-114">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="b2d2b-115">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="b2d2b-115">Windows SDK</span></span> | <span data-ttu-id="b2d2b-116">7.0 或更高版本</span><span class="sxs-lookup"><span data-stu-id="b2d2b-116">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="b2d2b-117">下載範例</span><span class="sxs-lookup"><span data-stu-id="b2d2b-117">Downloading the Sample</span></span>

<span data-ttu-id="b2d2b-118">下列位置提供此範例。</span><span class="sxs-lookup"><span data-stu-id="b2d2b-118">This sample is available in the following location.</span></span>

| <span data-ttu-id="b2d2b-119">Location</span><span class="sxs-lookup"><span data-stu-id="b2d2b-119">Location</span></span>      | <span data-ttu-id="b2d2b-120">路徑 URL</span><span class="sxs-lookup"><span data-stu-id="b2d2b-120">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="b2d2b-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="b2d2b-121">GitHub</span></span>  | [<span data-ttu-id="b2d2b-122">WSFromScript 範例</span><span class="sxs-lookup"><span data-stu-id="b2d2b-122">WSFromScript sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/WSFromScript)    |

> [!NOTE]  
> <span data-ttu-id="b2d2b-123">針對所有 Windows 版本（包括 Windows 7），建議您直接從 GitHub 下載最新版本的範例。</span><span class="sxs-lookup"><span data-stu-id="b2d2b-123">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="b2d2b-124">建立範例</span><span class="sxs-lookup"><span data-stu-id="b2d2b-124">Building the Sample</span></span>

<span data-ttu-id="b2d2b-125">若要從命令提示字元視窗建立範例：</span><span class="sxs-lookup"><span data-stu-id="b2d2b-125">To build the sample from the Command Prompt window:</span></span>

1. <span data-ttu-id="b2d2b-126">開啟 [命令提示字元] 視窗，並流覽至 **QueryEverything** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="b2d2b-126">Open the Command Prompt window and navigate to the **QueryEverything** project directory.</span></span> <span data-ttu-id="b2d2b-127">例如，Windows 7 SDK 的完整預設安裝路徑為 `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\WindowsSearch\WSFromScript` 。</span><span class="sxs-lookup"><span data-stu-id="b2d2b-127">For example, the full default installation path of the Windows 7 SDK is `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\WindowsSearch\WSFromScript`.</span></span>
2. <span data-ttu-id="b2d2b-128">輸入 `cscript QueryEverything.vbs`。</span><span class="sxs-lookup"><span data-stu-id="b2d2b-128">Enter `cscript QueryEverything.vbs`.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2d2b-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="b2d2b-129">Related topics</span></span>

### <a name="conceptual"></a><span data-ttu-id="b2d2b-130">概念</span><span class="sxs-lookup"><span data-stu-id="b2d2b-130">Conceptual</span></span>

<span data-ttu-id="b2d2b-131">[**VBScript 語言參考**](/previous-versions/d1wf56tt(v=vs.71))</span><span class="sxs-lookup"><span data-stu-id="b2d2b-131">[**VBScript Language Reference**](/previous-versions/d1wf56tt(v=vs.71))</span></span>

### <a name="other-samples"></a><span data-ttu-id="b2d2b-132">其他範例</span><span class="sxs-lookup"><span data-stu-id="b2d2b-132">Other Samples</span></span>

[<span data-ttu-id="b2d2b-133">搜尋程式碼範例</span><span class="sxs-lookup"><span data-stu-id="b2d2b-133">Search Code Samples</span></span>](-search-samples-ovw.md)
