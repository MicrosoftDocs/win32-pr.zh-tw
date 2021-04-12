---
description: Intel AVX 函式。
ms.assetid: 237f356a-9ee8-4c52-b08c-a6695c52713a
title: AVX 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b0b56c83b6beb674bc284b139bb656441956705
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187592"
---
# <a name="avx-functions"></a><span data-ttu-id="f758c-103">AVX 函式</span><span class="sxs-lookup"><span data-stu-id="f758c-103">AVX Functions</span></span>

<span data-ttu-id="f758c-104">以下是 Intel AVX 函數。</span><span class="sxs-lookup"><span data-stu-id="f758c-104">The following are the Intel AVX functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f758c-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="f758c-105">In this section</span></span>



| <span data-ttu-id="f758c-106">主題</span><span class="sxs-lookup"><span data-stu-id="f758c-106">Topic</span></span>                                                                   | <span data-ttu-id="f758c-107">描述</span><span class="sxs-lookup"><span data-stu-id="f758c-107">Description</span></span>                                                                                                                    |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f758c-108">**CopyCoNtext**</span><span class="sxs-lookup"><span data-stu-id="f758c-108">**CopyContext**</span></span>](/windows/desktop/api/WinBase/nf-winbase-copycontext)<br/>                           | <span data-ttu-id="f758c-109">複製來源內容結構 (包括任何 XState) 至初始化的目的地內容結構。</span><span class="sxs-lookup"><span data-stu-id="f758c-109">Copies a source context structure (including any XState) onto an initialized destination context structure.</span></span><br/>         |
| [<span data-ttu-id="f758c-110">**GetEnabledXStateFeatures**</span><span class="sxs-lookup"><span data-stu-id="f758c-110">**GetEnabledXStateFeatures**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getenabledxstatefeatures)<br/> | <span data-ttu-id="f758c-111">取得 x86 或 x64 處理器上已啟用 XState 功能的遮罩。</span><span class="sxs-lookup"><span data-stu-id="f758c-111">Gets a mask of enabled XState features on x86 or x64 processors.</span></span><br/>                                                    |
| [<span data-ttu-id="f758c-112">**GetXStateFeaturesMask**</span><span class="sxs-lookup"><span data-stu-id="f758c-112">**GetXStateFeaturesMask**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getxstatefeaturesmask)<br/>       | <span data-ttu-id="f758c-113">傳回在 [**內容**](/windows/desktop/api/WinNT/ns-winnt-wow64_context) 結構中設定的 XState 功能遮罩。</span><span class="sxs-lookup"><span data-stu-id="f758c-113">Returns the mask of XState features set within a [**CONTEXT**](/windows/desktop/api/WinNT/ns-winnt-wow64_context) structure.</span></span><br/>                        |
| [<span data-ttu-id="f758c-114">**InitializeCoNtext**</span><span class="sxs-lookup"><span data-stu-id="f758c-114">**InitializeContext**</span></span>](/windows/desktop/api/WinBase/nf-winbase-initializecontext)<br/>               | <span data-ttu-id="f758c-115">使用必要的大小和對齊方式，初始化緩衝區內的 [**內容**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) 結構。</span><span class="sxs-lookup"><span data-stu-id="f758c-115">Initializes a [**CONTEXT**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) structure inside a buffer with the necessary size and alignment.</span></span><br/>       |
| [<span data-ttu-id="f758c-116">**LocateXStateFeature**</span><span class="sxs-lookup"><span data-stu-id="f758c-116">**LocateXStateFeature**</span></span>](/windows/desktop/api/WinBase/nf-winbase-locatexstatefeature)<br/>           | <span data-ttu-id="f758c-117">抓取 [**內容**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) 結構內 XState 功能的處理器狀態指標。</span><span class="sxs-lookup"><span data-stu-id="f758c-117">Retrieves a pointer to the processor state for an XState feature within a [**CONTEXT**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) structure.</span></span><br/> |
| [<span data-ttu-id="f758c-118">**SetXStateFeaturesMask**</span><span class="sxs-lookup"><span data-stu-id="f758c-118">**SetXStateFeaturesMask**</span></span>](/windows/desktop/api/WinBase/nf-winbase-setxstatefeaturesmask)<br/>       | <span data-ttu-id="f758c-119">設定在 [**內容**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) 結構中設定的 XState 功能遮罩。</span><span class="sxs-lookup"><span data-stu-id="f758c-119">Sets the mask of XState features set within a [**CONTEXT**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) structure.</span></span><br/>                             |



 

 

 




