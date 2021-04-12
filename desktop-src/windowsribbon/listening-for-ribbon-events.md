---
title: 接聽功能區事件
description: Windows 功能區架構使用 Windows 的事件追蹤 (ETW) 基礎結構，讓開發人員瞭解使用者如何與應用程式的功能區互動。
ms.assetid: F29A8E41-C902-410E-BD28-653E078320E9
keywords:
- Windows 功能區，事件
- 功能區、事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcbfb2c6417c1423cb785b6b80de4396146535c2
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "104316615"
---
# <a name="listening-for-ribbon-events"></a><span data-ttu-id="e3658-105">接聽功能區事件</span><span class="sxs-lookup"><span data-stu-id="e3658-105">Listening for Ribbon Events</span></span>

<span data-ttu-id="e3658-106">Windows 功能區架構使用 [windows 的事件追蹤 (ETW) ](../etw/event-tracing-portal.md) 基礎結構，讓開發人員瞭解使用者如何與應用程式的功能區互動。</span><span class="sxs-lookup"><span data-stu-id="e3658-106">The Windows Ribbon framework uses the [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) infrastructure to enable developers to learn how users are interacting with their application's ribbon.</span></span>

## <a name="introduction"></a><span data-ttu-id="e3658-107">簡介</span><span class="sxs-lookup"><span data-stu-id="e3658-107">Introduction</span></span>

<span data-ttu-id="e3658-108">功能區架構事件機制的設計，是為了讓架構將功能區 UI 附隨報告到應用程式，讓您可以監視使用者活動、瞭解其互動模式，以及評估使用趨勢。</span><span class="sxs-lookup"><span data-stu-id="e3658-108">The Ribbon framework event mechanism is designed such that the framework reports ribbon UI events to the application so you can monitor user activity, learn their interaction patterns, and assess usage trends.</span></span> <span data-ttu-id="e3658-109">這項資訊可用來改善您的功能區應用程式未來反覆運算的使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="e3658-109">This information can be used to refine the user experience for future iterations of your ribbon app.</span></span>

<span data-ttu-id="e3658-110">使用功能區架構事件包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="e3658-110">Using the Ribbon framework events involves the following:</span></span>

1.  <span data-ttu-id="e3658-111">功能區應用程式必須註冊 [Windows (ETW) ](../etw/event-tracing-portal.md) 接聽程式的事件追蹤，才能從功能區架構接收功能區事件通知。</span><span class="sxs-lookup"><span data-stu-id="e3658-111">The ribbon application must register an [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) listener to receive ribbon event notifications from the Ribbon framework.</span></span>
2.  <span data-ttu-id="e3658-112">如果應用程式已 [為 Windows (ETW) ](../etw/event-tracing-portal.md) 接聽程式註冊事件追蹤，則功能區架構會在執行時間引發功能區 UI 事件回呼。</span><span class="sxs-lookup"><span data-stu-id="e3658-112">The Ribbon framework fires ribbon UI event callbacks at run time, if the application has registered an [Event Tracing for Windows (ETW)](../etw/event-tracing-portal.md) listener.</span></span>

## <a name="supported-events"></a><span data-ttu-id="e3658-113">支援的事件</span><span class="sxs-lookup"><span data-stu-id="e3658-113">Supported events</span></span>

