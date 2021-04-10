---
description: .
ms.assetid: 8c883462-29d8-46c4-b1c6-3ae8b8d3b397
title: 新的 Low-Level 二進位檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6b6e197f22df9fb3d6e12aeeff3c5f4a2a0e41c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194156"
---
# <a name="new-low-level-binaries"></a><span data-ttu-id="a7d28-103">新的 Low-Level 二進位檔</span><span class="sxs-lookup"><span data-stu-id="a7d28-103">New Low-Level Binaries</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="a7d28-104">受影響的平臺</span><span class="sxs-lookup"><span data-stu-id="a7d28-104">Affected Platforms</span></span>

<span data-ttu-id="a7d28-105">**客戶** 端-Windows 7</span><span class="sxs-lookup"><span data-stu-id="a7d28-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="a7d28-106">**伺服器** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a7d28-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="a7d28-107">功能影響</span><span class="sxs-lookup"><span data-stu-id="a7d28-107">Feature Impact</span></span>

<span data-ttu-id="a7d28-108">**嚴重性** -中</span><span class="sxs-lookup"><span data-stu-id="a7d28-108">**Severity** - Medium</span></span>  
<span data-ttu-id="a7d28-109">**頻率** -高</span><span class="sxs-lookup"><span data-stu-id="a7d28-109">**Frequency** - High</span></span>  











## <a name="description"></a><span data-ttu-id="a7d28-110">Description</span><span class="sxs-lookup"><span data-stu-id="a7d28-110">Description</span></span>

<span data-ttu-id="a7d28-111">為了改善內部工程效率並改善未來工作的基礎，我們已將一些功能重新放置到新的低層級二進位檔。</span><span class="sxs-lookup"><span data-stu-id="a7d28-111">To improve internal engineering efficiencies and improve foundations for future work, we have relocated some functionality to new low-level binaries.</span></span> <span data-ttu-id="a7d28-112">這項重整功能可讓您在未來的 Windows 安裝中提供功能子集，以縮減介面區 (磁片和記憶體需求、服務以及受攻擊面) 。</span><span class="sxs-lookup"><span data-stu-id="a7d28-112">This refactoring will make it possible for future installs of Windows to provide subsets of functionality to reduce surface area (disk and memory requirements, servicing, and attack surface).</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="a7d28-113">影響的表現</span><span class="sxs-lookup"><span data-stu-id="a7d28-113">Manifestation of Impact</span></span>

<span data-ttu-id="a7d28-114">作為我們移至低層級二進位檔的功能範例，kernelbase.dll 從 kernel32.dll 和 advapi32.dll 取得功能。</span><span class="sxs-lookup"><span data-stu-id="a7d28-114">As an example of functionality that we moved to low-level binaries, kernelbase.dll gets functionality from kernel32.dll and advapi32.dll.</span></span> <span data-ttu-id="a7d28-115">這表示現有的二進位檔現在會將呼叫向下轉送至新的二進位檔，而不是直接處理它們;轉送可以是靜態 (匯出資料表會顯示重新導向) ， (或 dll 具有可向下呼叫新二進位) 的存根常式。</span><span class="sxs-lookup"><span data-stu-id="a7d28-115">This means that the existing binary now forwards calls down to the new binary rather than handling them directly; the forwarding can be static (the export table shows the redirection), or runtime (the dll has a stub routine that calls down to the new binary).</span></span> <span data-ttu-id="a7d28-116">這會影響低層級的應用程式，例如與內部 Api 和位移相依的安全性和備份應用程式。</span><span class="sxs-lookup"><span data-stu-id="a7d28-116">This will impact low-level applications such as security and backup applications that are dependent upon internal APIs and offsets.</span></span>

## <a name="solution"></a><span data-ttu-id="a7d28-117">解決方法</span><span class="sxs-lookup"><span data-stu-id="a7d28-117">Solution</span></span>

<span data-ttu-id="a7d28-118">唯一的影響是嘗試查看 kernel32.dll 的程式碼，或在記憶體中 advapi32.dll 匯出資料表的程式碼，例如防毒程式可能會執行的動作。</span><span class="sxs-lookup"><span data-stu-id="a7d28-118">The only impact is to code that makes assumptions when attempting to look at the kernel32.dll or the advapi32.dll export table in memory, such as an anti-virus application might do.</span></span> <span data-ttu-id="a7d28-119">使用已發佈的 Api，而不是其執行的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a7d28-119">Use published APIs and not the details of their implementation.</span></span> <span data-ttu-id="a7d28-120">這只是執行 API 的詳細資料的一個範例。</span><span class="sxs-lookup"><span data-stu-id="a7d28-120">This is just one example of implementing around a detail of implementation for an API.</span></span>

 

 



