---
description: 現在是在 Server Core 上的 .NET 2.0 子集
ms.assetid: f91c4604-b2d6-41e5-be66-bbc8a4f0e28e
title: 現在是在 Server Core 上的 .NET 2.0 子集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b6ef839f525acf190df384e3fe8394f2b785d45
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116146"
---
# <a name="subset-of-net-20-now-on-server-core"></a><span data-ttu-id="4bd8d-103">現在是在 Server Core 上的 .NET 2.0 子集</span><span class="sxs-lookup"><span data-stu-id="4bd8d-103">Subset of .NET 2.0 Now on Server Core</span></span>

## <a name="platform"></a><span data-ttu-id="4bd8d-104">平台</span><span class="sxs-lookup"><span data-stu-id="4bd8d-104">Platform</span></span>

<span data-ttu-id="4bd8d-105">**伺服器** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4bd8d-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="4bd8d-106">功能影響</span><span class="sxs-lookup"><span data-stu-id="4bd8d-106">Feature Impact</span></span>

 <span data-ttu-id="4bd8d-107">**嚴重性** -低</span><span class="sxs-lookup"><span data-stu-id="4bd8d-107">**Severity** - Low</span></span>  
<span data-ttu-id="4bd8d-108">**頻率** -低</span><span class="sxs-lookup"><span data-stu-id="4bd8d-108">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="4bd8d-109">Description</span><span class="sxs-lookup"><span data-stu-id="4bd8d-109">Description</span></span>

<span data-ttu-id="4bd8d-110">Windows Server 2008 R2 的 Server Core 安裝選項現在包含 .NET Framework 2.0 的子集。</span><span class="sxs-lookup"><span data-stu-id="4bd8d-110">The Server Core installation option for Windows Server 2008 R2 now includes a subset of the .NET Framework 2.0.</span></span> <span data-ttu-id="4bd8d-111">子集是 .NET 2.0 中與 Server Core 中的功能相符的功能;未將任何二進位檔新增至 Server Core 基底，以允許 .NET 2.0 的任何部分正常運作。</span><span class="sxs-lookup"><span data-stu-id="4bd8d-111">The subset is the functionality in .NET 2.0 that aligns with the functionality in Server Core; no binaries were added to the Server Core base to allow any portion of .NET 2.0 to function.</span></span>

<span data-ttu-id="4bd8d-112">Windows Server 2008 的 Server Core 安裝選項中沒有 .NET 支援。</span><span class="sxs-lookup"><span data-stu-id="4bd8d-112">There was no .NET support in the Server Core installation option for Windows Server 2008.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="4bd8d-113">影響的表現</span><span class="sxs-lookup"><span data-stu-id="4bd8d-113">Manifestation of Impact</span></span>

<span data-ttu-id="4bd8d-114">這可讓某些以 .NET 2.0 為基礎的應用程式在 Windows Server 2008 R2 的 Server Core 上執行。</span><span class="sxs-lookup"><span data-stu-id="4bd8d-114">This allows some .NET 2.0 based-applications to run on Server Core in Windows Server 2008 R2.</span></span>

## <a name="testing"></a><span data-ttu-id="4bd8d-115">測試</span><span class="sxs-lookup"><span data-stu-id="4bd8d-115">Testing</span></span>

<span data-ttu-id="4bd8d-116">確認您的程式碼所使用的 .NET 類別包含在 Server Core 中。</span><span class="sxs-lookup"><span data-stu-id="4bd8d-116">Verify that the .NET classes your code uses is included in Server Core.</span></span> <span data-ttu-id="4bd8d-117">也請測試在 Server Core 上執行此程式碼的任何應用程式。</span><span class="sxs-lookup"><span data-stu-id="4bd8d-117">Also test any applications that run this code on Server Core.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="4bd8d-118">其他資源的連結</span><span class="sxs-lookup"><span data-stu-id="4bd8d-118">Links to Other Resources</span></span>

-   <span data-ttu-id="4bd8d-119">[Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4bd8d-119">[Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))</span></span>
-   [<span data-ttu-id="4bd8d-120">Server Core Blog</span><span class="sxs-lookup"><span data-stu-id="4bd8d-120">Server Core Blog</span></span>](https://blogs.technet.com/server_core/archive/2008/11/25/net-2-0-and-server-core-in-windows-server-2008-r2.aspx)
-   <span data-ttu-id="4bd8d-121">另 *請參閱* *Windows SERVER 2008 R2 SDK* 的伺服器核心區段（當它變成可用時）</span><span class="sxs-lookup"><span data-stu-id="4bd8d-121">*See also* the Server Core section of the *Windows Server 2008 R2 SDK* when it becomes available</span></span>

> [!Note]  
> <span data-ttu-id="4bd8d-122">這些資源可能無法在某些語言及國家/地區中使用。</span><span class="sxs-lookup"><span data-stu-id="4bd8d-122">These resources may not be available in some languages and countries/regions.</span></span>

 

 

 
