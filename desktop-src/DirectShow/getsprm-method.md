---
description: GetSPRM 方法會抓取指定的系統參數 register。
ms.assetid: c6177f43-2809-4ef2-bc94-ac9a28f94621
title: GetSPRM 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc8b6898902eda55e0e877878343a25d82d03660
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103935630"
---
# <a name="getsprm-method"></a><span data-ttu-id="85895-103">GetSPRM 方法</span><span class="sxs-lookup"><span data-stu-id="85895-103">GetSPRM Method</span></span>

> [!Note]  
> <span data-ttu-id="85895-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="85895-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="85895-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="85895-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="85895-106">方法會抓取 `GetSPRM` 指定的系統參數暫存器。</span><span class="sxs-lookup"><span data-stu-id="85895-106">The `GetSPRM` method retrieves the specified system parameter register.</span></span>

``` syntax
[ iSPRM = ] MSWebDVD.GetSPRM(iIndex)
```

## <a name="parameters"></a><span data-ttu-id="85895-107">參數</span><span class="sxs-lookup"><span data-stu-id="85895-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85895-108"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span><span class="sxs-lookup"><span data-stu-id="85895-108"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span></span>
</dt> <dd>

<span data-ttu-id="85895-109">指定您想要取出其值作為整數的註冊。</span><span class="sxs-lookup"><span data-stu-id="85895-109">Specifies the register whose value you want to retrieve as an Integer.</span></span> <span data-ttu-id="85895-110">整數的範圍必須介於0到23之間。</span><span class="sxs-lookup"><span data-stu-id="85895-110">The Integer must range from 0 through 23.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85895-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="85895-111">Return Value</span></span>

<span data-ttu-id="85895-112">傳回整數值，代表指定之暫存器的內容。</span><span class="sxs-lookup"><span data-stu-id="85895-112">Returns an integer value representing the contents of the specified register.</span></span>

## <a name="remarks"></a><span data-ttu-id="85895-113">備註</span><span class="sxs-lookup"><span data-stu-id="85895-113">Remarks</span></span>

<span data-ttu-id="85895-114">光碟控制項系統參數會註冊 (SPRMs) 。</span><span class="sxs-lookup"><span data-stu-id="85895-114">The disc controls system parameter registers (SPRMs).</span></span> <span data-ttu-id="85895-115">播放機應用程式不需要存取這些暫存器，即可取得任何標準導覽功能。</span><span class="sxs-lookup"><span data-stu-id="85895-115">A player application doesn't need to access these registers for any standard navigation functionality.</span></span> <span data-ttu-id="85895-116">SPRMs 代表播放程式的狀態。</span><span class="sxs-lookup"><span data-stu-id="85895-116">SPRMs represent the status of the player.</span></span> <span data-ttu-id="85895-117">每一個都有意義，由使用者喜好設定、光碟命令，以及應用程式無法直接控制的其他專案來設定。</span><span class="sxs-lookup"><span data-stu-id="85895-117">Each one has a meaning, set by user preferences, disc commands, and other occurrences that an application has no direct control over.</span></span> <span data-ttu-id="85895-118">應用程式可以讀取這些暫存器，但無法寫入這些暫存器。</span><span class="sxs-lookup"><span data-stu-id="85895-118">An application can read these registers but cannot write to them.</span></span> <span data-ttu-id="85895-119">若要有效地使用這些暫存器，您可能需要更深入瞭解 DVD 流覽命令，而非本檔所提供的資訊。</span><span class="sxs-lookup"><span data-stu-id="85895-119">To use these registers effectively, you will probably need a more detailed knowledge of the DVD navigation commands than is provided in this documentation.</span></span> <span data-ttu-id="85895-120">下表顯示每個註冊的內容。</span><span class="sxs-lookup"><span data-stu-id="85895-120">The following table shows the contents of each register.</span></span> <span data-ttu-id="85895-121">如需註冊內容的詳細資訊，請參閱 [ **IDvdInfo2：： GetAllSPRMs**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getallsprms)</span><span class="sxs-lookup"><span data-stu-id="85895-121">For more detailed information on the register contents, see [**IDvdInfo2::GetAllSPRMs**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getallsprms)</span></span>



