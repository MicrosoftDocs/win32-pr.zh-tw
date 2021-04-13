---
description: 參數資訊
ms.assetid: 2600b200-f57a-46cd-8740-89b7f7aba540
title: 參數資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a1a311bbaa7907af0b3578ed88c28e573649f43
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510208"
---
# <a name="parameter-information"></a><span data-ttu-id="4c1e0-103">參數資訊</span><span class="sxs-lookup"><span data-stu-id="4c1e0-103">Parameter Information</span></span>

<span data-ttu-id="4c1e0-104">[**IMediaParamInfo：： GetParamInfo**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getparaminfo)方法會傳回用來描述參數的 [**MP \_ PARAMINFO**](/previous-versions/windows/desktop/api/Medparam/ns-medparam-mp_paraminfo)結構。</span><span class="sxs-lookup"><span data-stu-id="4c1e0-104">The [**IMediaParamInfo::GetParamInfo**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getparaminfo) method returns an [**MP\_PARAMINFO**](/previous-versions/windows/desktop/api/Medparam/ns-medparam-mp_paraminfo) structure that describes a parameter.</span></span> <span data-ttu-id="4c1e0-105">此結構包含下列資訊：</span><span class="sxs-lookup"><span data-stu-id="4c1e0-105">This structure contains the following information:</span></span>

-   <span data-ttu-id="4c1e0-106">**MpType** 成員會指出參數值的資料類型。</span><span class="sxs-lookup"><span data-stu-id="4c1e0-106">The **mpType** member indicates the data type of the parameter value.</span></span> <span data-ttu-id="4c1e0-107">為了提高效率，所有參數都會實作為32位浮點值。</span><span class="sxs-lookup"><span data-stu-id="4c1e0-107">For efficiency, all parameters are implemented as 32-bit floating-point values.</span></span> <span data-ttu-id="4c1e0-108">[**MP \_ 型**](/previous-versions/windows/desktop/api/Medparam/ne-medparam-mp_type)別列舉會定義要將值轉譯為整數、浮點數、布林值或列舉 (整數系列) 。</span><span class="sxs-lookup"><span data-stu-id="4c1e0-108">The [**MP\_TYPE**](/previous-versions/windows/desktop/api/Medparam/ne-medparam-mp_type) enumeration defines whether to interpret the value as an integer, floating-point value, Boolean, or enumeration (integer series).</span></span>
-   <span data-ttu-id="4c1e0-109">**MopCaps** 成員會指出此參數支援的曲線。</span><span class="sxs-lookup"><span data-stu-id="4c1e0-109">The **mopCaps** member indicates which curves this parameter supports.</span></span> <span data-ttu-id="4c1e0-110">如果資料類型是布林值或列舉，則參數可以支援的唯一曲線是「跳過」。</span><span class="sxs-lookup"><span data-stu-id="4c1e0-110">If the data type is Boolean or enumeration, the only curve that the parameter can support is "Jump."</span></span>
-   <span data-ttu-id="4c1e0-111">**MpdMinValue** 和 **mpdMaxValue** 成員會定義此參數的最小值和最大值。</span><span class="sxs-lookup"><span data-stu-id="4c1e0-111">The **mpdMinValue** and **mpdMaxValue** members define the minimum and maximum values for this parameter.</span></span> <span data-ttu-id="4c1e0-112">此參數的任何曲線都必須落在此範圍內。</span><span class="sxs-lookup"><span data-stu-id="4c1e0-112">Any curves for this parameter must fall within this range.</span></span>
-   <span data-ttu-id="4c1e0-113">**MpdNeutralValue** 成員是參數的預設值。</span><span class="sxs-lookup"><span data-stu-id="4c1e0-113">The **mpdNeutralValue** member is the default value of the parameter.</span></span>
-   <span data-ttu-id="4c1e0-114">**SzLabel** 成員是參數的名稱，而 **szUnitText** 成員是參數的測量單位的名稱。</span><span class="sxs-lookup"><span data-stu-id="4c1e0-114">The **szLabel** member is the name of the parameter, and the **szUnitText** member is the name for the unit of measure for the parameter.</span></span> <span data-ttu-id="4c1e0-115">範例可能包括「磁片區」、「分貝」或「頻率」和「kHz」。</span><span class="sxs-lookup"><span data-stu-id="4c1e0-115">Examples might include "Volume" and "Decibels," or "Frequency" and "kHz."</span></span> <span data-ttu-id="4c1e0-116">這兩個字串都是英文，而且絕對不會當地語系化。</span><span class="sxs-lookup"><span data-stu-id="4c1e0-116">Both strings are English and are never localized.</span></span> <span data-ttu-id="4c1e0-117">SQL-DMO 可以透過 [**IMediaParamInfo：： GetParamText**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getparamtext) 方法提供當地語系化的版本。</span><span class="sxs-lookup"><span data-stu-id="4c1e0-117">The DMO can provide localized versions through the [**IMediaParamInfo::GetParamText**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getparamtext) method.</span></span>

<span data-ttu-id="4c1e0-118">在每個參數的整個存留期內，每個參數的資訊都會保持固定。</span><span class="sxs-lookup"><span data-stu-id="4c1e0-118">The information for each parameter remains fixed throughout the lifetime of the DMO.</span></span> <span data-ttu-id="4c1e0-119">因此，用戶端可以查詢此資訊一次，然後加以快取。</span><span class="sxs-lookup"><span data-stu-id="4c1e0-119">Therefore, the client can query for this information once and then cache it.</span></span>

<span data-ttu-id="4c1e0-120">**時間格式**</span><span class="sxs-lookup"><span data-stu-id="4c1e0-120">**Time Formats**</span></span>

