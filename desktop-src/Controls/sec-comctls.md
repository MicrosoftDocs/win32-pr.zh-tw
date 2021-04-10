---
title: Microsoft Windows 控制項安全性考慮
description: 本主題提供與 Windows 控制項相關之安全性考慮的資訊。
ms.assetid: d5396fa1-452e-40e1-beaf-ae04690048f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e29ba986ddd1db980134f428c8abf152321617ef
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "104093459"
---
# <a name="security-considerations-microsoft-windows-controls"></a><span data-ttu-id="626ae-103">安全性考慮： Microsoft Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="626ae-103">Security Considerations: Microsoft Windows Controls</span></span>

<span data-ttu-id="626ae-104">本主題提供與 Windows 控制項相關之安全性考慮的資訊。</span><span class="sxs-lookup"><span data-stu-id="626ae-104">This topic provides information about security considerations related to the Windows controls.</span></span> <span data-ttu-id="626ae-105">本主題中的資訊並不提供您需要瞭解的安全性問題，請使用它作為此技術領域的起點和參考。</span><span class="sxs-lookup"><span data-stu-id="626ae-105">The information in this topic does not provide all you need to know about security issues—use it as a starting point and reference for this technology area.</span></span>

<span data-ttu-id="626ae-106">電腦之間的互連能力很常見;開發人員的主要考慮必須是應用程式安全性。</span><span class="sxs-lookup"><span data-stu-id="626ae-106">Interconnectivity among computers is common; a developer's chief concern must be application security.</span></span> <span data-ttu-id="626ae-107">下列各節將討論在撰寫 Windows 控制項的程式設計時應考慮的一些潛在安全性問題。</span><span class="sxs-lookup"><span data-stu-id="626ae-107">The following sections discuss some potential security issues to consider when programming Windows controls.</span></span>

