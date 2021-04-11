---
title: DWM 總覽
description: DWM 總覽
ms.assetid: 32ff4ab3-e02e-4e6a-8833-2537eb3f65c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9622023856005700f576970238a3444a0589c71d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021925"
---
# <a name="dwm-overviews"></a><span data-ttu-id="05478-103">DWM 總覽</span><span class="sxs-lookup"><span data-stu-id="05478-103">DWM Overviews</span></span>

## <a name="in-this-section"></a><span data-ttu-id="05478-104">本節內容</span><span class="sxs-lookup"><span data-stu-id="05478-104">In this section</span></span>



| <span data-ttu-id="05478-105">主題</span><span class="sxs-lookup"><span data-stu-id="05478-105">Topic</span></span>                                                                             | <span data-ttu-id="05478-106">描述</span><span class="sxs-lookup"><span data-stu-id="05478-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="05478-107">Enable and Control DWM Composition (啟用並控制 DWM 組合)</span><span class="sxs-lookup"><span data-stu-id="05478-107">Enable and Control DWM Composition</span></span>](composition-ovw.md)<br/>              | <span data-ttu-id="05478-108">桌面視窗管理員 (DWM) 撰寫 Api 提供數個函式，可用來設定及查詢 DWM 所使用的基本資訊。</span><span class="sxs-lookup"><span data-stu-id="05478-108">The Desktop Window Manager (DWM) composition APIs provides several functions for setting and querying for basic information that is used by the DWM.</span></span> <span data-ttu-id="05478-109">這些 Api 可讓您查詢及變更撰寫狀態。</span><span class="sxs-lookup"><span data-stu-id="05478-109">These APIs enable you to query and change the composition state.</span></span> <span data-ttu-id="05478-110">此外，您可以針對不同的 DWM 視窗屬性，設定和查詢轉譯原則。</span><span class="sxs-lookup"><span data-stu-id="05478-110">Additionally, you can set and query the rendering policy for different DWM window attributes.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="05478-111">DWM 模糊背後總覽</span><span class="sxs-lookup"><span data-stu-id="05478-111">DWM Blur Behind Overview</span></span>](blur-ovw.md)<br/>                               | <span data-ttu-id="05478-112">其中一個特徵 DWM 效果是半透明且模糊的非工作區。</span><span class="sxs-lookup"><span data-stu-id="05478-112">One of the signature DWM effects is a translucent and blurred non-client area.</span></span> <span data-ttu-id="05478-113">DWM Api 可讓應用程式將這些效果套用到其最上層視窗的工作區。</span><span class="sxs-lookup"><span data-stu-id="05478-113">The DWM APIs enable applications to apply these effects to the client area of their top-level windows.</span></span><br/>                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="05478-114">DWM 縮圖總覽</span><span class="sxs-lookup"><span data-stu-id="05478-114">DWM Thumbnail Overview</span></span>](thumbnail-ovw.md)<br/>                            | <span data-ttu-id="05478-115">DWM 可顯示應用程式視窗的縮圖標記法。</span><span class="sxs-lookup"><span data-stu-id="05478-115">DWM enables the display of thumbnail representations of application windows.</span></span> <span data-ttu-id="05478-116">這些不是視窗的靜態快照集，而是縮圖來源視窗與接收即時縮圖轉譯之目的地視窗上的位置之間的動態、固定連接。</span><span class="sxs-lookup"><span data-stu-id="05478-116">These are not static snapshots of a window, but are instead dynamic, constant connections between a thumbnail source window and a location on a destination window that receives the live thumbnail rendering.</span></span> <span data-ttu-id="05478-117">這可讓您快速查看執行中的應用程式，方法是將滑鼠停留在工作列上的應用程式上，或使用 ALT 鍵的按鍵手勢來查看並快速切換至應用程式。</span><span class="sxs-lookup"><span data-stu-id="05478-117">This allows a quick view of running applications by hovering over the application on the taskbar or using the ALT-TAB key gesture to see and quickly switch to an application.</span></span><br/> |
| [<span data-ttu-id="05478-118">存取及控制 DWM 框架資料</span><span class="sxs-lookup"><span data-stu-id="05478-118">Accessing and Controlling DWM Frame Data</span></span>](frametiming-ovw.md)<br/>        | <span data-ttu-id="05478-119">本主題討論用於排程和媒體簡報的 DWM Api。</span><span class="sxs-lookup"><span data-stu-id="05478-119">This topic discusses the DWM APIs that are used for scheduling and media presentation.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="05478-120">效能考慮和最佳作法</span><span class="sxs-lookup"><span data-stu-id="05478-120">Performance Considerations and Best Practices</span></span>](bestpractices-ovw.md)<br/> | <span data-ttu-id="05478-121">本主題提供一組使用 DWM Api 的最佳做法。</span><span class="sxs-lookup"><span data-stu-id="05478-121">This topic presents a set of best practices for using the DWM APIs.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="05478-122">使用 DWM 的自訂視窗框架</span><span class="sxs-lookup"><span data-stu-id="05478-122">Custom Window Frame Using DWM</span></span>](customframe.md)<br/>                       | <span data-ttu-id="05478-123">本主題將示範如何使用 DWM Api 來為您的應用程式建立自訂視窗框架。</span><span class="sxs-lookup"><span data-stu-id="05478-123">This topic demonstrates how to use the DWM APIs to create custom window frames for your application.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                       |



 

 

 