<span data-ttu-id="4c1e0-121">用戶端必須為輸入資料輸入時間戳記，以便可以計算對應的參數值。</span><span class="sxs-lookup"><span data-stu-id="4c1e0-121">The client must time stamp the input data, so that the DMO can calculate the corresponding parameter values.</span></span> <span data-ttu-id="4c1e0-122">根據預設，時間戳記代表單位為100毫微秒，也稱為 *參考時間*。</span><span class="sxs-lookup"><span data-stu-id="4c1e0-122">By default, time stamps represent units of 100 nanoseconds, also called *reference time*.</span></span> <span data-ttu-id="4c1e0-123">不過，此時間單位對每個應用程式來說都不方便，因此，每個的選項都有支援其他時間格式的選項。</span><span class="sxs-lookup"><span data-stu-id="4c1e0-123">This time unit is not convenient for every application, however, so a DMO has an option to support other time formats.</span></span> <span data-ttu-id="4c1e0-124">時間格式是由 GUID 所識別。</span><span class="sxs-lookup"><span data-stu-id="4c1e0-124">Time formats are identified by GUID.</span></span>



| <span data-ttu-id="4c1e0-125">**GUID**</span><span class="sxs-lookup"><span data-stu-id="4c1e0-125">**GUID**</span></span>              | <span data-ttu-id="4c1e0-126">Description</span><span class="sxs-lookup"><span data-stu-id="4c1e0-126">Description</span></span>                   |
|-----------------------|-------------------------------|
| <span data-ttu-id="4c1e0-127">GUID \_ 時間 \_ 參考</span><span class="sxs-lookup"><span data-stu-id="4c1e0-127">GUID\_TIME\_REFERENCE</span></span> | <span data-ttu-id="4c1e0-128">參考時間</span><span class="sxs-lookup"><span data-stu-id="4c1e0-128">Reference time</span></span>                |
| <span data-ttu-id="4c1e0-129">GUID \_ 時間 \_ 音樂</span><span class="sxs-lookup"><span data-stu-id="4c1e0-129">GUID\_TIME\_MUSIC</span></span>     | <span data-ttu-id="4c1e0-130">每季的各部分附注 (PPQN) </span><span class="sxs-lookup"><span data-stu-id="4c1e0-130">Parts per quarter note (PPQN)</span></span> |
| <span data-ttu-id="4c1e0-131">GUID \_ 時間 \_ 範例</span><span class="sxs-lookup"><span data-stu-id="4c1e0-131">GUID\_TIME\_SAMPLES</span></span>   | <span data-ttu-id="4c1e0-132">每秒樣本數</span><span class="sxs-lookup"><span data-stu-id="4c1e0-132">Samples per second</span></span>            |



 

<span data-ttu-id="4c1e0-133">建議協力廠商視需要定義自己的時間格式。</span><span class="sxs-lookup"><span data-stu-id="4c1e0-133">Third parties are encouraged to define their own time formats as needed.</span></span> <span data-ttu-id="4c1e0-134">不過，所有 DMOs 都必須支援參考時間。</span><span class="sxs-lookup"><span data-stu-id="4c1e0-134">However, all DMOs must support reference time.</span></span> <span data-ttu-id="4c1e0-135">這會提供每個人都可以使用的標準基準。</span><span class="sxs-lookup"><span data-stu-id="4c1e0-135">This provides a standard baseline that everyone can use.</span></span> <span data-ttu-id="4c1e0-136">若要判斷 SQL-DMO 支援多少時間格式，請呼叫 [**IMediaParamInfo：： GetNumTimeFormats**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getnumtimeformats) 方法。</span><span class="sxs-lookup"><span data-stu-id="4c1e0-136">To determine how many time formats a DMO supports, call the [**IMediaParamInfo::GetNumTimeFormats**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getnumtimeformats) method.</span></span> <span data-ttu-id="4c1e0-137">若要列舉支援的格式，請呼叫 [**IMediaParamInfo：： GetSupportedTimeFormat**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getsupportedtimeformat) 方法。</span><span class="sxs-lookup"><span data-stu-id="4c1e0-137">To enumerate the supported formats, call the [**IMediaParamInfo::GetSupportedTimeFormat**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparaminfo-getsupportedtimeformat) method.</span></span>

<span data-ttu-id="4c1e0-138">若要設定時間格式，請呼叫 [**IMediaParams：： SetTimeFormat**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-settimeformat)。</span><span class="sxs-lookup"><span data-stu-id="4c1e0-138">To set the time format, call [**IMediaParams::SetTimeFormat**](/previous-versions/windows/desktop/api/Medparam/nf-medparam-imediaparams-settimeformat).</span></span> <span data-ttu-id="4c1e0-139">這個方法會指定時間格式的 GUID 和 *時間資料*，也就是每個時鐘的單位數刻度。</span><span class="sxs-lookup"><span data-stu-id="4c1e0-139">This method specifies the time format GUID and the *time data*, which is the number of units per clock tick.</span></span> <span data-ttu-id="4c1e0-140">例如，如果時間格式為每秒的樣本，而時間資料為32，則時間戳記值10會對應到320範例。</span><span class="sxs-lookup"><span data-stu-id="4c1e0-140">For example, if the time format is samples per second, and the time data is 32, then a time stamp value of 10 corresponds to 320 samples.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c1e0-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="4c1e0-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c1e0-142">媒體參數</span><span class="sxs-lookup"><span data-stu-id="4c1e0-142">Media Parameters</span></span>](media-parameters.md)
</dt> </dl>

 

 



