---
description: 描述與 PresentEx 呼叫相關的 swapchain 統計資料。
ms.assetid: aa100b83-6fbf-442d-9891-7fc034a5b1d5
title: D3DPRESENTSTATS 結構 (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPRESENTSTATS
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b49a589fa1702f61e5a5daef806a5b36d464d0ec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196310"
---
# <a name="d3dpresentstats-structure"></a><span data-ttu-id="7909e-103">D3DPRESENTSTATS 結構</span><span class="sxs-lookup"><span data-stu-id="7909e-103">D3DPRESENTSTATS structure</span></span>

<span data-ttu-id="7909e-104">描述與 [**PresentEx**](/windows/win32/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) 呼叫相關的 swapchain 統計資料。</span><span class="sxs-lookup"><span data-stu-id="7909e-104">Describes swapchain statistics relating to [**PresentEx**](/windows/win32/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) calls.</span></span>

## <a name="syntax"></a><span data-ttu-id="7909e-105">語法</span><span class="sxs-lookup"><span data-stu-id="7909e-105">Syntax</span></span>


```C++
typedef struct _D3DPRESENTSTATS {
  UINT          PresentCount;
  UINT          PresentRefreshCount;
  UINT          SyncRefreshCount;
  LARGE_INTEGER SyncQPCTime;
  LARGE_INTEGER SyncGPUTime;
} D3DPRESENTSTATS;
```



## <a name="members"></a><span data-ttu-id="7909e-106">成員</span><span class="sxs-lookup"><span data-stu-id="7909e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7909e-107">**PresentCount**</span><span class="sxs-lookup"><span data-stu-id="7909e-107">**PresentCount**</span></span>
</dt> <dd>

<span data-ttu-id="7909e-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7909e-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7909e-109">目前正在輸出至螢幕的顯示裝置所執行的成功目前呼叫計數。</span><span class="sxs-lookup"><span data-stu-id="7909e-109">Running count of successful Present calls made by a display device that is currently outputting to screen.</span></span> <span data-ttu-id="7909e-110">此參數實際上是最後一個出現之呼叫的目前識別碼，不一定是目前所發出的 API 呼叫總數。</span><span class="sxs-lookup"><span data-stu-id="7909e-110">This parameter is really the Present ID of the last Present call and is not necessarily the total number of Present API calls made.</span></span>

</dd> <dt>

<span data-ttu-id="7909e-111">**PresentRefreshCount**</span><span class="sxs-lookup"><span data-stu-id="7909e-111">**PresentRefreshCount**</span></span>
</dt> <dd>

<span data-ttu-id="7909e-112">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7909e-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7909e-113">在螢幕上顯示最後一次出現的 vblank 計數，vblank 計數會隨著每個 vblank 間隔遞增一次。</span><span class="sxs-lookup"><span data-stu-id="7909e-113">The vblank count at which the last Present was displayed on screen, the vblank count increments once every vblank interval.</span></span>

</dd> <dt>

<span data-ttu-id="7909e-114">**SyncRefreshCount**</span><span class="sxs-lookup"><span data-stu-id="7909e-114">**SyncRefreshCount**</span></span>
</dt> <dd>

<span data-ttu-id="7909e-115">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7909e-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7909e-116">排程器上次呼叫 QueryPerformanceCounter 來取樣電腦時間時的 vblank 計數。</span><span class="sxs-lookup"><span data-stu-id="7909e-116">The vblank count when the scheduler last sampled the machine time by calling QueryPerformanceCounter.</span></span>

</dd> <dt>

<span data-ttu-id="7909e-117">**SyncQPCTime**</span><span class="sxs-lookup"><span data-stu-id="7909e-117">**SyncQPCTime**</span></span>
</dt> <dd>

<span data-ttu-id="7909e-118">類型： **[**大型 \_ 整數**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span><span class="sxs-lookup"><span data-stu-id="7909e-118">Type: **[**LARGE\_INTEGER**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span></span>

</dd> <dd>

<span data-ttu-id="7909e-119">排程器上次取樣的電腦時間，藉由呼叫 [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)取得。</span><span class="sxs-lookup"><span data-stu-id="7909e-119">The scheduler's last sampled machine time, obtained by calling [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

</dd> <dt>

<span data-ttu-id="7909e-120">**SyncGPUTime**</span><span class="sxs-lookup"><span data-stu-id="7909e-120">**SyncGPUTime**</span></span>
</dt> <dd>

<span data-ttu-id="7909e-121">類型： **[**大型 \_ 整數**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span><span class="sxs-lookup"><span data-stu-id="7909e-121">Type: **[**LARGE\_INTEGER**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**</span></span>

</dd> <dd>

<span data-ttu-id="7909e-122">不使用這個值。</span><span class="sxs-lookup"><span data-stu-id="7909e-122">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7909e-123">備註</span><span class="sxs-lookup"><span data-stu-id="7909e-123">Remarks</span></span>

<span data-ttu-id="7909e-124">當9Ex 應用程式 (D3DSWAPEFFECT FLIPEX) 採用翻轉模式時 \_ ，應用程式可以在任何時間點呼叫 GetPresentStatistics 來偵測框架卸載。</span><span class="sxs-lookup"><span data-stu-id="7909e-124">When a 9Ex application adopts Flip Mode present (D3DSWAPEFFECT\_FLIPEX), applications can detect frame dropping by calling GetPresentStatistics at any point in time.</span></span> <span data-ttu-id="7909e-125">實際上，使用者可以執行下列動作。</span><span class="sxs-lookup"><span data-stu-id="7909e-125">In effect, they can do the following.</span></span>

1.  <span data-ttu-id="7909e-126">轉譯為背景緩衝區</span><span class="sxs-lookup"><span data-stu-id="7909e-126">Render to the back buffer</span></span>
2.  <span data-ttu-id="7909e-127">呼叫存在</span><span class="sxs-lookup"><span data-stu-id="7909e-127">Call Present</span></span>
3.  <span data-ttu-id="7909e-128">呼叫 GetPresentStats 並儲存產生的 D3DPRESENTSTATS 結構</span><span class="sxs-lookup"><span data-stu-id="7909e-128">Call GetPresentStats and store the resulting D3DPRESENTSTATS structure</span></span>
4.  <span data-ttu-id="7909e-129">將下一個畫面格轉譯為背景緩衝區</span><span class="sxs-lookup"><span data-stu-id="7909e-129">Render the next frame to the back buffer</span></span>
5.  <span data-ttu-id="7909e-130">呼叫存在</span><span class="sxs-lookup"><span data-stu-id="7909e-130">Call Present</span></span>
6.  <span data-ttu-id="7909e-131">重複步驟4和 5 1 或更多次</span><span class="sxs-lookup"><span data-stu-id="7909e-131">Repeat steps 4 and 5 one or more times</span></span>
7.  <span data-ttu-id="7909e-132">呼叫 GetPresentStats 並儲存產生的 D3DPRESENTSTATS 結構</span><span class="sxs-lookup"><span data-stu-id="7909e-132">Call GetPresentStats and store the resulting D3DPRESENTSTATS structure</span></span>
8.  <span data-ttu-id="7909e-133">比較兩個預存 D3DPRESENTSTATS 結構的 PresentRefreshCount 值。</span><span class="sxs-lookup"><span data-stu-id="7909e-133">Compare the values of PresentRefreshCount from the two stored D3DPRESENTSTATS structures.</span></span> <span data-ttu-id="7909e-134">應用程式可以根據 PresentRefreshCount 增量和 PresentCount 指派的框架呈現的假設，來計算特定 PresentCount 參數的對應 PresentRefreshCount。</span><span class="sxs-lookup"><span data-stu-id="7909e-134">The application can calculate the corresponding PresentRefreshCount of a particular PresentCount parameter based on the assumptions of PresentRefreshCount increment and PresentCount assignment of frame presents.</span></span> <span data-ttu-id="7909e-135">如果上一次取樣的 PresentRefreshCount 不符合 PresentCount (也就是，如果 PresentRefreshCount 已遞增但 PresentCount 沒有，則會卸載畫面格。 ) </span><span class="sxs-lookup"><span data-stu-id="7909e-135">If the PresentRefreshCount last sampled does not match the PresentCount (i.e. if the PresentRefreshCount has incremented but PresentCount has not, then there was frame dropping.)</span></span>

<span data-ttu-id="7909e-136">應用程式可以藉由取樣任何兩個 PresentCount 和 GetPresentStats (實例來判斷是否已卸載框架) 。</span><span class="sxs-lookup"><span data-stu-id="7909e-136">Applications can determine whether a frame has been dropped by sampling any two instances of PresentCount and GetPresentStats (by calling GetPresentStats API at any two points in time).</span></span> <span data-ttu-id="7909e-137">例如，以與監視器重新整理速率相同的速率呈現的媒體應用程式 (例如，監視器重新整理速率為60Hz，應用程式每隔1/60 秒會顯示一個框架，) 想要呈現框架 A、B、C、D、E，每個畫面格都對應到目前的識別碼 (PresentCount) 1、2、3、7、8。</span><span class="sxs-lookup"><span data-stu-id="7909e-137">For example, a media application that is presenting at the same rate as the monitor refresh rate (for example, monitor refresh rate is 60Hz, the application presents a frame every 1/60 seconds) wants to present frames A, B, C, D, E, each corresponding to Present IDs (PresentCount) 1, 2, 3, 7, 8.</span></span>

<span data-ttu-id="7909e-138">應用程式程式碼看起來會像下列順序。</span><span class="sxs-lookup"><span data-stu-id="7909e-138">The application code looks like the following sequence.</span></span>

1.  <span data-ttu-id="7909e-139">將框架 A 轉譯為背景緩衝區</span><span class="sxs-lookup"><span data-stu-id="7909e-139">Render frame A to the back buffer</span></span>
2.  <span data-ttu-id="7909e-140">呼叫存在，PresentCount = 1</span><span class="sxs-lookup"><span data-stu-id="7909e-140">Call Present, PresentCount = 1</span></span>
3.  <span data-ttu-id="7909e-141">呼叫 GetPresentStats 並儲存產生的 D3DPRESENTSTATS 結構</span><span class="sxs-lookup"><span data-stu-id="7909e-141">Call GetPresentStats and store the resulting D3DPRESENTSTATS structure</span></span>
4.  <span data-ttu-id="7909e-142">分別轉譯接下來的4個框架 B、C、D、E</span><span class="sxs-lookup"><span data-stu-id="7909e-142">Render the next 4 frames, B, C, D, E, respectively</span></span>
5.  <span data-ttu-id="7909e-143">呼叫目前的4次，分別為 PresentCounts = 2、3、7、8</span><span class="sxs-lookup"><span data-stu-id="7909e-143">Call Present 4 times, PresentCounts = 2, 3, 7, 8, respectively</span></span>
6.  <span data-ttu-id="7909e-144">呼叫 GetPresentStats 並儲存產生的 D3DPRESENTSTATS 結構</span><span class="sxs-lookup"><span data-stu-id="7909e-144">Call GetPresentStats and store the resulting D3DPRESENTSTATS structure</span></span>
7.  <span data-ttu-id="7909e-145">比較兩個預存 D3DPRESENTSTATS 結構的 PresentRefreshCount 值。</span><span class="sxs-lookup"><span data-stu-id="7909e-145">Compare the values of PresentRefreshCount from the two stored D3DPRESENTSTATS structures.</span></span> <span data-ttu-id="7909e-146">如果差異為2，也就是兩個 GetPresentStats API 呼叫之間已超過 2 vblank 間隔，則最後一個呈現的畫面格應該是畫面格 C。由於應用程式會顯示一次 vblank 的間隔， (監視器) 的重新整理頻率、呈現框架 A 與顯示畫面格 C 之間所經過的時間，應該是 2 vblanks。</span><span class="sxs-lookup"><span data-stu-id="7909e-146">If the difference is 2, i.e. 2 vblank intervals has elapsed between the two GetPresentStats API calls, then the last presented frame should be frame C. Because the application presents once very vblank interval (the refresh rate of the monitor), the time elapsed between when frame A is presented and when frame C is presented should be 2 vblanks.</span></span>
8.  <span data-ttu-id="7909e-147">比較兩個預存 D3DPRESENTSTATS 結構的 PresentCount 值。</span><span class="sxs-lookup"><span data-stu-id="7909e-147">Compare the values of PresentCount from the two stored D3DPRESENTSTATS structures.</span></span> <span data-ttu-id="7909e-148">如果第一個 PresentCount 是 1 (對應至框架 A) ，而第二個 (PresentCount 對應至框架 C) ，則未卸載任何框架。</span><span class="sxs-lookup"><span data-stu-id="7909e-148">If the first PresentCount is 1 (corresponding to frame A) and the second PresentCount is 3 (corresponding to frame C), then no frames have been dropped.</span></span> <span data-ttu-id="7909e-149">如果第二個 PresentCount 是3（對應至框架 D），則應用程式會知道一個框架已卸載。</span><span class="sxs-lookup"><span data-stu-id="7909e-149">If the second PresentCount is 3, which corresponds to frame D, then the application knows that one frame has been dropped.</span></span>

<span data-ttu-id="7909e-150">請注意，呼叫 GetPresentStatistics 之後，不論 FLIPEX 模式 PresentEx 呼叫的狀態為何，都會進行處理。</span><span class="sxs-lookup"><span data-stu-id="7909e-150">Note that GetPresentStatistics will be processed after it is called, regardless of the state of FLIPEX mode PresentEx calls.</span></span>

<span data-ttu-id="7909e-151">**Windows Vista：** 目前的呼叫將會排入佇列，然後再處理 GetPresentStats 呼叫。</span><span class="sxs-lookup"><span data-stu-id="7909e-151">**Windows Vista:** The Present calls will be queued and then processed before GetPresentStats call will be processed.</span></span>

<span data-ttu-id="7909e-152">當應用程式偵測到呈現特定畫面格之後，就可以略過這些框架，並修正簡報以重新同步處理 vblank。</span><span class="sxs-lookup"><span data-stu-id="7909e-152">When an application detects that the presentation of certain frames are behind, it can skip those frames and correct the presentation to re-synchronize with the vblank.</span></span> <span data-ttu-id="7909e-153">若要這樣做，應用程式可以單純地轉譯最晚的畫面格，並使用佇列中下一個正確的框架開始轉譯。</span><span class="sxs-lookup"><span data-stu-id="7909e-153">To do this, an application can simply not render the late frames and start rendering with the next correct frame in the queue.</span></span> <span data-ttu-id="7909e-154">但是，如果應用程式已經開始轉譯延遲的畫面格，就可以在名為 D3DPRESENT FORCEIMMEDIATE 的 D3D9Ex 中使用新的呈現參數 \_ 。</span><span class="sxs-lookup"><span data-stu-id="7909e-154">However, if an application has already started the rendering of late frames, it can use a new Present parameter in D3D9Ex called D3DPRESENT\_FORCEIMMEDIATE.</span></span> <span data-ttu-id="7909e-155">旗標會在目前的 API 呼叫的參數中傳遞，並向執行時間指出框架將在下一個 vblank 間隔內立即處理，實際上完全不會顯示在螢幕上。</span><span class="sxs-lookup"><span data-stu-id="7909e-155">The flag will be passed in the parameters of Present API call and indicates to the runtime that the frame will be processed immediately within the next vblank interval, effectively not visible on screen at all.</span></span> <span data-ttu-id="7909e-156">以下是在上一個範例中的最後一個步驟之後的應用程式使用範例。</span><span class="sxs-lookup"><span data-stu-id="7909e-156">Here is the application usage example after the last step in the previous example.</span></span>

1.  <span data-ttu-id="7909e-157">將下一個畫面格轉譯為背景緩衝區</span><span class="sxs-lookup"><span data-stu-id="7909e-157">Render the next frame to the back buffer</span></span>
2.  <span data-ttu-id="7909e-158">從 PresentRefreshCount 探索下一個畫面格已延遲</span><span class="sxs-lookup"><span data-stu-id="7909e-158">Discover from PresentRefreshCount that the next frame is already late</span></span>
3.  <span data-ttu-id="7909e-159">將目前間隔設定為 D3DPRESENT \_ FORCEIMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="7909e-159">Set Present interval to D3DPRESENT\_FORCEIMMEDIATE</span></span>
4.  <span data-ttu-id="7909e-160">在下一個畫面上呼叫</span><span class="sxs-lookup"><span data-stu-id="7909e-160">Call Present on the next frame</span></span>

<span data-ttu-id="7909e-161">應用程式可以用相同的方式同步處理影片和音訊串流，因為 GetPresentStatistics 的行為不會在該情況下變更。</span><span class="sxs-lookup"><span data-stu-id="7909e-161">Applications can synchronize video and audio streams in the same manner because the behavior of GetPresentStatistics does not change in that scenario.</span></span>

<span data-ttu-id="7909e-162">D3D9Ex Flip 模式提供畫面格統計資訊給視窗型應用程式和全螢幕9Ex 應用程式。</span><span class="sxs-lookup"><span data-stu-id="7909e-162">D3D9Ex Flip Mode provides frame statistics information to windowed applications and full screen 9Ex applications.</span></span>

<span data-ttu-id="7909e-163">**Windows Vista：** 使用 DWM Api 來取出目前的統計資料。</span><span class="sxs-lookup"><span data-stu-id="7909e-163">**Windows Vista:** Use the DWM APIs for retrieving present statistics.</span></span>

<span data-ttu-id="7909e-164">當桌面視窗管理員關閉時，使用切換模式的視窗模式9Ex 應用程式將會收到有限精確度的現有統計資料資訊。</span><span class="sxs-lookup"><span data-stu-id="7909e-164">When Desktop Window Manager is turned off, windowed mode 9Ex applications using flip mode will receive present statistics information of limited accuracy.</span></span>

<span data-ttu-id="7909e-165">\* \* Windows Vista： \* \*</span><span class="sxs-lookup"><span data-stu-id="7909e-165">\*\*Windows Vista:  \*\*</span></span>

<span data-ttu-id="7909e-166">如果應用程式的速度不夠快，無法跟上監視器的重新整理率，可能是因為硬體太慢或系統資源不足，則可能會遇到圖形問題。</span><span class="sxs-lookup"><span data-stu-id="7909e-166">If an application is not fast enough to keep up with the monitor's refresh rate, possibly due to slow hardware or lack of system resources, then it can experience a graphics glitch.</span></span> <span data-ttu-id="7909e-167">問題就是所謂的視覺化擁塞中斷。</span><span class="sxs-lookup"><span data-stu-id="7909e-167">A glitch is a so-called visual hiccup.</span></span> <span data-ttu-id="7909e-168">如果監視設定為在 60 Hz 重新整理，且應用程式只能管理 30 fps，則一半的畫面格將會發生問題。</span><span class="sxs-lookup"><span data-stu-id="7909e-168">If a monitor is set to refresh at 60 Hz, and the application can only manage 30 fps, then half of the frames will have glitches.</span></span>

<span data-ttu-id="7909e-169">應用程式可以藉由追蹤 SynchRefreshCount 來偵測出問題。</span><span class="sxs-lookup"><span data-stu-id="7909e-169">Applications can detect a glitch by keeping track of SynchRefreshCount.</span></span> <span data-ttu-id="7909e-170">例如，應用程式可能會執行下列一連串的動作。</span><span class="sxs-lookup"><span data-stu-id="7909e-170">For example, an application might perform the following sequence of actions.</span></span>

1.  <span data-ttu-id="7909e-171">轉譯為背景緩衝區。</span><span class="sxs-lookup"><span data-stu-id="7909e-171">Render to the back buffer.</span></span>
2.  <span data-ttu-id="7909e-172">呼叫存在。</span><span class="sxs-lookup"><span data-stu-id="7909e-172">Call Present.</span></span>
3.  <span data-ttu-id="7909e-173">呼叫 GetPresentStats 並儲存產生的 D3DPRESENTSTATS 結構。</span><span class="sxs-lookup"><span data-stu-id="7909e-173">Call GetPresentStats and store the resulting D3DPRESENTSTATS structure.</span></span>
4.  <span data-ttu-id="7909e-174">將下一個畫面格轉譯為背景緩衝區。</span><span class="sxs-lookup"><span data-stu-id="7909e-174">Render the next frame to the back buffer.</span></span>
5.  <span data-ttu-id="7909e-175">呼叫存在。</span><span class="sxs-lookup"><span data-stu-id="7909e-175">Call Present.</span></span>
6.  <span data-ttu-id="7909e-176">呼叫 GetPresentStats 並儲存產生的 D3DPRESENTSTATS 結構。</span><span class="sxs-lookup"><span data-stu-id="7909e-176">Call GetPresentStats and store the resulting D3DPRESENTSTATS structure.</span></span>
7.  <span data-ttu-id="7909e-177">比較兩個預存 D3DPRESENTSTATS 結構的 SyncRefreshCount 值。</span><span class="sxs-lookup"><span data-stu-id="7909e-177">Compare the values of SyncRefreshCount from the two stored D3DPRESENTSTATS structures.</span></span> <span data-ttu-id="7909e-178">如果差異大於一，則會略過框架。</span><span class="sxs-lookup"><span data-stu-id="7909e-178">If the difference is greater than one, then a frame was skipped.</span></span>

## <a name="requirements"></a><span data-ttu-id="7909e-179">規格需求</span><span class="sxs-lookup"><span data-stu-id="7909e-179">Requirements</span></span>



| <span data-ttu-id="7909e-180">需求</span><span class="sxs-lookup"><span data-stu-id="7909e-180">Requirement</span></span> | <span data-ttu-id="7909e-181">值</span><span class="sxs-lookup"><span data-stu-id="7909e-181">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7909e-182">標頭</span><span class="sxs-lookup"><span data-stu-id="7909e-182">Header</span></span><br/> | <dl> <span data-ttu-id="7909e-183"><dt>D3d9types。h</dt></span><span class="sxs-lookup"><span data-stu-id="7909e-183"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7909e-184">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7909e-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7909e-185">Direct3D 結構</span><span class="sxs-lookup"><span data-stu-id="7909e-185">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
