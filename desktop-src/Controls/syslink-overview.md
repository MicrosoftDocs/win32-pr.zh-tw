---
title: 關於 SysLink 控制項
description: SysLink 控制項是一種視窗，會轉譯標記的文字，並在使用者按一下其內嵌超連結時通知應用程式。 此控制項提供使用 [命令連結] 按鈕的方便替代方法。 如需詳細資訊，請參閱按鈕類型。
ms.assetid: 38cfac3d-de60-4882-a434-4f498330b77d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deb0d15cac479b844b0ea8510c34cc57f56822be
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024157"
---
# <a name="about-syslink-controls"></a><span data-ttu-id="e1cfc-105">關於 SysLink 控制項</span><span class="sxs-lookup"><span data-stu-id="e1cfc-105">About SysLink Controls</span></span>

<span data-ttu-id="e1cfc-106">SysLink 控制項是一種視窗，會轉譯標記的文字，並在使用者按一下其內嵌超連結時通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="e1cfc-106">A SysLink control is a window that renders marked-up text, and notifies the application when users click its embedded hyperlinks.</span></span> <span data-ttu-id="e1cfc-107">此控制項提供使用 [ [**命令連結] 按鈕**](button-styles.md)的方便替代方法。</span><span class="sxs-lookup"><span data-stu-id="e1cfc-107">This control provides a convenient alternative to using the [**Command link button**](button-styles.md).</span></span> <span data-ttu-id="e1cfc-108">如需詳細資訊，請參閱 [按鈕類型](button-types-and-styles.md)。</span><span class="sxs-lookup"><span data-stu-id="e1cfc-108">For more information, see [Button Types](button-types-and-styles.md).</span></span>

<span data-ttu-id="e1cfc-109">每個 SysLink 控制項都可以支援多個超連結，而且您可以透過以零為基底的索引來存取每個超連結。</span><span class="sxs-lookup"><span data-stu-id="e1cfc-109">Each SysLink control can support multiple hyperlinks, and you can access each hyperlink through a zero-based index.</span></span> <span data-ttu-id="e1cfc-110">SysLink 控制項是在 ComCtl32.dll 第6版中定義，而且需要資訊清單或指示詞，指定應該使用第6版的 DLL （如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="e1cfc-110">The SysLink control is defined in the ComCtl32.dll version 6, and it requires a manifest or directive that specifies that version 6 of the DLL should be used if it is available.</span></span> <span data-ttu-id="e1cfc-111">如需詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="e1cfc-111">For more information, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

<span data-ttu-id="e1cfc-112">本文包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="e1cfc-112">This article contains the following sections.</span></span>