-   [<span data-ttu-id="626ae-108">以 Null 終止的控制訊息</span><span class="sxs-lookup"><span data-stu-id="626ae-108">Null-terminated Control Messages</span></span>](#null-terminated-control-messages)
-   [<span data-ttu-id="626ae-109">字串使用</span><span class="sxs-lookup"><span data-stu-id="626ae-109">String Use</span></span>](#string-use)
-   [<span data-ttu-id="626ae-110">輸入驗證</span><span class="sxs-lookup"><span data-stu-id="626ae-110">Input Validation</span></span>](#input-validation)
-   [<span data-ttu-id="626ae-111">密碼使用</span><span class="sxs-lookup"><span data-stu-id="626ae-111">Password Use</span></span>](#password-use)
-   [<span data-ttu-id="626ae-112">安全性警示</span><span class="sxs-lookup"><span data-stu-id="626ae-112">Security Alerts</span></span>](#security-alerts)
-   [<span data-ttu-id="626ae-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="626ae-113">Related topics</span></span>](#related-topics)

## <a name="null-terminated-control-messages"></a><span data-ttu-id="626ae-114">以 Null 終止的控制訊息</span><span class="sxs-lookup"><span data-stu-id="626ae-114">Null-terminated Control Messages</span></span>

<span data-ttu-id="626ae-115">許多控制訊息和宏都有字串參數。</span><span class="sxs-lookup"><span data-stu-id="626ae-115">Many of the control messages and macros have string parameters.</span></span> <span data-ttu-id="626ae-116">這些訊息通常不會驗證輸入字串，尤其是它們不會檢查是否有終止 `'\0'` 。</span><span class="sxs-lookup"><span data-stu-id="626ae-116">Often these messages do not validate the input strings, in particular, they do not check for a terminating `'\0'`.</span></span> <span data-ttu-id="626ae-117">當您呼叫使用字串作為參數的訊息時，請明確指定字串為以 null 結束。</span><span class="sxs-lookup"><span data-stu-id="626ae-117">When you call a message that uses a string as a parameter, explicitly specify that the string is null-terminated.</span></span>

## <a name="string-use"></a><span data-ttu-id="626ae-118">字串使用</span><span class="sxs-lookup"><span data-stu-id="626ae-118">String Use</span></span>

<span data-ttu-id="626ae-119">當您編寫 Windows 控制項的程式時，必須操作字串。</span><span class="sxs-lookup"><span data-stu-id="626ae-119">When you program Windows controls, it is necessary to manipulate strings.</span></span> <span data-ttu-id="626ae-120">幾乎每個控制項都需要插入文字。</span><span class="sxs-lookup"><span data-stu-id="626ae-120">Almost every control requires text to be inserted.</span></span> <span data-ttu-id="626ae-121">例如，若要填入清單方塊，您必須將字串載入控制項。</span><span class="sxs-lookup"><span data-stu-id="626ae-121">For example, to populate a list box you must load strings into the control.</span></span> <span data-ttu-id="626ae-122">因為使用字串不正確通常會造成緩衝區溢位，請採取預防措施以避免此安全性風險。</span><span class="sxs-lookup"><span data-stu-id="626ae-122">Because using strings incorrectly often causes buffer overruns, take precautions to avoid this security risk.</span></span>

<span data-ttu-id="626ae-123">For more information about buffer overruns, see *Writing Secure Code* by Michael Howard and David LeBlanc, Microsoft Press, 2002 and [Best Practices for the Security APIs](/windows/desktop/SecBP/best-practices-for-the-security-apis).</span><span class="sxs-lookup"><span data-stu-id="626ae-123">For more information about buffer overruns, see *Writing Secure Code* by Michael Howard and David LeBlanc, Microsoft Press, 2002 and [Best Practices for the Security APIs](/windows/desktop/SecBP/best-practices-for-the-security-apis).</span></span>

## <a name="input-validation"></a><span data-ttu-id="626ae-124">輸入驗證</span><span class="sxs-lookup"><span data-stu-id="626ae-124">Input Validation</span></span>

<span data-ttu-id="626ae-125">下列控制訊息可能會出現安全性問題。</span><span class="sxs-lookup"><span data-stu-id="626ae-125">The following control messages can present security problems.</span></span>

-   [<span data-ttu-id="626ae-126">**CB \_ GETLBTEXT**</span><span class="sxs-lookup"><span data-stu-id="626ae-126">**CB\_GETLBTEXT**</span></span>](cb-getlbtext.md)
-   [<span data-ttu-id="626ae-127">**LVM \_ GETISEARCHSTRING**</span><span class="sxs-lookup"><span data-stu-id="626ae-127">**LVM\_GETISEARCHSTRING**</span></span>](lvm-getisearchstring.md)
-   [<span data-ttu-id="626ae-128">**SB \_ GETTEXT**</span><span class="sxs-lookup"><span data-stu-id="626ae-128">**SB\_GETTEXT**</span></span>](sb-gettext.md)
-   [<span data-ttu-id="626ae-129">**SB \_ GETTIPTEXT**</span><span class="sxs-lookup"><span data-stu-id="626ae-129">**SB\_GETTIPTEXT**</span></span>](sb-gettiptext.md)
-   [<span data-ttu-id="626ae-130">**TB \_ GETBUTTONTEXT**</span><span class="sxs-lookup"><span data-stu-id="626ae-130">**TB\_GETBUTTONTEXT**</span></span>](tb-getbuttontext.md)
-   [<span data-ttu-id="626ae-131">**TTM \_ GETTEXT**</span><span class="sxs-lookup"><span data-stu-id="626ae-131">**TTM\_GETTEXT**</span></span>](ttm-gettext.md)
-   [<span data-ttu-id="626ae-132">**TVM \_ GETISEARCHSTRING**</span><span class="sxs-lookup"><span data-stu-id="626ae-132">**TVM\_GETISEARCHSTRING**</span></span>](tvm-getisearchstring.md)

<span data-ttu-id="626ae-133">如果文字在呼叫之間變更，以取得文字長度以及文字顯示或使用的時間，則可能會發生緩衝區溢位。</span><span class="sxs-lookup"><span data-stu-id="626ae-133">If the text changes between the call to get the text length and the time the text is displayed or used, a buffer overrun can occur.</span></span> <span data-ttu-id="626ae-134">若要避免這種情況，您必須在使用之前先驗證字串。</span><span class="sxs-lookup"><span data-stu-id="626ae-134">To avoid this, you must validate the string before using it.</span></span> <span data-ttu-id="626ae-135">此外，抓取文字、 [**CB \_ GETLBTEXT**](cb-getlbtext.md)、 [**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md)和 [**TTM \_ GETTEXT**](ttm-gettext.md)的訊息沒有任何緩衝區大小參數，可呈現緩衝區溢位的可能性。</span><span class="sxs-lookup"><span data-stu-id="626ae-135">In addition, the messages that retrieve text, [**CB\_GETLBTEXT**](cb-getlbtext.md), [**TB\_GETBUTTONTEXT**](tb-getbuttontext.md), and [**TTM\_GETTEXT**](ttm-gettext.md), have no buffer size parameter that presents the potential for a buffer overrun.</span></span>

<span data-ttu-id="626ae-136">當您使用 [**cb \_ GETLBTEXT**](cb-getlbtext.md) 或 [**sb \_ GETTEXT**](sb-gettext.md)時，您應該先呼叫 [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md) 或 [**sb \_ GETTEXTLENGTH**](sb-gettextlength.md) 來取得緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="626ae-136">When you use [**CB\_GETLBTEXT**](cb-getlbtext.md) or [**SB\_GETTEXT**](sb-gettext.md), you should first call [**CB\_GETLBTEXTLEN**](cb-getlbtextlen.md) or [**SB\_GETTEXTLENGTH**](sb-gettextlength.md) to obtain the buffer size.</span></span> <span data-ttu-id="626ae-137">其中有些訊息、 [**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md)、 [**LVM \_ GETISEARCHSTRING**](lvm-getisearchstring.md)和 [**TVM \_ GETISEARCHSTRING**](tvm-getisearchstring.md)可以使用 **Null** 參數值來呼叫，以取得字串的長度，然後再叫用訊息來取得字串。</span><span class="sxs-lookup"><span data-stu-id="626ae-137">Some of these messages, [**TB\_GETBUTTONTEXT**](tb-getbuttontext.md), [**LVM\_GETISEARCHSTRING**](lvm-getisearchstring.md), and [**TVM\_GETISEARCHSTRING**](tvm-getisearchstring.md), can be called with a **NULL** parameter value to obtain the length of the string before invoking the message to retrieve the string.</span></span>

<span data-ttu-id="626ae-138">您應該特別注意的訊息是狀態列 [**SB \_ GETTIPTEXT**](sb-gettiptext.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="626ae-138">A message that you should pay particular attention to is the status bar [**SB\_GETTIPTEXT**](sb-gettiptext.md) message.</span></span> <span data-ttu-id="626ae-139">此訊息不會提供任何方法來查詢要抓取之字串的長度。</span><span class="sxs-lookup"><span data-stu-id="626ae-139">This message provides no way to query the length of the string that is to be retrieved.</span></span>

## <a name="password-use"></a><span data-ttu-id="626ae-140">密碼使用</span><span class="sxs-lookup"><span data-stu-id="626ae-140">Password Use</span></span>

<span data-ttu-id="626ae-141">如果您使用密碼保護的編輯控制項 ([**ES \_ 密碼**](edit-control-styles.md) 樣式) ，包含所抓取文字的緩衝區必須儘快設定為零，以避免在記憶體中公開使用者的密碼。</span><span class="sxs-lookup"><span data-stu-id="626ae-141">If you use password-protected edit controls ([**ES\_PASSWORD**](edit-control-styles.md) style), the buffer that contains the retrieved text must be set to zero as soon as possible to avoid exposing the user's password in memory.</span></span>

## <a name="security-alerts"></a><span data-ttu-id="626ae-142">安全性警示</span><span class="sxs-lookup"><span data-stu-id="626ae-142">Security Alerts</span></span>

<span data-ttu-id="626ae-143">下表列出如果使用不當，可能會危及應用程式安全性的功能。</span><span class="sxs-lookup"><span data-stu-id="626ae-143">The following table lists features that, if used incorrectly, can compromise the security of your applications.</span></span> <span data-ttu-id="626ae-144">此處所列的訊息不會提供指定緩衝區大小的參數。</span><span class="sxs-lookup"><span data-stu-id="626ae-144">The messages listed here do not provide a parameter that specifies the buffer size.</span></span>



| <span data-ttu-id="626ae-145">功能</span><span class="sxs-lookup"><span data-stu-id="626ae-145">Feature</span></span>                                               | <span data-ttu-id="626ae-146">降低</span><span class="sxs-lookup"><span data-stu-id="626ae-146">Mitigation</span></span>                                                                                                                                              |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="626ae-147">**DlgDirListComboBox**</span><span class="sxs-lookup"><span data-stu-id="626ae-147">**DlgDirListComboBox**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dlgdirlistcomboboxa)      | <span data-ttu-id="626ae-148">請確定函式所使用的緩衝區可以寫入，而且是以 null 結束。</span><span class="sxs-lookup"><span data-stu-id="626ae-148">Make sure the buffer used by the function can be written to and is null-terminated.</span></span>                                                                     |
| [<span data-ttu-id="626ae-149">**CB \_ GETLBTEXT**</span><span class="sxs-lookup"><span data-stu-id="626ae-149">**CB\_GETLBTEXT**</span></span>](cb-getlbtext.md)                 | <span data-ttu-id="626ae-150">呼叫 [**cb \_ GETLBTEXTLEN**](cb-getlbtextlen.md) 以取得緩衝區大小，然後呼叫 [**cb \_ GETLBTEXT**](cb-getlbtext.md) 來取出字串。</span><span class="sxs-lookup"><span data-stu-id="626ae-150">Call [**CB\_GETLBTEXTLEN**](cb-getlbtextlen.md) to obtain the buffer size, and then call [**CB\_GETLBTEXT**](cb-getlbtext.md) to retrieve the string.</span></span> |
| [<span data-ttu-id="626ae-151">**LVM \_ GETISEARCHSTRING**</span><span class="sxs-lookup"><span data-stu-id="626ae-151">**LVM\_GETISEARCHSTRING**</span></span>](lvm-getisearchstring.md) | <span data-ttu-id="626ae-152">呼叫具有 **Null** 參數值的訊息，以取得緩衝區大小，然後再次呼叫訊息以取得字串。</span><span class="sxs-lookup"><span data-stu-id="626ae-152">Call the message with a **NULL** parameter value to obtain the buffer size, and then call the message a second time to retrieve the string.</span></span>             |
| [<span data-ttu-id="626ae-153">**SB \_ GETTEXT**</span><span class="sxs-lookup"><span data-stu-id="626ae-153">**SB\_GETTEXT**</span></span>](sb-gettext.md)                     | <span data-ttu-id="626ae-154">呼叫 [**sb \_ GETTEXTLENGTH**](sb-gettextlength.md) 來取得緩衝區大小，然後呼叫 [**sb \_ GETTEXT**](sb-gettext.md) 來取出字串。</span><span class="sxs-lookup"><span data-stu-id="626ae-154">Call [**SB\_GETTEXTLENGTH**](sb-gettextlength.md) to obtain the buffer size, and then call [**SB\_GETTEXT**](sb-gettext.md) to retrieve the string.</span></span>   |
| [<span data-ttu-id="626ae-155">**TB \_ GETBUTTONTEXT**</span><span class="sxs-lookup"><span data-stu-id="626ae-155">**TB\_GETBUTTONTEXT**</span></span>](tb-getbuttontext.md)         | <span data-ttu-id="626ae-156">呼叫具有 **Null** 參數值的訊息，以取得緩衝區大小，然後再次呼叫訊息以取得字串。</span><span class="sxs-lookup"><span data-stu-id="626ae-156">Call the message with a **NULL** parameter value to obtain the buffer size, and then call the message a second time to retrieve the string.</span></span>             |
| [<span data-ttu-id="626ae-157">**TTM \_ GETTEXT**</span><span class="sxs-lookup"><span data-stu-id="626ae-157">**TTM\_GETTEXT**</span></span>](ttm-gettext.md)                   | <span data-ttu-id="626ae-158">此訊息不會提供您知道或指定緩衝區大小的方法。</span><span class="sxs-lookup"><span data-stu-id="626ae-158">This message does not provide a way for you to know or specify the size of the buffer.</span></span>                                                                  |
| [<span data-ttu-id="626ae-159">**TVM \_ GETISEARCHSTRING**</span><span class="sxs-lookup"><span data-stu-id="626ae-159">**TVM\_GETISEARCHSTRING**</span></span>](tvm-getisearchstring.md) | <span data-ttu-id="626ae-160">傳遞 **Null** 參數值以取得緩衝區大小，然後再次呼叫訊息以取得字串，藉以呼叫訊息。</span><span class="sxs-lookup"><span data-stu-id="626ae-160">Call the message by passing a **NULL** parameter value to obtain the buffer size, and then call the message a second time to retrieve the string.</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="626ae-161">相關主題</span><span class="sxs-lookup"><span data-stu-id="626ae-161">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="626ae-162">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="626ae-162">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="626ae-163">Microsoft 安全性</span><span class="sxs-lookup"><span data-stu-id="626ae-163">Microsoft Security</span></span>](https://www.microsoft.com/security/default.aspx)
</dt> <dt>

[<span data-ttu-id="626ae-164">安全性</span><span class="sxs-lookup"><span data-stu-id="626ae-164">Security</span></span>](/windows/desktop/security)
</dt> <dt>

[<span data-ttu-id="626ae-165">TechNet 安全性資源</span><span class="sxs-lookup"><span data-stu-id="626ae-165">TechNet Security Resources</span></span>](https://www.microsoft.com/technet/security/Bulletin/MS10-059.mspx)
</dt> <dt>

[<span data-ttu-id="626ae-166">安全性 Api 的最佳作法</span><span class="sxs-lookup"><span data-stu-id="626ae-166">Best Practices for the Security APIs</span></span>](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> </dl>

 

 