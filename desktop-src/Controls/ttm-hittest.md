---
title: 'TTM_HITTEST 訊息 (Commctrl .h) '
description: 測試點以判斷它是否在指定之工具的周框矩形內，如果是，則會抓取工具的相關資訊。
ms.assetid: d4dcc29b-c64c-41b8-a153-300df68ecdf5
keywords:
- TTM_HITTEST message Windows 控制項
topic_type:
- apiref
api_name:
- TTM_HITTEST
- TTM_HITTESTA
- TTM_HITTESTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b515ccb5c283b66760f24c02749368e424e6fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465352"
---
# <a name="ttm_hittest-message"></a><span data-ttu-id="0e098-104">TTM \_ system.windows.media.visualtreehelper.hittest 訊息</span><span class="sxs-lookup"><span data-stu-id="0e098-104">TTM\_HITTEST message</span></span>

<span data-ttu-id="0e098-105">測試點以判斷它是否在指定之工具的周框矩形內，如果是，則會抓取工具的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0e098-105">Tests a point to determine whether it is within the bounding rectangle of the specified tool and, if it is, retrieves information about the tool.</span></span>

## <a name="parameters"></a><span data-ttu-id="0e098-106">參數</span><span class="sxs-lookup"><span data-stu-id="0e098-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e098-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0e098-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0e098-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="0e098-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0e098-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0e098-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0e098-110">[**TTHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tthittestinfoa)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="0e098-110">Pointer to a [**TTHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tthittestinfoa) structure.</span></span> <span data-ttu-id="0e098-111">傳送訊息時， **hwnd** 成員必須指定工具的控制碼，而 **pt** 成員必須指定點的座標。</span><span class="sxs-lookup"><span data-stu-id="0e098-111">When sending the message, the **hwnd** member must specify the handle to a tool and the **pt** member must specify the coordinates of a point.</span></span> <span data-ttu-id="0e098-112">如果傳回值為 **TRUE**，則 **Ti** 成員 ([**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) 結構) 接收有關該點之工具的資訊。</span><span class="sxs-lookup"><span data-stu-id="0e098-112">If the return value is **TRUE**, the **ti** member (a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure) receives information about the tool that occupies the point.</span></span> <span data-ttu-id="0e098-113">傳送此訊息之前，必須先填入 **ti** 結構的 **cbSize** 成員。</span><span class="sxs-lookup"><span data-stu-id="0e098-113">The **cbSize** member of the **ti** structure must be filled in before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e098-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="0e098-114">Return value</span></span>

<span data-ttu-id="0e098-115">如果工具佔用指定的點，則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="0e098-115">Returns **TRUE** if the tool occupies the specified point, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e098-116">備註</span><span class="sxs-lookup"><span data-stu-id="0e098-116">Remarks</span></span>

<span data-ttu-id="0e098-117">當工具已設定 TTF TRACK 旗標時，必須傳送此訊息 \_ 。</span><span class="sxs-lookup"><span data-stu-id="0e098-117">This message must be sent when the tool has the TTF\_TRACK flag set.</span></span> <span data-ttu-id="0e098-118">如需此旗標的詳細資訊，請參閱 [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa)。</span><span class="sxs-lookup"><span data-stu-id="0e098-118">For more information on this flag, see [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa).</span></span> <span data-ttu-id="0e098-119">\_如果未設定 TTF TRACK，TTM system.windows.media.visualtreehelper.hittest 將會失敗 \_ ，不論點擊點是否在 [工具] 矩形中。</span><span class="sxs-lookup"><span data-stu-id="0e098-119">TTM\_HITTEST will fail if TTF\_TRACK is not set, regardless if the hit point is in the tools rectangle or not.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e098-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="0e098-120">Requirements</span></span>



| <span data-ttu-id="0e098-121">需求</span><span class="sxs-lookup"><span data-stu-id="0e098-121">Requirement</span></span> | <span data-ttu-id="0e098-122">值</span><span class="sxs-lookup"><span data-stu-id="0e098-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0e098-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0e098-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0e098-124">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0e098-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0e098-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0e098-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0e098-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0e098-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0e098-127">標頭</span><span class="sxs-lookup"><span data-stu-id="0e098-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e098-128"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="0e098-128"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="0e098-129">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="0e098-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0e098-130">**TTM \_HITTESTW** (Unicode) 和 **TTM \_ HITTESTA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="0e098-130">**TTM\_HITTESTW** (Unicode) and **TTM\_HITTESTA** (ANSI)</span></span><br/>                   |



 

 





