---
title: 'TTM_GETTEXT 訊息 (Commctrl .h) '
description: 抓取工具提示控制項維護工具的相關資訊。
ms.assetid: f2afa706-4209-4761-a981-df3d5b938c88
keywords:
- TTM_GETTEXT message Windows 控制項
topic_type:
- apiref
api_name:
- TTM_GETTEXT
- TTM_GETTEXTA
- TTM_GETTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f774671d34f89306593d23481fa917190ae69aaa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106996579"
---
# <a name="ttm_gettext-message"></a><span data-ttu-id="a0808-104">TTM \_ GETTEXT 訊息</span><span class="sxs-lookup"><span data-stu-id="a0808-104">TTM\_GETTEXT message</span></span>

<span data-ttu-id="a0808-105">抓取工具提示控制項維護工具的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a0808-105">Retrieves the information a tooltip control maintains about a tool.</span></span>

## <a name="parameters"></a><span data-ttu-id="a0808-106">參數</span><span class="sxs-lookup"><span data-stu-id="a0808-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0808-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a0808-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a0808-108">要複製到 **lpszText** 所指向之緩衝區的 **TCHARs** 數目，包括終止的 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a0808-108">The number of **TCHARs**, including the terminating **NULL**, to copy to the buffer pointed to by **lpszText**.</span></span> </dd> <dt>

<span data-ttu-id="a0808-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a0808-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a0808-110">[**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="a0808-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="a0808-111">將此結構的 **cbSize** 成員設定為， `sizeof(TOOLINFO)` 然後再傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="a0808-111">Set the **cbSize** member of this structure to `sizeof(TOOLINFO)` before sending this message.</span></span> <span data-ttu-id="a0808-112">設定 **hwnd** 和 **uId** 成員，以識別要取得資訊的工具。</span><span class="sxs-lookup"><span data-stu-id="a0808-112">Set the **hwnd** and **uId** members to identify the tool for which to retrieve information.</span></span> <span data-ttu-id="a0808-113">配置 *wParam* 所指定之大小的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="a0808-113">Allocate a buffer of size specified by *wParam*.</span></span> <span data-ttu-id="a0808-114">設定 **lpszText** 成員指向緩衝區以接收工具文字。</span><span class="sxs-lookup"><span data-stu-id="a0808-114">Set the **lpszText** member to point to the buffer to receive the tool text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0808-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="a0808-115">Return value</span></span>

<span data-ttu-id="a0808-116">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="a0808-116">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0808-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="a0808-117">Requirements</span></span>



| <span data-ttu-id="a0808-118">需求</span><span class="sxs-lookup"><span data-stu-id="a0808-118">Requirement</span></span> | <span data-ttu-id="a0808-119">值</span><span class="sxs-lookup"><span data-stu-id="a0808-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a0808-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a0808-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a0808-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a0808-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a0808-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a0808-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a0808-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a0808-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a0808-124">標頭</span><span class="sxs-lookup"><span data-stu-id="a0808-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0808-125"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a0808-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="a0808-126">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="a0808-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a0808-127">**TTM \_GETTEXTW** (Unicode) 和 **TTM \_ GETTEXTA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="a0808-127">**TTM\_GETTEXTW** (Unicode) and **TTM\_GETTEXTA** (ANSI)</span></span><br/>                   |



 

 





