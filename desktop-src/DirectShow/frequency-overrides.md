---
description: 頻率覆寫
ms.assetid: 0e45d0a6-3c3e-462c-a8dc-c4f25b614b85
title: 頻率覆寫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57177e4990cb40be271fc551718964faf1696d2d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509826"
---
# <a name="frequency-overrides"></a><span data-ttu-id="c3467-103">頻率覆寫</span><span class="sxs-lookup"><span data-stu-id="c3467-103">Frequency Overrides</span></span>

<span data-ttu-id="c3467-104">花費大量的精力來確保每個國家/地區的廣播頻率和色彩標準指派都是正確的。</span><span class="sxs-lookup"><span data-stu-id="c3467-104">A significant amount of effort was spent to ensure that the broadcast frequencies and color standard assignments are correct for each country/region.</span></span> <span data-ttu-id="c3467-105">儘管如此，在某些情況下，頻率資料表還不夠、包含錯誤或淘汰。</span><span class="sxs-lookup"><span data-stu-id="c3467-105">Even so, there will be situations when the frequency tables are not sufficient, contain errors, or become obsolete.</span></span> <span data-ttu-id="c3467-106">若要解決這個問題，可以使用下列登錄機碼，選擇性地覆寫 TV 調諧器篩選準則的頻率資料表中所列的頻率：</span><span class="sxs-lookup"><span data-stu-id="c3467-106">To address this problem, the frequencies listed in the TV Tuner filter's frequency tables may be selectively overridden, by using the following registry key:</span></span>

<span data-ttu-id="c3467-107">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **電視 System Services** \\ **TVAutoTune** \\ **TS0-1**</span><span class="sxs-lookup"><span data-stu-id="c3467-107">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**TV System Services**\\**TVAutoTune**\\**TS0-1**</span></span>

> [!Note]  
> <span data-ttu-id="c3467-108">從 Windows 7 開始，在 x64 版本的 Windows 上執行的 x86 應用程式會使用下列重新導向的登錄機碼：</span><span class="sxs-lookup"><span data-stu-id="c3467-108">Starting in Windows 7, the following redirected registry key is used for x86 applications running on x64 versions of Windows:</span></span>

 

<span data-ttu-id="c3467-109">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Wow6432Node** \\ **Microsoft** \\ **電視 System Services** \\ **TVAutoTune** \\ **TS0-1**</span><span class="sxs-lookup"><span data-stu-id="c3467-109">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Wow6432Node**\\**Microsoft**\\**TV System Services**\\**TVAutoTune**\\**TS0-1**</span></span>

<span data-ttu-id="c3467-110">頻率覆寫會分組為應用程式定義的「微調空間」，並以數位來識別。</span><span class="sxs-lookup"><span data-stu-id="c3467-110">Frequency overrides are grouped into application-defined "tuning spaces," which are identified by number.</span></span> <span data-ttu-id="c3467-111">下列範例顯示範例覆寫：</span><span class="sxs-lookup"><span data-stu-id="c3467-111">The following example shows an example override:</span></span>

``` syntax
HKEY_LOCAL_MACHINE\Software\Microsoft\TV System Services\TVAutoTune\TS0-1
"12"=dword:04022750
```

<span data-ttu-id="c3467-112">在此情況下，「TS0-1」表示微調空間的空間為0。</span><span class="sxs-lookup"><span data-stu-id="c3467-112">In this case, "TS0-1" indicates Tuning Space 0 for cable frequencies.</span></span> <span data-ttu-id="c3467-113">第一個數位會識別微調空間。</span><span class="sxs-lookup"><span data-stu-id="c3467-113">The first number identifies the tuning space.</span></span> <span data-ttu-id="c3467-114">第二個數字是針對廣播頻率為0，而針對纜線頻率為1。</span><span class="sxs-lookup"><span data-stu-id="c3467-114">The second number is either 0 for broadcast frequencies or 1 for cable frequencies.</span></span>