<span data-ttu-id="e3658-114">下表說明對功能區應用程式公開的事件。</span><span class="sxs-lookup"><span data-stu-id="e3658-114">The events exposed to ribbon applications are described in the following table.</span></span> 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e3658-115">事件</span><span class="sxs-lookup"><span data-stu-id="e3658-115">Event</span></span></th>
<th><span data-ttu-id="e3658-116">附隨報告</span><span class="sxs-lookup"><span data-stu-id="e3658-116">Event report</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e3658-117">索引標籤已啟用</span><span class="sxs-lookup"><span data-stu-id="e3658-117">Tab activated</span></span></td>
<td><span data-ttu-id="e3658-118">命令 ID</span><span class="sxs-lookup"><span data-stu-id="e3658-118">Command ID</span></span><br/> <span data-ttu-id="e3658-119">命令名稱</span><span class="sxs-lookup"><span data-stu-id="e3658-119">Command name</span></span><br/> <span data-ttu-id="e3658-120">事件動詞</span><span class="sxs-lookup"><span data-stu-id="e3658-120">Event verb</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3658-121">已啟用內容索引標籤</span><span class="sxs-lookup"><span data-stu-id="e3658-121">Contextual tab activated</span></span></td>
<td><span data-ttu-id="e3658-122">命令 ID</span><span class="sxs-lookup"><span data-stu-id="e3658-122">Command ID</span></span><br/> <span data-ttu-id="e3658-123">命令名稱</span><span class="sxs-lookup"><span data-stu-id="e3658-123">Command name</span></span><br/> <span data-ttu-id="e3658-124">事件動詞</span><span class="sxs-lookup"><span data-stu-id="e3658-124">Event verb</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e3658-125">開啟的應用程式功能表</span><span class="sxs-lookup"><span data-stu-id="e3658-125">Application Menu opened</span></span></td>
<td><span data-ttu-id="e3658-126">事件動詞</span><span class="sxs-lookup"><span data-stu-id="e3658-126">Event verb</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3658-127">應用程式功能表已關閉</span><span class="sxs-lookup"><span data-stu-id="e3658-127">Application Menu closed</span></span></td>
<td><span data-ttu-id="e3658-128">事件動詞</span><span class="sxs-lookup"><span data-stu-id="e3658-128">Event verb</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e3658-129">功能表 (一般或圖庫) 開啟</span><span class="sxs-lookup"><span data-stu-id="e3658-129">Menu (regular or gallery) opened</span></span></td>
<td><span data-ttu-id="e3658-130">命令 ID</span><span class="sxs-lookup"><span data-stu-id="e3658-130">Command ID</span></span><br/> <span data-ttu-id="e3658-131">命令名稱</span><span class="sxs-lookup"><span data-stu-id="e3658-131">Command name</span></span><br/> <span data-ttu-id="e3658-132">事件動詞</span><span class="sxs-lookup"><span data-stu-id="e3658-132">Event verb</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e3658-133">QAT 功能表事件不會公開。</span><span class="sxs-lookup"><span data-stu-id="e3658-133">QAT menu events are not exposed.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3658-134"> (一般或圖庫) 關閉的功能表</span><span class="sxs-lookup"><span data-stu-id="e3658-134">Menu (regular or gallery) closed</span></span></td>
<td><span data-ttu-id="e3658-135">命令 ID</span><span class="sxs-lookup"><span data-stu-id="e3658-135">Command ID</span></span><br/> <span data-ttu-id="e3658-136">命令名稱</span><span class="sxs-lookup"><span data-stu-id="e3658-136">Command name</span></span><br/> <span data-ttu-id="e3658-137">事件動詞</span><span class="sxs-lookup"><span data-stu-id="e3658-137">Event verb</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e3658-138">QAT 功能表事件不會公開。</span><span class="sxs-lookup"><span data-stu-id="e3658-138">QAT menu events are not exposed.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e3658-139">命令</span><span class="sxs-lookup"><span data-stu-id="e3658-139">Command</span></span></td>
<td><span data-ttu-id="e3658-140">命令 ID</span><span class="sxs-lookup"><span data-stu-id="e3658-140">Command ID</span></span><br/> <span data-ttu-id="e3658-141">命令名稱</span><span class="sxs-lookup"><span data-stu-id="e3658-141">Command name</span></span><br/> <span data-ttu-id="e3658-142">事件動詞</span><span class="sxs-lookup"><span data-stu-id="e3658-142">Event verb</span></span><br/> <span data-ttu-id="e3658-143">下列其中一個事件位置：</span><span class="sxs-lookup"><span data-stu-id="e3658-143">One of the following event locations:</span></span>
<ul>
<li><span data-ttu-id="e3658-144">絲帶</span><span class="sxs-lookup"><span data-stu-id="e3658-144">RIBBON</span></span></li>
<li><span data-ttu-id="e3658-145">QUICKACCESSTOOLBAR</span><span class="sxs-lookup"><span data-stu-id="e3658-145">QUICKACCESSTOOLBAR</span></span></li>
<li><span data-ttu-id="e3658-146">APPLICATIONMENU</span><span class="sxs-lookup"><span data-stu-id="e3658-146">APPLICATIONMENU</span></span></li>
<li><span data-ttu-id="e3658-147">CONTEXTPOPUP</span><span class="sxs-lookup"><span data-stu-id="e3658-147">CONTEXTPOPUP</span></span></li>
</ul>
<br/> <span data-ttu-id="e3658-148">父命令識別碼</span><span class="sxs-lookup"><span data-stu-id="e3658-148">Parent Command ID</span></span><br/> <span data-ttu-id="e3658-149">父命令名稱</span><span class="sxs-lookup"><span data-stu-id="e3658-149">Parent Command name</span></span><br/> <span data-ttu-id="e3658-150">下列其中一種調用方法：</span><span class="sxs-lookup"><span data-stu-id="e3658-150">One of the following invoke methods:</span></span>
<ul>
<li><span data-ttu-id="e3658-151">點擊</span><span class="sxs-lookup"><span data-stu-id="e3658-151">CLICK</span></span></li>
<li><span data-ttu-id="e3658-152">KEYTIP</span><span class="sxs-lookup"><span data-stu-id="e3658-152">KEYTIP</span></span></li>
<li><span data-ttu-id="e3658-153">鍵盤</span><span class="sxs-lookup"><span data-stu-id="e3658-153">KEYBOARD</span></span></li>
<li><span data-ttu-id="e3658-154">觸摸</span><span class="sxs-lookup"><span data-stu-id="e3658-154">TOUCH</span></span></li>
</ul>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e3658-155">專案資源庫和下拉式方塊包括選取的專案索引，但不包含字串和整數值。</span><span class="sxs-lookup"><span data-stu-id="e3658-155">Item galleries and combo boxes include the selected item index but do not include string and integer values.</span></span> <span data-ttu-id="e3658-156">Spinners 不包含整數值。</span><span class="sxs-lookup"><span data-stu-id="e3658-156">Spinners do not include the integer value.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3658-157">功能區最小化</span><span class="sxs-lookup"><span data-stu-id="e3658-157">Ribbon minimized</span></span></td>
<td><span data-ttu-id="e3658-158">事件動詞</span><span class="sxs-lookup"><span data-stu-id="e3658-158">Event verb</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e3658-159">功能區展開 (展開按鈕，或按一下釘選的) </span><span class="sxs-lookup"><span data-stu-id="e3658-159">Ribbon expanded (expand button clicked or tap pinned)</span></span></td>
<td><span data-ttu-id="e3658-160">事件動詞</span><span class="sxs-lookup"><span data-stu-id="e3658-160">Event verb</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3658-161">應用程式模式切換</span><span class="sxs-lookup"><span data-stu-id="e3658-161">Application mode switched</span></span></td>
<td><span data-ttu-id="e3658-162">事件動詞</span><span class="sxs-lookup"><span data-stu-id="e3658-162">Event verb</span></span><br/> <span data-ttu-id="e3658-163">透過 <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes"><strong>SetModes</strong></a>) 設定的模式識別碼 (值</span><span class="sxs-lookup"><span data-stu-id="e3658-163">Mode ID (value set through <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes"><strong>SetModes</strong></a>)</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e3658-164">應用程式會負責將此整數解壓縮，以判斷已設定的模式。</span><span class="sxs-lookup"><span data-stu-id="e3658-164">The application is responsible for unpacking this integer to determine which modes were set.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e3658-165">顯示工具提示</span><span class="sxs-lookup"><span data-stu-id="e3658-165">Tooltip displayed</span></span></td>
<td><span data-ttu-id="e3658-166">事件動詞</span><span class="sxs-lookup"><span data-stu-id="e3658-166">Event verb</span></span><br/> <span data-ttu-id="e3658-167">父命令識別碼</span><span class="sxs-lookup"><span data-stu-id="e3658-167">Parent Command ID</span></span><br/> <span data-ttu-id="e3658-168">父命令名稱</span><span class="sxs-lookup"><span data-stu-id="e3658-168">Parent Command name</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="e3658-169">相關主題</span><span class="sxs-lookup"><span data-stu-id="e3658-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3658-170">Windows 功能區架構開發人員指南</span><span class="sxs-lookup"><span data-stu-id="e3658-170">Windows Ribbon Framework Developer Guides</span></span>](windowsribbon-guides-entry.md)
</dt> <dt>

[<span data-ttu-id="e3658-171">使用功能區標記宣告命令和控制項</span><span class="sxs-lookup"><span data-stu-id="e3658-171">Declaring Commands and Controls with Ribbon Markup</span></span>](./windowsribbon-schema.md)
</dt> <dt>

[<span data-ttu-id="e3658-172">功能區使用者體驗指導方針</span><span class="sxs-lookup"><span data-stu-id="e3658-172">Ribbon User Experience Guidelines</span></span>](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[<span data-ttu-id="e3658-173">功能區設計流程</span><span class="sxs-lookup"><span data-stu-id="e3658-173">Ribbon Design Process</span></span>](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

