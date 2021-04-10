---
title: Windows 硬體認證套件
description: Windows 硬體認證套件
ms.assetid: 99BD2D7D-8F9D-445E-AE04-6A58FFF3DCE6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dba820d62d6766f74549ed23f7a5abdccbca258b
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "104024223"
---
# <a name="windows-hardware-certification-kit"></a><span data-ttu-id="3f26c-103">Windows 硬體認證套件</span><span class="sxs-lookup"><span data-stu-id="3f26c-103">Windows Hardware Certification Kit</span></span>

## <a name="platforms"></a><span data-ttu-id="3f26c-104">平台</span><span class="sxs-lookup"><span data-stu-id="3f26c-104">Platforms</span></span>

 <span data-ttu-id="3f26c-105">**客戶** 端-Windows 7 \| Windows 8</span><span class="sxs-lookup"><span data-stu-id="3f26c-105">**Clients** - Windows 7 \| Windows 8</span></span>  
<span data-ttu-id="3f26c-106">**伺服器** -windows Server 2008 R2 \| windows server 2012</span><span class="sxs-lookup"><span data-stu-id="3f26c-106">**Servers** - Windows Server 2008 R2 \| Windows Server 2012</span></span>  
<span data-ttu-id="3f26c-107">**伺服器/控制器** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3f26c-107">**Server/Controller** - Windows Server 2008 R2</span></span>  


## <a name="description"></a><span data-ttu-id="3f26c-108">Description</span><span class="sxs-lookup"><span data-stu-id="3f26c-108">Description</span></span>

<span data-ttu-id="3f26c-109">Windows 硬體認證套件可讓開發人員、Isv、Ihv 和 Oem 針對最新的 Windows 作業系統認證其硬體裝置、系統和篩選器驅動程式。</span><span class="sxs-lookup"><span data-stu-id="3f26c-109">The Windows Hardware Certification Kit enables developers, ISVs, IHVs, and OEMs to certify their hardware devices, systems, and filter drivers for the latest Windows operating systems.</span></span> <span data-ttu-id="3f26c-110">其中包含認證硬體和篩選這些作業系統所需的所有工具和檔：</span><span class="sxs-lookup"><span data-stu-id="3f26c-110">It contains all the tools and documentation that you need to certify your hardware and filter drivers for these operating systems:</span></span>

-   <span data-ttu-id="3f26c-111">Windows 8</span><span class="sxs-lookup"><span data-stu-id="3f26c-111">Windows 8</span></span>
-   <span data-ttu-id="3f26c-112">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3f26c-112">Windows Server 2012</span></span>
-   <span data-ttu-id="3f26c-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3f26c-113">Windows 7</span></span>
-   <span data-ttu-id="3f26c-114">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3f26c-114">Windows Server 2008 R2</span></span>

<span data-ttu-id="3f26c-115">Windows 硬體認證套件取代了 Windows 標誌套件，而且是 Windows 認證程式的一部分。</span><span class="sxs-lookup"><span data-stu-id="3f26c-115">The Windows Hardware Certification Kit replaces the Windows Logo Kit and is a part of the Windows Certification Program.</span></span>

## <a name="usage-or-best-practices"></a><span data-ttu-id="3f26c-116">使用方式或最佳做法</span><span class="sxs-lookup"><span data-stu-id="3f26c-116">Usage or best practices</span></span>

<span data-ttu-id="3f26c-117">在測試任何硬體或篩選器驅動程式之前，您必須根據您所認證的硬體或篩選器驅動程式來設定適當的測試環境。</span><span class="sxs-lookup"><span data-stu-id="3f26c-117">Before you can test any hardware or filter driver, you must set up the proper test environment based on the hardware or filter driver you are certifying.</span></span> <span data-ttu-id="3f26c-118">這包括控制器、用戶端，以及可能的額外硬體 (例如多功能裝置) 或軟體。</span><span class="sxs-lookup"><span data-stu-id="3f26c-118">This includes the controller, client, and potentially additional hardware (for example, multi-function devices) or software.</span></span> <span data-ttu-id="3f26c-119">設定環境之後，您可以使用新的 HCK Studio 工具來測試您的硬體。</span><span class="sxs-lookup"><span data-stu-id="3f26c-119">After your environment is set up, you can test your hardware using the new HCK’s Studio tool.</span></span> <span data-ttu-id="3f26c-120">這些步驟概述認證測試程式。</span><span class="sxs-lookup"><span data-stu-id="3f26c-120">These steps outline the certification test process.</span></span>

1.  <span data-ttu-id="3f26c-121">設定測試環境。</span><span class="sxs-lookup"><span data-stu-id="3f26c-121">Set up test environment.</span></span>
2.  <span data-ttu-id="3f26c-122">建立專案。</span><span class="sxs-lookup"><span data-stu-id="3f26c-122">Create a project.</span></span>
3.  <span data-ttu-id="3f26c-123">建立一或多個電腦集區。</span><span class="sxs-lookup"><span data-stu-id="3f26c-123">Create one or more machine pools.</span></span>
4.  <span data-ttu-id="3f26c-124">選取要驗證的功能。</span><span class="sxs-lookup"><span data-stu-id="3f26c-124">Select features to validate.</span></span>
5.  <span data-ttu-id="3f26c-125">針對這些功能選取並執行測試。</span><span class="sxs-lookup"><span data-stu-id="3f26c-125">Select and run tests against those features.</span></span>
6.  <span data-ttu-id="3f26c-126">查看測試結果。</span><span class="sxs-lookup"><span data-stu-id="3f26c-126">View test results.</span></span>
7.  <span data-ttu-id="3f26c-127">提交您的套件。</span><span class="sxs-lookup"><span data-stu-id="3f26c-127">Submit your package.</span></span>

## <a name="resources"></a><span data-ttu-id="3f26c-128">資源</span><span class="sxs-lookup"><span data-stu-id="3f26c-128">Resources</span></span>

-   [<span data-ttu-id="3f26c-129">Windows 硬體開發</span><span class="sxs-lookup"><span data-stu-id="3f26c-129">Windows Hardware Development</span></span>](https://msdn.microsoft.com/windows/hardware/)
-   <span data-ttu-id="3f26c-130">[Windows 硬體認證計畫](/previous-versions/windows/hardware/hck/jj124227(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3f26c-130">[Windows Hardware Certification Program](/previous-versions/windows/hardware/hck/jj124227(v=vs.85))</span></span>
-   <span data-ttu-id="3f26c-131">[開始開發 Windows 的硬體](/previous-versions/gg507680(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="3f26c-131">[Start Developing Hardware for Windows](/previous-versions/gg507680(v=msdn.10))</span></span>

 

 