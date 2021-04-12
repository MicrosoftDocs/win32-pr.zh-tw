---
title: WM_ADSPROP_SHEET_CREATE 訊息
description: 傳送至通知物件，以在 Active Directory MMC 嵌入式管理單元中建立次要屬性工作表。
ms.assetid: 3efa25f2-cd39-44f8-952e-203f1519ce2c
ms.tgt_platform: multiple
keywords:
- WM_ADSPROP_SHEET_CREATE 訊息 Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_SHEET_CREATE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b540ffd87d4350a323577ff5fa317e94f9271f2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508615"
---
# <a name="wm_adsprop_sheet_create-message"></a><span data-ttu-id="539a2-104">WM \_ ADSPROP \_ 工作表 \_ 建立訊息</span><span class="sxs-lookup"><span data-stu-id="539a2-104">WM\_ADSPROP\_SHEET\_CREATE message</span></span>

<span data-ttu-id="539a2-105">會將 **WM \_ ADSPROP \_ 工作表 \_ 建立** 訊息傳送至通知物件，以在 Active Directory MMC 嵌入式管理單元中建立次要屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="539a2-105">The **WM\_ADSPROP\_SHEET\_CREATE** message is sent to the notification object to create a secondary property sheet in an Active Directory MMC snap-in.</span></span>

> [!Note]  
> <span data-ttu-id="539a2-106">這個訊息值未定義于已發行的標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="539a2-106">This message value is not defined in a published header file.</span></span> <span data-ttu-id="539a2-107">若要使用這個訊息值，您必須以所示的確切格式來定義它。</span><span class="sxs-lookup"><span data-stu-id="539a2-107">To use this message value, you must define it yourself in the exact format shown.</span></span>

 


```C++
#define WM_ADSPROP_SHEET_CREATE (WM_USER + 1108)
LRESULT SendMessage( (HWND)   hwnd, 
                     (UINT)   WM_ADSPROP_SHEET_CREATE,
                     (WPARAM) wParam, 
                     (LPARAM) lParam);
```



## <a name="parameters"></a><span data-ttu-id="539a2-108">參數</span><span class="sxs-lookup"><span data-stu-id="539a2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="539a2-109">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="539a2-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="539a2-110">通知物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="539a2-110">The handle of the notification object.</span></span> <span data-ttu-id="539a2-111">若要取得此控制碼，請呼叫 [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj)。</span><span class="sxs-lookup"><span data-stu-id="539a2-111">To obtain this handle, call [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> <dt>

<span data-ttu-id="539a2-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="539a2-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="539a2-113">包含 [**DSA \_ SEC \_ 頁面 \_ 資訊**](dsa-sec-page-info.md) 結構的指標，此結構會定義要建立的次要頁面。</span><span class="sxs-lookup"><span data-stu-id="539a2-113">Contains a pointer to a [**DSA\_SEC\_PAGE\_INFO**](dsa-sec-page-info.md) structure that defines the secondary page to create.</span></span> <span data-ttu-id="539a2-114">只有一個次要屬性工作表可以使用 **WM \_ ADSPROP \_ 工作表 \_ 建立** 訊息來建立，因此 [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) 結構只能包含一個 [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) 結構。</span><span class="sxs-lookup"><span data-stu-id="539a2-114">Only one secondary property sheet can be created with the **WM\_ADSPROP\_SHEET\_CREATE** message, so the [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) structure can only contain one [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) structure.</span></span>

</dd> <dt>

<span data-ttu-id="539a2-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="539a2-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="539a2-116">未使用。</span><span class="sxs-lookup"><span data-stu-id="539a2-116">Not used.</span></span> <span data-ttu-id="539a2-117">必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="539a2-117">Must be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="539a2-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="539a2-118">Return value</span></span>

