---
title: 'LVM_GETISEARCHSTRING 訊息 (Commctrl .h) '
description: 抓取清單視圖控制項的遞增搜尋字串。 您可以明確地傳送此訊息，或使用 ListView \_ GetISearchString 宏來傳送。
ms.assetid: e953c4a0-0556-4987-8abf-3276e787fe49
keywords:
- LVM_GETISEARCHSTRING message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETISEARCHSTRING
- LVM_GETISEARCHSTRINGA
- LVM_GETISEARCHSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9040cf96c5c483b29764b1ccfb67e0e4fff3f897
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466513"
---
# <a name="lvm_getisearchstring-message"></a><span data-ttu-id="6906a-105">LVM \_ GETISEARCHSTRING 訊息</span><span class="sxs-lookup"><span data-stu-id="6906a-105">LVM\_GETISEARCHSTRING message</span></span>

<span data-ttu-id="6906a-106">抓取清單視圖控制項的遞增搜尋字串。</span><span class="sxs-lookup"><span data-stu-id="6906a-106">Retrieves the incremental search string of a list-view control.</span></span> <span data-ttu-id="6906a-107">您可以明確地傳送此訊息，或使用 [**ListView \_ GetISearchString**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getisearchstring) 宏來傳送。</span><span class="sxs-lookup"><span data-stu-id="6906a-107">You can send this message explicitly or by using the [**ListView\_GetISearchString**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getisearchstring) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6906a-108">參數</span><span class="sxs-lookup"><span data-stu-id="6906a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6906a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6906a-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6906a-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="6906a-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6906a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6906a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6906a-112">接收累加式搜尋字串的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="6906a-112">Pointer to a buffer that receives the incremental search string.</span></span> <span data-ttu-id="6906a-113">若要只取出字串的長度，請將 *lParam* 設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="6906a-113">To just retrieve the length of the string, set *lParam* to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6906a-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="6906a-114">Return value</span></span>

<span data-ttu-id="6906a-115">傳回累加式搜尋字串中的字元數，不包括結束的 Null 字元，或如果清單視圖控制項不在累加式搜尋模式中，則為零。</span><span class="sxs-lookup"><span data-stu-id="6906a-115">Returns the number of characters in the incremental search string, not including the terminating NULL character, or zero if the list-view control is not in incremental search mode.</span></span>

## <a name="remarks"></a><span data-ttu-id="6906a-116">備註</span><span class="sxs-lookup"><span data-stu-id="6906a-116">Remarks</span></span>

<span data-ttu-id="6906a-117">**安全性警告：** 不當使用此訊息可能會危及程式的安全性。</span><span class="sxs-lookup"><span data-stu-id="6906a-117">**Security Warning:** Using this message incorrectly might compromise the security of your program.</span></span> <span data-ttu-id="6906a-118">此訊息不會提供您知道緩衝區大小的方法。</span><span class="sxs-lookup"><span data-stu-id="6906a-118">This message does not provide a way for you to know the size of the buffer.</span></span> <span data-ttu-id="6906a-119">如果您使用此訊息，請先呼叫在 *lParam* 中傳遞 **null** 的訊息，這會傳回字元數，但不包括需要的 **null** 。</span><span class="sxs-lookup"><span data-stu-id="6906a-119">If you use this message, first call the message passing **NULL** in the *lParam*, this returns the number of characters, excluding **NULL** that are required.</span></span> <span data-ttu-id="6906a-120">然後第二次呼叫訊息以抓取字串。</span><span class="sxs-lookup"><span data-stu-id="6906a-120">Then call the message a second time to retrieve the string.</span></span> <span data-ttu-id="6906a-121">您應該先複習 [安全性考慮： Microsoft Windows 控制項](sec-comctls.md) ，再繼續進行。</span><span class="sxs-lookup"><span data-stu-id="6906a-121">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

<span data-ttu-id="6906a-122">*增量搜尋字串* 是使用者輸入的字元序列，而清單視圖則具有輸入焦點。</span><span class="sxs-lookup"><span data-stu-id="6906a-122">The *incremental search string* is the character sequence that the user types while the list view has the input focus.</span></span> <span data-ttu-id="6906a-123">每次使用者輸入一個字元時，系統會將字元附加到搜尋字串，然後搜尋相符的專案。</span><span class="sxs-lookup"><span data-stu-id="6906a-123">Each time the user types a character, the system appends the character to the search string and then searches for a matching item.</span></span> <span data-ttu-id="6906a-124">如果系統找到相符專案，則會選取專案，並視需要將它滾動至 view。</span><span class="sxs-lookup"><span data-stu-id="6906a-124">If the system finds a match, it selects the item and, if necessary, scrolls it into view.</span></span>

<span data-ttu-id="6906a-125">超時期間是與使用者輸入的每個字元相關聯。</span><span class="sxs-lookup"><span data-stu-id="6906a-125">A time-out period is associated with each character that the user types.</span></span> <span data-ttu-id="6906a-126">如果在使用者鍵入另一個字元之前經過超時時間，則會重設增量搜尋字串。</span><span class="sxs-lookup"><span data-stu-id="6906a-126">If the time-out period elapses before the user types another character, the incremental search string is reset.</span></span>

<span data-ttu-id="6906a-127">請確定緩衝區夠大，足以容納字串和終止的 Null 字元。</span><span class="sxs-lookup"><span data-stu-id="6906a-127">Make sure that the buffer is large enough to hold the string and the terminating NULL character.</span></span> <span data-ttu-id="6906a-128">如果太小，則會產生立即不正確分頁錯誤。</span><span class="sxs-lookup"><span data-stu-id="6906a-128">If it is too small, an immediate invalid page fault will result.</span></span>

## <a name="requirements"></a><span data-ttu-id="6906a-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="6906a-129">Requirements</span></span>



| <span data-ttu-id="6906a-130">需求</span><span class="sxs-lookup"><span data-stu-id="6906a-130">Requirement</span></span> | <span data-ttu-id="6906a-131">值</span><span class="sxs-lookup"><span data-stu-id="6906a-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6906a-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6906a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6906a-133">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6906a-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6906a-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6906a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6906a-135">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6906a-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6906a-136">標頭</span><span class="sxs-lookup"><span data-stu-id="6906a-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="6906a-137"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="6906a-137"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="6906a-138">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="6906a-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6906a-139">**LVM \_GETISEARCHSTRINGW** (Unicode) 和 **LVM \_ GETISEARCHSTRINGA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="6906a-139">**LVM\_GETISEARCHSTRINGW** (Unicode) and **LVM\_GETISEARCHSTRINGA** (ANSI)</span></span><br/> |



 

 





