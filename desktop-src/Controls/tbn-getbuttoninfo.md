---
title: 'TBN_GETBUTTONINFO (Commctrl 的通知碼) '
description: 抓取工具列自訂資訊，並通知工具列的父視窗對工具列進行的任何變更。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 088527fe-5a38-4c35-ba68-d0cbfdee410c
keywords:
- TBN_GETBUTTONINFO 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TBN_GETBUTTONINFO
- TBN_GETBUTTONINFOA
- TBN_GETBUTTONINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 409297306901980fa8b831e5c1129a13c596ef0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934781"
---
# <a name="tbn_getbuttoninfo-notification-code"></a><span data-ttu-id="d5a49-105">TBN \_ GETBUTTONINFO 通知碼</span><span class="sxs-lookup"><span data-stu-id="d5a49-105">TBN\_GETBUTTONINFO notification code</span></span>

<span data-ttu-id="d5a49-106">抓取工具列自訂資訊，並通知工具列的父視窗對工具列進行的任何變更。</span><span class="sxs-lookup"><span data-stu-id="d5a49-106">Retrieves toolbar customization information and notifies the toolbar's parent window of any changes being made to the toolbar.</span></span> <span data-ttu-id="d5a49-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="d5a49-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_GETBUTTONINFO 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d5a49-108">參數</span><span class="sxs-lookup"><span data-stu-id="d5a49-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5a49-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d5a49-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d5a49-110">[**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="d5a49-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure.</span></span> <span data-ttu-id="d5a49-111">**IItem** 成員會指定以零為起始的索引，此索引會提供 [自訂工具列] 對話方塊所顯示的按鈕計數，以及工具列上顯示的按鈕。</span><span class="sxs-lookup"><span data-stu-id="d5a49-111">The **iItem** member specifies a zero-based index that provides a count of the buttons the Customize Toolbar dialog box displays as both available and present on the toolbar.</span></span> <span data-ttu-id="d5a49-112">**PszText** 成員指定目前按鈕文字的位址，而 **cchText** 指定其長度（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="d5a49-112">The **pszText** member specifies the address of the current button text, and **cchText** specifies its length in characters.</span></span> <span data-ttu-id="d5a49-113">應用程式應該以按鈕的相關資訊填入結構。</span><span class="sxs-lookup"><span data-stu-id="d5a49-113">The application should fill the structure with information about the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5a49-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="d5a49-114">Return value</span></span>

<span data-ttu-id="d5a49-115">如果按鈕資訊已複製到指定的結構，則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="d5a49-115">Returns **TRUE** if button information was copied to the specified structure, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5a49-116">備註</span><span class="sxs-lookup"><span data-stu-id="d5a49-116">Remarks</span></span>

<span data-ttu-id="d5a49-117">工具列控制項會配置緩衝區，而接收者 (父視窗) 必須將文字複製到該緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d5a49-117">The toolbar control allocates a buffer, and the receiver (parent window) must copy the text into that buffer.</span></span> <span data-ttu-id="d5a49-118">當 TBN \_ GETBUTTONINFO 傳送至父視窗時，cchText 成員會包含工具列所配置的緩衝區長度。</span><span class="sxs-lookup"><span data-stu-id="d5a49-118">The **cchText** member contains the length of the buffer allocated by the toolbar when TBN\_GETBUTTONINFO is sent to the parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5a49-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="d5a49-119">Requirements</span></span>



| <span data-ttu-id="d5a49-120">需求</span><span class="sxs-lookup"><span data-stu-id="d5a49-120">Requirement</span></span> | <span data-ttu-id="d5a49-121">值</span><span class="sxs-lookup"><span data-stu-id="d5a49-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d5a49-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d5a49-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d5a49-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d5a49-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d5a49-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d5a49-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d5a49-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d5a49-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d5a49-126">標頭</span><span class="sxs-lookup"><span data-stu-id="d5a49-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5a49-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="d5a49-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="d5a49-128">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="d5a49-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d5a49-129">**TBN \_GETBUTTONINFOW** (Unicode) 和 **TBN \_ GETBUTTONINFOA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="d5a49-129">**TBN\_GETBUTTONINFOW** (Unicode) and **TBN\_GETBUTTONINFOA** (ANSI)</span></span><br/>       |



 

 