<span data-ttu-id="539a2-119">此訊息的傳回值一律為零。</span><span class="sxs-lookup"><span data-stu-id="539a2-119">The return value for this message is always zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="539a2-120">備註</span><span class="sxs-lookup"><span data-stu-id="539a2-120">Remarks</span></span>

<span data-ttu-id="539a2-121">呼叫端必須使用 [**LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc)函式的單一呼叫來配置 [**DSA \_ SEC \_ 頁面 \_ 資訊**](dsa-sec-page-info.md)結構、title 字串和所有 [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)字串。</span><span class="sxs-lookup"><span data-stu-id="539a2-121">The caller must allocate the [**DSA\_SEC\_PAGE\_INFO**](dsa-sec-page-info.md) structure, the title string and all [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) strings using a single call to the [**LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc) function.</span></span> <span data-ttu-id="539a2-122">**WM \_ ADSPROP \_ SHEET \_ CREATE** message 是非同步訊息，因此它會在建立次要工作表之前傳回。</span><span class="sxs-lookup"><span data-stu-id="539a2-122">The **WM\_ADSPROP\_SHEET\_CREATE** message is an asynchronous message, so it will return before the secondary sheet is created.</span></span> <span data-ttu-id="539a2-123">因此，在訊息傳回之後，記憶體必須保持不變。</span><span class="sxs-lookup"><span data-stu-id="539a2-123">Because of this, the memory must remain intact after the message returns.</span></span> <span data-ttu-id="539a2-124">接收器會在建立次要工作表之後，透過單一呼叫 [**>localfree**](/windows/desktop/api/winbase/nf-winbase-localfree) 函式來釋放此記憶體。</span><span class="sxs-lookup"><span data-stu-id="539a2-124">The receiver will free this memory with a single call to the [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) function after the secondary sheet is created.</span></span>

## <a name="requirements"></a><span data-ttu-id="539a2-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="539a2-125">Requirements</span></span>



| <span data-ttu-id="539a2-126">需求</span><span class="sxs-lookup"><span data-stu-id="539a2-126">Requirement</span></span> | <span data-ttu-id="539a2-127">值</span><span class="sxs-lookup"><span data-stu-id="539a2-127">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="539a2-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="539a2-128">Minimum supported client</span></span><br/> | <span data-ttu-id="539a2-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="539a2-129">Windows Vista</span></span><br/>       |
| <span data-ttu-id="539a2-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="539a2-130">Minimum supported server</span></span><br/> | <span data-ttu-id="539a2-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="539a2-131">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="539a2-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="539a2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="539a2-133">**CFSTR \_ DS \_ PARENTHWND**</span><span class="sxs-lookup"><span data-stu-id="539a2-133">**CFSTR\_DS\_PARENTHWND**</span></span>](cfstr-ds-parenthwnd.md)
</dt> <dt>

[<span data-ttu-id="539a2-134">**DSA \_ 秒 \_ 頁面 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="539a2-134">**DSA\_SEC\_PAGE\_INFO**</span></span>](dsa-sec-page-info.md)
</dt> <dt>

[<span data-ttu-id="539a2-135">**DSOBJECTNAMES**</span><span class="sxs-lookup"><span data-stu-id="539a2-135">**DSOBJECTNAMES**</span></span>](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames)
</dt> <dt>

[<span data-ttu-id="539a2-136">**DSOBJECT**</span><span class="sxs-lookup"><span data-stu-id="539a2-136">**DSOBJECT**</span></span>](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)
</dt> <dt>

[<span data-ttu-id="539a2-137">**LocalAlloc**</span><span class="sxs-lookup"><span data-stu-id="539a2-137">**LocalAlloc**</span></span>](/windows/desktop/api/winbase/nf-winbase-localalloc)
</dt> <dt>

[<span data-ttu-id="539a2-138">**>localfree**</span><span class="sxs-lookup"><span data-stu-id="539a2-138">**LocalFree**</span></span>](/windows/desktop/api/winbase/nf-winbase-localfree)
</dt> </dl>

 

