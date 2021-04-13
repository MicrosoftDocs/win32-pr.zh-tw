---
title: 自 Windows 7 起的重要變更，以確保相容性
description: 自 Windows 7 起的重要變更，以確保相容性
ms.assetid: 6930AA8C-B9AE-44C0-BC7F-12342DBBEB5E
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9ee24b18be55ff498d6c3870f77a32270df68284
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301687"
---
# <a name="key-changes-since-windows-7-to-ensure-compatibility"></a><span data-ttu-id="c32b9-103">自 Windows 7 起的重要變更，以確保相容性</span><span class="sxs-lookup"><span data-stu-id="c32b9-103">Key changes since Windows 7 to ensure compatibility</span></span>

<span data-ttu-id="c32b9-104">我們了解對於開發人員來說，相容性非常重要。</span><span class="sxs-lookup"><span data-stu-id="c32b9-104">We understand that compatibility matters to developers.</span></span> <span data-ttu-id="c32b9-105">ISV 與開發人員希望確保他們的 app 可在所有支援的 Windows 作業系統版本上如預期般運作。</span><span class="sxs-lookup"><span data-stu-id="c32b9-105">ISVs and developers want to ensure their apps will run as expected on all supported versions of the Windows OS.</span></span> <span data-ttu-id="c32b9-106">消費者與企業的主要投資在這裡—他們希望確保他們付費使用的 app 可以持續運作。</span><span class="sxs-lookup"><span data-stu-id="c32b9-106">Consumers and businesses have a key investment here—they want to ensure that the apps they have paid for will continue to work.</span></span> <span data-ttu-id="c32b9-107">我們了解相容性是採購決策的主要條件。</span><span class="sxs-lookup"><span data-stu-id="c32b9-107">We know that compatibility is the primary criteria for purchase decisions.</span></span> <span data-ttu-id="c32b9-108">以最佳作法撰寫的應用程式，在發行新的 Windows 版本時，會導致程式碼變換變得更少，而且會降低分散程度—這些應用程式具有較少的工程投資來維護，並且加快上市時間。</span><span class="sxs-lookup"><span data-stu-id="c32b9-108">Apps that are well written based on best practices will lead to much less code churn when a new Windows version is released, and will reduce fragmentation—these apps have a reduced engineering investment to maintain, and a faster time to market.</span></span>

<span data-ttu-id="c32b9-109">在 Windows 7 時期，是以非常被動的方式處理相容性問題。</span><span class="sxs-lookup"><span data-stu-id="c32b9-109">In the Windows 7 timeframe, compatibility was very much a reactive approach.</span></span> <span data-ttu-id="c32b9-110">在 Windows 8 中，我們開始以不同的觀點，在 Windows 內盡力確保在設計時便將相容性納入考量，而非在事後補救。</span><span class="sxs-lookup"><span data-stu-id="c32b9-110">In Windows 8, we started looking at this differently, working within Windows to ensure that compatibility was by design rather than an afterthought.</span></span> <span data-ttu-id="c32b9-111">Windows 10 是到目前為止最符合「透過設計提供相容性」的 OS 版本。</span><span class="sxs-lookup"><span data-stu-id="c32b9-111">Windows 10 is the most compatible-by-design version of the OS to date.</span></span> <span data-ttu-id="c32b9-112">以下是我們達成這項目標的主要方法：</span><span class="sxs-lookup"><span data-stu-id="c32b9-112">Here are some key ways we accomplished this:</span></span>

-   <span data-ttu-id="c32b9-113">應用程式遙測：這可協助我們瞭解 Windows 生態系統中的應用程式熱門程度，以通知相容性測試。</span><span class="sxs-lookup"><span data-stu-id="c32b9-113">App telemetry: this helps us understand app popularity in the Windows ecosystem to inform compatibility testing.</span></span>
-   <span data-ttu-id="c32b9-114">ISV 合作關係：直接與外部合作夥伴合作，為他們提供資料並協助修正使用者體驗的問題。</span><span class="sxs-lookup"><span data-stu-id="c32b9-114">ISV partnerships: work directly with external partners to provide them with data and help fix issues that our users experience.</span></span>
-   <span data-ttu-id="c32b9-115">設計評論，上游偵測：與功能小組合作，減少 Windows 中的重大變更數目。</span><span class="sxs-lookup"><span data-stu-id="c32b9-115">Design reviews, upstream detection: partner with feature teams to reduce the number of breaking changes in Windows.</span></span> <span data-ttu-id="c32b9-116">相容性檢閱是功能小組必須通過的門檻。</span><span class="sxs-lookup"><span data-stu-id="c32b9-116">Compatibility review is a gate that our feature teams must pass.</span></span>
-   <span data-ttu-id="c32b9-117">更嚴密地控制 API 變更 & 改良的通訊</span><span class="sxs-lookup"><span data-stu-id="c32b9-117">Tighter control over API changes & improved communication</span></span>
-   <span data-ttu-id="c32b9-118">試驗和意見反應迴圈： Windows 測試人員人口會收到 flighted 組建，以協助改善在將最終組建發行給客戶之前，尋找相容性問題的能力。</span><span class="sxs-lookup"><span data-stu-id="c32b9-118">Flighting and feedback loop: The Windows Insider population receives flighted builds that help improve our ability to find compatibility issues before a final build is released to customers.</span></span> <span data-ttu-id="c32b9-119">這個意見反應程序不僅能揭露錯誤，也確保我們推出的是使用者想要的功能。</span><span class="sxs-lookup"><span data-stu-id="c32b9-119">This feedback process not only exposes bugs, but ensures we are shipping features our users want.</span></span>

 

 