| <span data-ttu-id="85895-122">註冊</span><span class="sxs-lookup"><span data-stu-id="85895-122">Register</span></span> | <span data-ttu-id="85895-123">目錄</span><span class="sxs-lookup"><span data-stu-id="85895-123">Contents</span></span>                        |
|----------|---------------------------------|
| <span data-ttu-id="85895-124">0</span><span class="sxs-lookup"><span data-stu-id="85895-124">0</span></span>        | <span data-ttu-id="85895-125">功能表語言代碼</span><span class="sxs-lookup"><span data-stu-id="85895-125">Menu language code</span></span>              |
| <span data-ttu-id="85895-126">1</span><span class="sxs-lookup"><span data-stu-id="85895-126">1</span></span>        | <span data-ttu-id="85895-127">音訊串流號碼</span><span class="sxs-lookup"><span data-stu-id="85895-127">Audio stream number</span></span>             |
| <span data-ttu-id="85895-128">2</span><span class="sxs-lookup"><span data-stu-id="85895-128">2</span></span>        | <span data-ttu-id="85895-129">子圖片資料流程號碼</span><span class="sxs-lookup"><span data-stu-id="85895-129">Subpicture stream number</span></span>        |
| <span data-ttu-id="85895-130">3</span><span class="sxs-lookup"><span data-stu-id="85895-130">3</span></span>        | <span data-ttu-id="85895-131">目前的角度數位</span><span class="sxs-lookup"><span data-stu-id="85895-131">Current angle number</span></span>            |
| <span data-ttu-id="85895-132">4</span><span class="sxs-lookup"><span data-stu-id="85895-132">4</span></span>        | <span data-ttu-id="85895-133">目前的標題編號</span><span class="sxs-lookup"><span data-stu-id="85895-133">Current title number</span></span>            |
| <span data-ttu-id="85895-134">5</span><span class="sxs-lookup"><span data-stu-id="85895-134">5</span></span>        | <span data-ttu-id="85895-135">標題編號</span><span class="sxs-lookup"><span data-stu-id="85895-135">Title number</span></span>                    |
| <span data-ttu-id="85895-136">6</span><span class="sxs-lookup"><span data-stu-id="85895-136">6</span></span>        | <span data-ttu-id="85895-137">PGC 編號</span><span class="sxs-lookup"><span data-stu-id="85895-137">PGC number</span></span>                      |
| <span data-ttu-id="85895-138">7</span><span class="sxs-lookup"><span data-stu-id="85895-138">7</span></span>        | <span data-ttu-id="85895-139">目前的章節號碼 (PLATFORM PTT) </span><span class="sxs-lookup"><span data-stu-id="85895-139">Current chapter number (PTT)</span></span>    |
| <span data-ttu-id="85895-140">8</span><span class="sxs-lookup"><span data-stu-id="85895-140">8</span></span>        | <span data-ttu-id="85895-141">反白顯示的按鈕編號</span><span class="sxs-lookup"><span data-stu-id="85895-141">Highlighted button number</span></span>       |
| <span data-ttu-id="85895-142">9</span><span class="sxs-lookup"><span data-stu-id="85895-142">9</span></span>        | <span data-ttu-id="85895-143">流覽計時器</span><span class="sxs-lookup"><span data-stu-id="85895-143">Navigation timer</span></span>                |
| <span data-ttu-id="85895-144">10</span><span class="sxs-lookup"><span data-stu-id="85895-144">10</span></span>       | <span data-ttu-id="85895-145">Nav 的 PGC 跳躍。</span><span class="sxs-lookup"><span data-stu-id="85895-145">PGC jump for nav.</span></span> <span data-ttu-id="85895-146">計時器</span><span class="sxs-lookup"><span data-stu-id="85895-146">timer</span></span>         |
| <span data-ttu-id="85895-147">11</span><span class="sxs-lookup"><span data-stu-id="85895-147">11</span></span>       | <span data-ttu-id="85895-148">卡拉卡拉音訊簡報模式</span><span class="sxs-lookup"><span data-stu-id="85895-148">Karaoke audio presentation mode</span></span> |
| <span data-ttu-id="85895-149">12</span><span class="sxs-lookup"><span data-stu-id="85895-149">12</span></span>       | <span data-ttu-id="85895-150">>PROCMONTRACE.PML 國家/地區碼</span><span class="sxs-lookup"><span data-stu-id="85895-150">PML country/region code</span></span>         |
| <span data-ttu-id="85895-151">13</span><span class="sxs-lookup"><span data-stu-id="85895-151">13</span></span>       | <span data-ttu-id="85895-152">Pml</span><span class="sxs-lookup"><span data-stu-id="85895-152">PML</span></span>                             |
| <span data-ttu-id="85895-153">14</span><span class="sxs-lookup"><span data-stu-id="85895-153">14</span></span>       | <span data-ttu-id="85895-154">影片設定</span><span class="sxs-lookup"><span data-stu-id="85895-154">Video setting</span></span>                   |
| <span data-ttu-id="85895-155">15</span><span class="sxs-lookup"><span data-stu-id="85895-155">15</span></span>       | <span data-ttu-id="85895-156">音訊功能</span><span class="sxs-lookup"><span data-stu-id="85895-156">Audio capability</span></span>                |
| <span data-ttu-id="85895-157">16</span><span class="sxs-lookup"><span data-stu-id="85895-157">16</span></span>       | <span data-ttu-id="85895-158">音訊語言</span><span class="sxs-lookup"><span data-stu-id="85895-158">Audio language</span></span>                  |
| <span data-ttu-id="85895-159">17</span><span class="sxs-lookup"><span data-stu-id="85895-159">17</span></span>       | <span data-ttu-id="85895-160">音訊語言延伸模組</span><span class="sxs-lookup"><span data-stu-id="85895-160">Audio language extension</span></span>        |
| <span data-ttu-id="85895-161">18</span><span class="sxs-lookup"><span data-stu-id="85895-161">18</span></span>       | <span data-ttu-id="85895-162">子圖片語言</span><span class="sxs-lookup"><span data-stu-id="85895-162">Subpicture language</span></span>             |
| <span data-ttu-id="85895-163">19</span><span class="sxs-lookup"><span data-stu-id="85895-163">19</span></span>       | <span data-ttu-id="85895-164">子圖片語言延伸模組</span><span class="sxs-lookup"><span data-stu-id="85895-164">Subpicture language extension</span></span>   |
| <span data-ttu-id="85895-165">20</span><span class="sxs-lookup"><span data-stu-id="85895-165">20</span></span>       | <span data-ttu-id="85895-166">播放程式區功能變數代碼</span><span class="sxs-lookup"><span data-stu-id="85895-166">Player region code</span></span>              |
| <span data-ttu-id="85895-167">21</span><span class="sxs-lookup"><span data-stu-id="85895-167">21</span></span>       | <span data-ttu-id="85895-168">保留</span><span class="sxs-lookup"><span data-stu-id="85895-168">Reserved</span></span>                        |
| <span data-ttu-id="85895-169">22</span><span class="sxs-lookup"><span data-stu-id="85895-169">22</span></span>       | <span data-ttu-id="85895-170">保留</span><span class="sxs-lookup"><span data-stu-id="85895-170">Reserved</span></span>                        |
| <span data-ttu-id="85895-171">23</span><span class="sxs-lookup"><span data-stu-id="85895-171">23</span></span>       | <span data-ttu-id="85895-172">保留</span><span class="sxs-lookup"><span data-stu-id="85895-172">Reserved</span></span>                        |



 

## <a name="see-also"></a><span data-ttu-id="85895-173">另請參閱</span><span class="sxs-lookup"><span data-stu-id="85895-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85895-174">**GetGPRM**</span><span class="sxs-lookup"><span data-stu-id="85895-174">**GetGPRM**</span></span>](getgprm-method.md)
</dt> <dt>

[<span data-ttu-id="85895-175">**SetGPRM**</span><span class="sxs-lookup"><span data-stu-id="85895-175">**SetGPRM**</span></span>](setgprm-method.md)
</dt> </dl>

 

 