<span data-ttu-id="c3467-115">名為 "12" 的子機碼會覆寫目前頻率資料表中索引12的頻率值。</span><span class="sxs-lookup"><span data-stu-id="c3467-115">The subkey named "12" overrides the frequency value for the frequency at index 12 in the current frequency table.</span></span> <span data-ttu-id="c3467-116">子機碼的值是一個 **DWORD** ，可指定以赫茲 (Hz) 的頻率。</span><span class="sxs-lookup"><span data-stu-id="c3467-116">The value of the subkey is a **DWORD** that specifies the frequency in Hertz (Hz).</span></span> <span data-ttu-id="c3467-117">在此範例中，頻率設為 67.25 MHz。</span><span class="sxs-lookup"><span data-stu-id="c3467-117">In this example, the frequency is set to 67.25 MHz.</span></span> <span data-ttu-id="c3467-118">您可以針對範圍介於1到999（含）的任何通道編號定義覆寫。</span><span class="sxs-lookup"><span data-stu-id="c3467-118">Overrides can be defined for any channel numbers in the range of 1 to 999, inclusive.</span></span> <span data-ttu-id="c3467-119">如果微調硬體不支援指定的頻率，微調要求將會失敗。</span><span class="sxs-lookup"><span data-stu-id="c3467-119">If the tuning hardware does not support a given frequency, the tune request will fail.</span></span>

<span data-ttu-id="c3467-120">這項機制也可以用來在 frequency 資料表中的現有範圍之外建立新的通道號碼。</span><span class="sxs-lookup"><span data-stu-id="c3467-120">This mechanism can also be used to create new channel numbers outside the existing range in the frequency table.</span></span> <span data-ttu-id="c3467-121">[**IAMTuner：： ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax)方法會傳回擴充的通道範圍。</span><span class="sxs-lookup"><span data-stu-id="c3467-121">The [**IAMTuner::ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) method will return the extended channel range.</span></span> <span data-ttu-id="c3467-122">例如，如果原始通道範圍是1到158，而將 "200" 的通道覆寫新增至登錄，則 **ChannelMinMax** 方法會傳回200作為最大通道。</span><span class="sxs-lookup"><span data-stu-id="c3467-122">For example, if the original channel range was 1 to 158, and a channel override of "200" is added to the registry, the **ChannelMinMax** method will return 200 as the maximum channel.</span></span> <span data-ttu-id="c3467-123">在此情況下，159到199範圍中的通道編號不會指派任何頻率，因此該範圍內的任何微調要求都會自動失敗。</span><span class="sxs-lookup"><span data-stu-id="c3467-123">In this case, channel numbers in the range of 159 to 199 will have no frequencies assigned to them, so any tuning requests in that range will automatically fail.</span></span>

<span data-ttu-id="c3467-124">[**IAMTuner：:p \_ TuningSpace**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace)方法可讓應用程式選擇要使用的一組覆寫和微調資訊。</span><span class="sxs-lookup"><span data-stu-id="c3467-124">The [**IAMTuner::put\_TuningSpace**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace) method allows the application to choose which set of overrides and fine-tuning information to use.</span></span> <span data-ttu-id="c3467-125">微調空間數目是任意的。</span><span class="sxs-lookup"><span data-stu-id="c3467-125">Tuning space numbers are arbitrary.</span></span> <span data-ttu-id="c3467-126">應用程式必須負責維護微調空間與頻率資料表之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="c3467-126">It is the application's responsibility to maintain the relationship between the tuning space and the frequency table.</span></span> <span data-ttu-id="c3467-127">最直接的方法是使用國家/地區碼作為微調空間號碼。</span><span class="sxs-lookup"><span data-stu-id="c3467-127">The most straightforward approach is to use the country/region code as the tuning space number.</span></span> <span data-ttu-id="c3467-128">然後，每次應用程式切換至新的國家/地區代碼時，也會切換至相同的微調空間 (順序) 。</span><span class="sxs-lookup"><span data-stu-id="c3467-128">Then, every time the application switches to a new country/region code, it also switches to the same tuning space (in that order).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c3467-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="c3467-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3467-130">國際類比電視微調</span><span class="sxs-lookup"><span data-stu-id="c3467-130">International Analog TV Tuning</span></span>](international-analog-tv-tuning.md)
</dt> </dl>

 

 



