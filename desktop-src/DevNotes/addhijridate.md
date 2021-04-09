---
description: HKCU \\ 主控台 \\ 國際化。
ms.assetid: e2925d92-19df-42e5-9893-2820f437d3a5
title: AddHijriDate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22a1c4a721af18e0a8994efdd7641581aa01c133
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847136"
---
# <a name="addhijridate"></a><span data-ttu-id="c2741-103">AddHijriDate</span><span class="sxs-lookup"><span data-stu-id="c2741-103">AddHijriDate</span></span>

<span data-ttu-id="c2741-104">**HKCU \\ 主控台 \\ 國際**</span><span class="sxs-lookup"><span data-stu-id="c2741-104">**HKCU\\Control Panel\\International**</span></span>



| <span data-ttu-id="c2741-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="c2741-105">Data type</span></span> | <span data-ttu-id="c2741-106">範圍</span><span class="sxs-lookup"><span data-stu-id="c2741-106">Range</span></span>                      | <span data-ttu-id="c2741-107">預設值</span><span class="sxs-lookup"><span data-stu-id="c2741-107">Default value</span></span> |
|-----------|----------------------------|---------------|
| <span data-ttu-id="c2741-108">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="c2741-108">REG\_SZ</span></span>   | <span data-ttu-id="c2741-109">*有效的調整值*</span><span class="sxs-lookup"><span data-stu-id="c2741-109">*A valid adjustment value*</span></span> | <span data-ttu-id="c2741-110">(無)</span><span class="sxs-lookup"><span data-stu-id="c2741-110">(None)</span></span>        |



 

## <a name="description"></a><span data-ttu-id="c2741-111">Description</span><span class="sxs-lookup"><span data-stu-id="c2741-111">Description</span></span>

<span data-ttu-id="c2741-112">指定回曆內日期的調整。</span><span class="sxs-lookup"><span data-stu-id="c2741-112">Specifies adjustments to the date within the Hijri calendar.</span></span>

<span data-ttu-id="c2741-113">回曆是在伊斯蘭世界中使用的陰曆行事曆。</span><span class="sxs-lookup"><span data-stu-id="c2741-113">The Hijri calendar is a lunar calendar used in the Islamic world.</span></span> <span data-ttu-id="c2741-114">月份的開始和結束時間，是根據新月球的觀察 decree。</span><span class="sxs-lookup"><span data-stu-id="c2741-114">The months begin and end according to a decree that is based on the observation of the new moon.</span></span> <span data-ttu-id="c2741-115">很難精確地預測月份的開頭和結尾，而且有區域性變化，因此會對行事曆進行調整，介於零到兩天之間。</span><span class="sxs-lookup"><span data-stu-id="c2741-115">It is difficult to accurately predict the beginnings and endings of the months, and there are regional variations, so an adjustment of between zero and two days is made to the calendar.</span></span>

<span data-ttu-id="c2741-116">**AddHijriDate** 登錄值會儲存此調整值，如下所示。</span><span class="sxs-lookup"><span data-stu-id="c2741-116">The **AddHijriDate** registry value stores this adjustment value as follows.</span></span>



| <span data-ttu-id="c2741-117">值</span><span class="sxs-lookup"><span data-stu-id="c2741-117">Value</span></span>          | <span data-ttu-id="c2741-118">意義</span><span class="sxs-lookup"><span data-stu-id="c2741-118">Meaning</span></span>                                                                                                                                                                                                                               |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2741-119">AddHijriDate-2</span><span class="sxs-lookup"><span data-stu-id="c2741-119">AddHijriDate-2</span></span> | <span data-ttu-id="c2741-120">兩天減去。</span><span class="sxs-lookup"><span data-stu-id="c2741-120">Subtract two days.</span></span>                                                                                                                                                                                                                    |
| <span data-ttu-id="c2741-121">AddHijriDate</span><span class="sxs-lookup"><span data-stu-id="c2741-121">AddHijriDate</span></span>   | <span data-ttu-id="c2741-122">減去一天。</span><span class="sxs-lookup"><span data-stu-id="c2741-122">Subtract one day.</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="c2741-123">(空白)</span><span class="sxs-lookup"><span data-stu-id="c2741-123">(blank)</span></span>        | <span data-ttu-id="c2741-124">不需要進行調整。</span><span class="sxs-lookup"><span data-stu-id="c2741-124">No adjustment is necessary.</span></span> <span data-ttu-id="c2741-125"> (如果尚未調整日期，此專案就不會出現在登錄中。</span><span class="sxs-lookup"><span data-stu-id="c2741-125">(If the date has not been adjusted, this entry does not appear in the registry.</span></span> <span data-ttu-id="c2741-126">如果日期已經過調整，然後還原為其原始值，此專案就會出現在登錄中，沒有任何值。 ) </span><span class="sxs-lookup"><span data-stu-id="c2741-126">If the date has been adjusted and then restored to its original value, this entry appears in the registry with no value.)</span></span> |
| <span data-ttu-id="c2741-127">AddHijriDate + 1</span><span class="sxs-lookup"><span data-stu-id="c2741-127">AddHijriDate+1</span></span> | <span data-ttu-id="c2741-128">新增一天。</span><span class="sxs-lookup"><span data-stu-id="c2741-128">Add one day.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="c2741-129">AddHijriDate + 2</span><span class="sxs-lookup"><span data-stu-id="c2741-129">AddHijriDate+2</span></span> | <span data-ttu-id="c2741-130">新增兩天。</span><span class="sxs-lookup"><span data-stu-id="c2741-130">Add two days.</span></span>                                                                                                                                                                                                                         |



 

