---
title: Windows Update 上適用的圖形驅動程式可用性
description: 這些驅動程式在 Windows Update (WU) 的可用性將會決定是否要自動提供使用者從 Windows 7、Windows 8 或 Windows 8.1 升級為 Windows 10。
ms.assetid: 166C0FE3-CB9D-4895-91AC-6E57EC1D8B21
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 208e984199c8de63dfa49133a255865035c84bdd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968220"
---
# <a name="availability-of-applicable-graphics-drivers-on-windows-update"></a><span data-ttu-id="b5391-103">Windows Update 上適用的圖形驅動程式可用性</span><span class="sxs-lookup"><span data-stu-id="b5391-103">Availability of applicable graphics drivers on Windows Update</span></span>

<span data-ttu-id="b5391-104">這些驅動程式在 Windows Update (WU) 的可用性將會決定是否要自動提供使用者從 Windows 7、Windows 8 或 Windows 8.1 升級為 Windows 10。</span><span class="sxs-lookup"><span data-stu-id="b5391-104">The availability of these drivers on Windows Update (WU) will determine whether a user is automatically offered an upgrade from Windows 7, Windows 8 or Windows 8.1 to Windows 10.</span></span> <span data-ttu-id="b5391-105">如果硬體掃描顯示電腦上的圖形介面卡 Windows Update 沒有可用的圖形驅動程式，則不會提供使用者更新的 Windows 10 OS。</span><span class="sxs-lookup"><span data-stu-id="b5391-105">If hardware scans showed that there was no graphics driver available on Windows Update for the graphics adapter in the PC, users were not offered the updated Windows 10 OS.</span></span> <span data-ttu-id="b5391-106">不過，使用者仍然可以透過其他來源取得 Windows 10，並手動執行升級。</span><span class="sxs-lookup"><span data-stu-id="b5391-106">However, users can still obtain Windows 10 through other sources and manually perform the upgrade.</span></span>

<span data-ttu-id="b5391-107">有些使用者不確定它們在其他人的情況下未提供升級的原因，即使 Upgrade Advisor 解釋沒有任何圖形驅動程式可供他們的硬體使用也是一樣。</span><span class="sxs-lookup"><span data-stu-id="b5391-107">Some users were unsure of why they were not offered the upgrade when other people were, even though the Upgrade Advisor explained that there was no graphics driver available for their hardware.</span></span>

<span data-ttu-id="b5391-108">此外，某些使用者強制進行升級，然後發現其圖形功能和效能因為缺乏硬體驅動程式而發生。</span><span class="sxs-lookup"><span data-stu-id="b5391-108">Additionally, some users forced an upgrade and then found that their graphics functionality and performance suffered due to the lack of a hardware driver.</span></span>

## <a name="mitigations"></a><span data-ttu-id="b5391-109">風險降低</span><span class="sxs-lookup"><span data-stu-id="b5391-109">Mitigations</span></span>

<span data-ttu-id="b5391-110">若要減輕這個問題，使用者可以手動安裝較舊的驅動程式，也就是從 Windows 7、Windows 8 或 Windows 8.1，方法是前往 IHV 或 OEM 網站，並明確下載驅動程式。</span><span class="sxs-lookup"><span data-stu-id="b5391-110">To mitigate this, users can manually install an older driver, i.e. from Windows 7, Windows 8 or Windows 8.1, by going to the IHV or OEM web site and downloading a driver explicitly.</span></span> <span data-ttu-id="b5391-111">這必須在升級之後完成，而且不保證可以運作。</span><span class="sxs-lookup"><span data-stu-id="b5391-111">This must be done after the upgrade and is not guaranteed to work.</span></span> <span data-ttu-id="b5391-112">如果 WU 無法使用適當的圖形驅動程式，則不支援任何解決方案。</span><span class="sxs-lookup"><span data-stu-id="b5391-112">There is no supported solution if a suitable graphics driver is not available on WU.</span></span> <span data-ttu-id="b5391-113">使用者必須決定是否要：</span><span class="sxs-lookup"><span data-stu-id="b5391-113">The user must decide whether to:</span></span>

-   <span data-ttu-id="b5391-114">保留在先前的作業系統;</span><span class="sxs-lookup"><span data-stu-id="b5391-114">Remain on the previous OS;</span></span>
-   <span data-ttu-id="b5391-115">接受軟體驅動程式的限制，Microsoft 基本顯示器介面卡 (MSBDA) ;或</span><span class="sxs-lookup"><span data-stu-id="b5391-115">Accept the limitations of the software driver, Microsoft Basic Display Adapter (MSBDA); or</span></span>
-   <span data-ttu-id="b5391-116">購買具有支援之 Windows 10 驅動程式的新圖形配接器。</span><span class="sxs-lookup"><span data-stu-id="b5391-116">Buy a new graphics card that has a supported Windows 10 driver.</span></span>

## <a name="solutions"></a><span data-ttu-id="b5391-117">方案</span><span class="sxs-lookup"><span data-stu-id="b5391-117">Solutions</span></span>

<span data-ttu-id="b5391-118">Ihv 和 Oem 將其 Windows 10 graphics 驅動程式上傳至適用于任何想要支援之硬體的 WU 是很重要的。</span><span class="sxs-lookup"><span data-stu-id="b5391-118">It’s critical that IHVs and OEMs upload their Windows 10 graphics drivers to WU for any hardware that they intend to support.</span></span>

<span data-ttu-id="b5391-119">請注意，已到達存留 (EOL) 的硬體在 WU 上可能沒有驅動程式。</span><span class="sxs-lookup"><span data-stu-id="b5391-119">Note that hardware that has reached End-Of-Live (EOL) might not have drivers on WU.</span></span> <span data-ttu-id="b5391-120">在此情況下沒有解決方案-使用者必須選擇上述 [緩和措施] 下的其中一個選項。</span><span class="sxs-lookup"><span data-stu-id="b5391-120">There is no solution in this case – the user must choose one of the options under Mitigations above.</span></span>

 

 