-   [<span data-ttu-id="e1cfc-113">SysLink 標記</span><span class="sxs-lookup"><span data-stu-id="e1cfc-113">SysLink Markup</span></span>](#syslink-markup)
-   [<span data-ttu-id="e1cfc-114">連結屬性</span><span class="sxs-lookup"><span data-stu-id="e1cfc-114">Link Attributes</span></span>](#link-attributes)
-   [<span data-ttu-id="e1cfc-115">連結狀態</span><span class="sxs-lookup"><span data-stu-id="e1cfc-115">Link States</span></span>](#link-states)
-   [<span data-ttu-id="e1cfc-116">雙向文字顯示的限制</span><span class="sxs-lookup"><span data-stu-id="e1cfc-116">Limitations on Bidirectional Text Display</span></span>](#limitations-on-bidirectional-text-display)

## <a name="syslink-markup"></a><span data-ttu-id="e1cfc-117">SysLink 標記</span><span class="sxs-lookup"><span data-stu-id="e1cfc-117">SysLink Markup</span></span>

<span data-ttu-id="e1cfc-118">SysLink 控制項支援 () 的錨點 &lt; 標記 &gt; 以及屬性 **HREF** 和 **ID**。</span><span class="sxs-lookup"><span data-stu-id="e1cfc-118">The SysLink control supports the anchor tag(&lt;a&gt;) along with the attributes **HREF** and **ID**.</span></span> <span data-ttu-id="e1cfc-119">**HREF** 可以是任何通訊協定，例如 HTTP、ftp 和 mailto。</span><span class="sxs-lookup"><span data-stu-id="e1cfc-119">An **HREF** can be any protocol, such as http, ftp, and mailto.</span></span> <span data-ttu-id="e1cfc-120">**識別碼** 是選擇性的名稱，在 SysLink 控制項內是唯一的，而且與個別連結相關聯。</span><span class="sxs-lookup"><span data-stu-id="e1cfc-120">An **ID** is an optional name, unique within a SysLink control, and it is associated with an individual link.</span></span> <span data-ttu-id="e1cfc-121">連結也會根據其在字串中的位置，指派以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="e1cfc-121">Links are also assigned a zero-based index according to their position within the string.</span></span> <span data-ttu-id="e1cfc-122">此索引是用來存取連結。</span><span class="sxs-lookup"><span data-stu-id="e1cfc-122">This index is used to access a link.</span></span>

## <a name="link-attributes"></a><span data-ttu-id="e1cfc-123">連結屬性</span><span class="sxs-lookup"><span data-stu-id="e1cfc-123">Link Attributes</span></span>

<span data-ttu-id="e1cfc-124">每個連結的屬性都可以在每個連結的錨點標記內設定，或藉由傳送 [**LM \_ SETITEM**](lm-setitem.md) 訊息來設定。</span><span class="sxs-lookup"><span data-stu-id="e1cfc-124">Each link's attributes can be set either within the anchor tag for each link or by sending the [**LM\_SETITEM**](lm-setitem.md) message.</span></span> <span data-ttu-id="e1cfc-125">藉由在初始化字串內指定屬性來設定屬性，只會初始化該值。</span><span class="sxs-lookup"><span data-stu-id="e1cfc-125">Setting an attribute by specifying it within the initialization string merely initializes the value.</span></span> <span data-ttu-id="e1cfc-126">您可以透過後續使用 **LM \_ SETITEM** 訊息來變更屬性的值。</span><span class="sxs-lookup"><span data-stu-id="e1cfc-126">You can change the value of an attribute through subsequent use of the **LM\_SETITEM** message.</span></span>

## <a name="link-states"></a><span data-ttu-id="e1cfc-127">連結狀態</span><span class="sxs-lookup"><span data-stu-id="e1cfc-127">Link States</span></span>

<span data-ttu-id="e1cfc-128">連結專案可以是三種狀態的其中一種，以下表中的旗標表示。</span><span class="sxs-lookup"><span data-stu-id="e1cfc-128">Link items can be in any one of three states, represented by the flags in the following table.</span></span>



| <span data-ttu-id="e1cfc-129">狀態旗標</span><span class="sxs-lookup"><span data-stu-id="e1cfc-129">State flag</span></span>   | <span data-ttu-id="e1cfc-130">外觀和意義</span><span class="sxs-lookup"><span data-stu-id="e1cfc-130">Appearance and meaning</span></span>                                            |
|--------------|-------------------------------------------------------------------|
| <span data-ttu-id="e1cfc-131">以 .LIS 為 \_ 焦點</span><span class="sxs-lookup"><span data-stu-id="e1cfc-131">LIS\_FOCUSED</span></span> | <span data-ttu-id="e1cfc-132">此連結具有鍵盤焦點，按下 Enter 會啟用它。</span><span class="sxs-lookup"><span data-stu-id="e1cfc-132">The link has the keyboard focus, and pressing Enter activates it.</span></span> |
| <span data-ttu-id="e1cfc-133">\_已啟用 .LIS</span><span class="sxs-lookup"><span data-stu-id="e1cfc-133">LIS\_ENABLED</span></span> | <span data-ttu-id="e1cfc-134">連結已啟用。</span><span class="sxs-lookup"><span data-stu-id="e1cfc-134">The link is enabled.</span></span>                                              |
| <span data-ttu-id="e1cfc-135">已 \_ 造訪的 .LIS</span><span class="sxs-lookup"><span data-stu-id="e1cfc-135">LIS\_VISITED</span></span> | <span data-ttu-id="e1cfc-136">使用者已流覽過連結所代表的 URL。</span><span class="sxs-lookup"><span data-stu-id="e1cfc-136">The user has already visited the URL represented by the link.</span></span>     |



 

## <a name="limitations-on-bidirectional-text-display"></a><span data-ttu-id="e1cfc-137">雙向文字顯示的限制</span><span class="sxs-lookup"><span data-stu-id="e1cfc-137">Limitations on Bidirectional Text Display</span></span>

<span data-ttu-id="e1cfc-138">某些語言（例如阿拉伯文或希伯來文）是由右至左寫入 (RTL) ;英文是由左至右 (LTR) 撰寫。</span><span class="sxs-lookup"><span data-stu-id="e1cfc-138">Some languages, such as Arabic or Hebrew, are written right-to-left (RTL); English is written left-to-right (LTR).</span></span> <span data-ttu-id="e1cfc-139">將 RTL 與 LTR 合併稱為雙向文字。</span><span class="sxs-lookup"><span data-stu-id="e1cfc-139">Combining RTL with LTR is called bidirectional text.</span></span> <span data-ttu-id="e1cfc-140">將 LTR 和 RTL Unicode 或 HTML 方向標記結構混合在資源字串中，做為控制字元串流程的雙向流程標記，在使用 SysLink 控制項時，可能不會產生預期的結果。</span><span class="sxs-lookup"><span data-stu-id="e1cfc-140">Mixing LTR and RTL Unicode or HTML directional markup constructs in resource strings, as bidirectional flow markers to control the flow of strings, may not produce the expected result when using a SysLink control.</span></span> <span data-ttu-id="e1cfc-141">例如，LTR 標記的句子可能無法在 RTL 內容中正確顯示。</span><span class="sxs-lookup"><span data-stu-id="e1cfc-141">For instance, an LTR-marked sentence may not display correctly in RTL context.</span></span>

> [!Note]  
> <span data-ttu-id="e1cfc-142">在所有情況下，SysLink 控制項不支援雙向顯示。</span><span class="sxs-lookup"><span data-stu-id="e1cfc-142">SysLink controls do not support bidirectional display under all scenarios.</span></span> <span data-ttu-id="e1cfc-143">只有當您知道簡單的 LTR 或 RTL 配置已足夠時，才使用 SysLink 控制項。</span><span class="sxs-lookup"><span data-stu-id="e1cfc-143">Use a SysLink control only if you know that a simple LTR or RTL layout is adequate.</span></span> <span data-ttu-id="e1cfc-144">否則，請考慮使用更先進的技術，例如 [MSHTML](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753630(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="e1cfc-144">Otherwise, consider using a more advanced technology such as [MSHTML](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753630(v=vs.85)).</span></span>

 

 

 