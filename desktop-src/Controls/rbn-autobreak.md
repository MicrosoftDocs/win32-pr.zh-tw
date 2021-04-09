---
title: 'RBN_AUTOBREAK 訊息 (Commctrl .h) '
description: 通知 Rebar 的父系，將會在橫條中顯示中斷。 父代會決定是否要進行中斷。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: b7a63027-6cfa-4d5a-9ea6-fdd8b4fb6864
keywords:
- RBN_AUTOBREAK message Windows 控制項
topic_type:
- apiref
api_name:
- RBN_AUTOBREAK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d614277d89578cb66e528ba16656ed55681ebbcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844339"
---
# <a name="rbn_autobreak-message"></a><span data-ttu-id="c164f-106">RBN \_ AUTOBREAK 訊息</span><span class="sxs-lookup"><span data-stu-id="c164f-106">RBN\_AUTOBREAK message</span></span>

<span data-ttu-id="c164f-107">通知 [Rebar 的](rebar-controls.md) 父系，將會在橫條中顯示中斷。</span><span class="sxs-lookup"><span data-stu-id="c164f-107">Notifies a [rebar's](rebar-controls.md) parent that a break will appear in the bar.</span></span> <span data-ttu-id="c164f-108">父代會決定是否要進行中斷。</span><span class="sxs-lookup"><span data-stu-id="c164f-108">The parent determines whether to make the break.</span></span> <span data-ttu-id="c164f-109">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="c164f-109">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_AUTOBREAK

    pnmRebarAutoBreak = (LPNMREBARAUTOBREAK) lParam;
```



## <a name="parameters"></a><span data-ttu-id="c164f-110">參數</span><span class="sxs-lookup"><span data-stu-id="c164f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c164f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c164f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c164f-112">[**NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak)結構的指標，其中包含通知碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c164f-112">Pointer to a [**NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c164f-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="c164f-113">Return value</span></span>

<span data-ttu-id="c164f-114">未使用此通知的傳回值。</span><span class="sxs-lookup"><span data-stu-id="c164f-114">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="c164f-115">備註</span><span class="sxs-lookup"><span data-stu-id="c164f-115">Remarks</span></span>

<span data-ttu-id="c164f-116">[**NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak)結構之 **fAutoBreak** 成員中的值會指出是否應該在 Rebar 中出現中斷。</span><span class="sxs-lookup"><span data-stu-id="c164f-116">The value in the **fAutoBreak** member of the [**NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) structure indicates whether a break should occur in the rebar.</span></span>

<span data-ttu-id="c164f-117">若要使用此通知碼，請在資訊清單中指定 Comctl32.dll 第6版。</span><span class="sxs-lookup"><span data-stu-id="c164f-117">To use this notification code, specify Comctl32.dll version 6 in the manifest.</span></span> <span data-ttu-id="c164f-118">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="c164f-118">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c164f-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="c164f-119">Requirements</span></span>



| <span data-ttu-id="c164f-120">需求</span><span class="sxs-lookup"><span data-stu-id="c164f-120">Requirement</span></span> | <span data-ttu-id="c164f-121">值</span><span class="sxs-lookup"><span data-stu-id="c164f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c164f-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c164f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c164f-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c164f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c164f-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c164f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c164f-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c164f-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c164f-126">標頭</span><span class="sxs-lookup"><span data-stu-id="c164f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c164f-127"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c164f-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





