---
title: 'TTM_ENUMTOOLS 訊息 (Commctrl .h) '
description: 抓取工具提示控制項針對目前工具 \ 郵件所維護的資訊，也就是工具提示目前顯示文字的工具。
ms.assetid: c470db71-c24c-45f4-b497-e59811017eee
keywords:
- TTM_ENUMTOOLS message Windows 控制項
topic_type:
- apiref
api_name:
- TTM_ENUMTOOLS
- TTM_ENUMTOOLSA
- TTM_ENUMTOOLSW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a67f23a145838aa3562c81e78fb82c3ea66320df
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327133"
---
# <a name="ttm_enumtools-message"></a><span data-ttu-id="0c35c-104">TTM \_ ENUMTOOLS 訊息</span><span class="sxs-lookup"><span data-stu-id="0c35c-104">TTM\_ENUMTOOLS message</span></span>

<span data-ttu-id="0c35c-105">抓取工具提示控制項針對目前工具所維護的資訊，也就是工具提示目前顯示文字的工具。</span><span class="sxs-lookup"><span data-stu-id="0c35c-105">Retrieves the information that a tooltip control maintains about the current tool that is, the tool for which the tooltip is currently displaying text.</span></span>

## <a name="parameters"></a><span data-ttu-id="0c35c-106">參數</span><span class="sxs-lookup"><span data-stu-id="0c35c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c35c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0c35c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0c35c-108">以零為基底的工具索引，用來取得資訊。</span><span class="sxs-lookup"><span data-stu-id="0c35c-108">Zero-based index of the tool for which to retrieve information.</span></span>

</dd> <dt>

<span data-ttu-id="0c35c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0c35c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0c35c-110">[**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)結構的指標，此結構會接收工具的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0c35c-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure that receives information about the tool.</span></span> <span data-ttu-id="0c35c-111">將此結構的 **cbSize** 成員設定為 SIZEOF (TOOLINFO) ，然後再傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="0c35c-111">Set the **cbSize** member of this structure to sizeof(TOOLINFO) before sending this message.</span></span> <span data-ttu-id="0c35c-112">配置緩衝區。</span><span class="sxs-lookup"><span data-stu-id="0c35c-112">Allocate a buffer.</span></span> <span data-ttu-id="0c35c-113">設定 **lpszText** 成員指向緩衝區以接收工具文字。</span><span class="sxs-lookup"><span data-stu-id="0c35c-113">Set the **lpszText** member to point to the buffer to receive the tool text.</span></span> <span data-ttu-id="0c35c-114">沒有任何方法可判斷所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="0c35c-114">There is no way to determine the required buffer size.</span></span> <span data-ttu-id="0c35c-115">不過，在 **TOOLINFO** 結構的 **lpszText** 成員上傳回的工具文字具有最大長度 80 **TCHARs**，包括終止的 **Null**。</span><span class="sxs-lookup"><span data-stu-id="0c35c-115">However, tool text, as returned at the **lpszText** member of the **TOOLINFO** structure, has a maximum length of 80 **TCHARs**, including the terminating **NULL**.</span></span> <span data-ttu-id="0c35c-116">如果文字超過此長度，則會被截斷。</span><span class="sxs-lookup"><span data-stu-id="0c35c-116">If the text exceeds this length, it is truncated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c35c-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="0c35c-117">Return value</span></span>

<span data-ttu-id="0c35c-118">無論是否列舉工具，都會傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="0c35c-118">Returns **FALSE** whether or not a tool was enumerated.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c35c-119">備註</span><span class="sxs-lookup"><span data-stu-id="0c35c-119">Remarks</span></span>

<span data-ttu-id="0c35c-120">**安全性警告：** 使用此訊息可能會危害程式的安全性。</span><span class="sxs-lookup"><span data-stu-id="0c35c-120">**Security Warning:** Using this message might compromise the security of your program.</span></span> <span data-ttu-id="0c35c-121">這則訊息不會提供訊息接收者知道緩衝區大小或指定緩衝區大小的方法。</span><span class="sxs-lookup"><span data-stu-id="0c35c-121">This message does not provide a way for the message receiver to know the size of the buffer or to specify the size of the buffer.</span></span> <span data-ttu-id="0c35c-122">您應該先複習 [安全性考慮： Microsoft Windows 控制項](sec-comctls.md) ，再繼續進行。</span><span class="sxs-lookup"><span data-stu-id="0c35c-122">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c35c-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="0c35c-123">Requirements</span></span>



| <span data-ttu-id="0c35c-124">需求</span><span class="sxs-lookup"><span data-stu-id="0c35c-124">Requirement</span></span> | <span data-ttu-id="0c35c-125">值</span><span class="sxs-lookup"><span data-stu-id="0c35c-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0c35c-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0c35c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0c35c-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0c35c-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0c35c-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0c35c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0c35c-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0c35c-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0c35c-130">標頭</span><span class="sxs-lookup"><span data-stu-id="0c35c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c35c-131"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="0c35c-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="0c35c-132">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="0c35c-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0c35c-133">**TTM \_ENUMTOOLSW** (Unicode) 和 **TTM \_ ENUMTOOLSA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="0c35c-133">**TTM\_ENUMTOOLSW** (Unicode) and **TTM\_ENUMTOOLSA** (ANSI)</span></span><br/>               |



 

 