<span data-ttu-id="c2741-131">此項目依預設不存在於登錄中。</span><span class="sxs-lookup"><span data-stu-id="c2741-131">This entry does not exist in the registry by default.</span></span> <span data-ttu-id="c2741-132">您可以使用 [登錄編輯程式] Regedit.exe，或使用下面所述的變更方法來加入它。</span><span class="sxs-lookup"><span data-stu-id="c2741-132">You can add it by using the registry editor Regedit.exe or by using the change method described below.</span></span>

## <a name="change-method"></a><span data-ttu-id="c2741-133">變更方法</span><span class="sxs-lookup"><span data-stu-id="c2741-133">Change Method</span></span>

<span data-ttu-id="c2741-134">若要變更此專案的值，或將它新增至登錄，請先安裝複雜字集和由右至左語言的檔案。</span><span class="sxs-lookup"><span data-stu-id="c2741-134">To change the value of this entry, or to add it to the registry, first install the files for complex script and right-to-left languages.</span></span> <span data-ttu-id="c2741-135">在主控台中，按一下 [ **地區及語言選項**]，然後按一下 [ **語言** ] 索引標籤。在 [ **補充語言支援**] 下，選取 [為 **複雜字集和由右至左的語言安裝** 檔案] 核取方塊， (包括泰文) 。</span><span class="sxs-lookup"><span data-stu-id="c2741-135">In Control Panel, click **Regional and Language Options**, then click the **Languages** tab. Under **Supplemental language support**, select the checkbox to **Install files for complex script and right-to-left languages (including Thai)**.</span></span> <span data-ttu-id="c2741-136">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="c2741-136">Click **OK**.</span></span>

<span data-ttu-id="c2741-137">若要變更此專案的值，或將它新增至登錄，請從主控台按一下 [ **地區及語言選項**]。</span><span class="sxs-lookup"><span data-stu-id="c2741-137">To change the value of this entry, or to add it to the registry, from Control Panel, click **Regional and Language Options**.</span></span> <span data-ttu-id="c2741-138">在 [ **標準及格式** ] 欄位中，選取使用回曆的地區設定。</span><span class="sxs-lookup"><span data-stu-id="c2741-138">In the **Standards and Formats** field, select a locale that uses the Hijri calendar.</span></span> <span data-ttu-id="c2741-139">按一下 [ **自訂** ] 按鈕，然後按一下 [ **日期** ] 索引標籤。在 [ **調整回曆的日期為：** ] 下拉式清單中，選取適當的值。</span><span class="sxs-lookup"><span data-stu-id="c2741-139">Click the **Customize** button, then click the **Date** tab. In the **Adjust Hijri date to:** drop-down list, select the appropriate value.</span></span> <span data-ttu-id="c2741-140">按一下 **[確定]**，然後再按一下 **[確定]** 。</span><span class="sxs-lookup"><span data-stu-id="c2741-140">Click **OK**, then click **OK** again.</span></span>

## <a name="activation-method"></a><span data-ttu-id="c2741-141">啟用方法</span><span class="sxs-lookup"><span data-stu-id="c2741-141">Activation Method</span></span>

<span data-ttu-id="c2741-142">透過主控台所做的變更會立即生效。</span><span class="sxs-lookup"><span data-stu-id="c2741-142">Changes to this entry made through Control Panel take effect immediately.</span></span>

 

 



