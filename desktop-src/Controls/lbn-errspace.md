---
title: 'LBN_ERRSPACE (Winuser 的通知碼) '
description: 通知應用程式清單方塊無法配置足夠的記憶體來符合特定的要求。 清單方塊的父視窗會透過 WM 命令訊息接收此通知碼 \_ 。
ms.assetid: ff716ad0-cbd8-4ac3-bcaf-d5be81355eaa
keywords:
- LBN_ERRSPACE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LBN_ERRSPACE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d324b17a83e38a9b3592be71720486910e88689d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104187300"
---
# <a name="lbn_errspace-notification-code"></a><span data-ttu-id="ed20a-105">LBN \_ ERRSPACE 通知碼</span><span class="sxs-lookup"><span data-stu-id="ed20a-105">LBN\_ERRSPACE notification code</span></span>

<span data-ttu-id="ed20a-106">通知應用程式清單方塊無法配置足夠的記憶體來符合特定的要求。</span><span class="sxs-lookup"><span data-stu-id="ed20a-106">Notifies the application that the list box cannot allocate enough memory to meet a specific request.</span></span> <span data-ttu-id="ed20a-107">清單方塊的父視窗會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息接收此通知碼。</span><span class="sxs-lookup"><span data-stu-id="ed20a-107">The parent window of the list box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
LBN_ERRSPACE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="ed20a-108">參數</span><span class="sxs-lookup"><span data-stu-id="ed20a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed20a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ed20a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ed20a-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含清單方塊的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ed20a-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the list box.</span></span> <span data-ttu-id="ed20a-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定通知碼。</span><span class="sxs-lookup"><span data-stu-id="ed20a-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="ed20a-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ed20a-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ed20a-113">清單方塊的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ed20a-113">Handle to the list box.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ed20a-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="ed20a-114">Requirements</span></span>



| <span data-ttu-id="ed20a-115">需求</span><span class="sxs-lookup"><span data-stu-id="ed20a-115">Requirement</span></span> | <span data-ttu-id="ed20a-116">值</span><span class="sxs-lookup"><span data-stu-id="ed20a-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed20a-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ed20a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ed20a-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ed20a-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ed20a-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ed20a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ed20a-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ed20a-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ed20a-121">標頭</span><span class="sxs-lookup"><span data-stu-id="ed20a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed20a-122"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="ed20a-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed20a-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ed20a-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="ed20a-124">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="ed20a-124">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="ed20a-125">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ed20a-125">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="ed20a-126">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ed20a-126">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ed20a-127">**WM \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="ed20a-127">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

