---
title: 專屬線上商店
description: 專屬線上商店
ms.assetid: f2b7f9a7-2299-48f4-b915-2c1a5e0d68bb
keywords:
- Windows Media Player 線上商店，獨家
- 線上商店，獨家
- 輸入1個線上商店，專屬
- 輸入2個線上商店，專屬
- 專屬線上商店
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f408a0ada0de46d637537ffccd3ec162da04e8ce
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106965005"
---
# <a name="exclusive-online-stores"></a><span data-ttu-id="11223-108">專屬線上商店</span><span class="sxs-lookup"><span data-stu-id="11223-108">Exclusive Online Stores</span></span>

<span data-ttu-id="11223-109">在 Windows Media Player 11 中，從遠端內嵌播放機控制項的應用程式可以指定專屬的線上商店。</span><span class="sxs-lookup"><span data-stu-id="11223-109">With Windows Media Player 11, an application that embeds the Player control remotely can specify an exclusive online store.</span></span> <span data-ttu-id="11223-110">在此情況下，會停用 Windows Media Player 中的服務選取器，而且只有指定的線上存放區可供使用者使用。</span><span class="sxs-lookup"><span data-stu-id="11223-110">In that case, the service selector in Windows Media Player is disabled, and only the specified online store is available to the user.</span></span> <span data-ttu-id="11223-111">此外，Windows Media Player 會採用專屬線上商店 ServiceInfo 檔的 **color** 元素所指定的色彩。</span><span class="sxs-lookup"><span data-stu-id="11223-111">Also, Windows Media Player adopts the color specified by the **Color** element of the exclusive online store's ServiceInfo document.</span></span>

<span data-ttu-id="11223-112">若要指定專屬的線上商店，應用程式必須將 ExclusiveService：*keyname* 附加至它從 [IWMPRemoteMediaServices：： GetServiceType](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getservicetype)傳回的字串結尾。</span><span class="sxs-lookup"><span data-stu-id="11223-112">To specify an exclusive online store, an application must append ExclusiveService:*keyname* to the end of the string that it returns from [IWMPRemoteMediaServices::GetServiceType](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getservicetype).</span></span> <span data-ttu-id="11223-113">例如，假設 Proseware 是指定給特定線上商店的索引鍵名稱。</span><span class="sxs-lookup"><span data-stu-id="11223-113">For example, suppose Proseware is the key name given to a particular online store.</span></span> <span data-ttu-id="11223-114">如果 **GetServiceType** 傳回 "Remote ExclusiveService： Proseware" 字串，則 Proseware 將是遠端內嵌播放機控制項中唯一可用的線上商店。</span><span class="sxs-lookup"><span data-stu-id="11223-114">If **GetServiceType** returns the string "Remote ExclusiveService:Proseware", then Proseware will be the only online store available in the remotely embedded Player control.</span></span>

<span data-ttu-id="11223-115">只有當應用程式啟動時，如果 Windows Media Player 尚未執行，應用程式才可以將 Windows Media Player 限制為專屬的線上商店。</span><span class="sxs-lookup"><span data-stu-id="11223-115">An application can limit Windows Media Player to an exclusive online store only if Windows Media Player is not already running when the application is launched.</span></span> <span data-ttu-id="11223-116">應用程式的責任是在執行應用程式之前，通知使用者必須關閉 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="11223-116">It is the application's responsibility to inform the user that he or she must close Windows Media Player before running the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="11223-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="11223-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11223-118">**Type 1 和 Type 2 線上商店的一般資訊**</span><span class="sxs-lookup"><span data-stu-id="11223-118">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="11223-119">**遠端處理 Windows Media Player 控制項**</span><span class="sxs-lookup"><span data-stu-id="11223-119">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




