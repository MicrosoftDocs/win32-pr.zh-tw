---
title: 'WM_CAP_SET_USER_DATA 訊息 (Vfw .h) '
description: WM \_ CAP \_ 設定 \_ 使用者資料訊息會將 \_ 長的 \_ PTR 資料值與捕捉視窗產生關聯。 您可以使用 capSetUserData 宏明確地傳送此訊息。
ms.assetid: 067502e3-f009-4cf2-b612-4a0b64624416
keywords:
- WM_CAP_SET_USER_DATA message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_SET_USER_DATA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 542b8e49f740bfc265824947237841dede1f6065
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106109"
---
# <a name="wm_cap_set_user_data-message"></a><span data-ttu-id="8aa48-105">WM \_ CAP \_ 設定 \_ 使用者 \_ 資料訊息</span><span class="sxs-lookup"><span data-stu-id="8aa48-105">WM\_CAP\_SET\_USER\_DATA message</span></span>

<span data-ttu-id="8aa48-106">**WM \_ CAP \_ 設定 \_ 使用者 \_ 資料** 訊息會將長的 **\_ PTR** 資料值與捕捉視窗產生關聯。</span><span class="sxs-lookup"><span data-stu-id="8aa48-106">The **WM\_CAP\_SET\_USER\_DATA** message associates a **LONG\_PTR** data value with a capture window.</span></span> <span data-ttu-id="8aa48-107">您可以使用 [**capSetUserData**](/windows/desktop/api/Vfw/nf-vfw-capsetuserdata) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="8aa48-107">You can send this message explicitly or by using the [**capSetUserData**](/windows/desktop/api/Vfw/nf-vfw-capsetuserdata) macro.</span></span>


```C++
WM_CAP_SET_USER_DATA 
wParam = (WPARAM) 0; 
lParam = (LPARAM)lUser; 
```



## <a name="parameters"></a><span data-ttu-id="8aa48-108">參數</span><span class="sxs-lookup"><span data-stu-id="8aa48-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8aa48-109"><span id="lUser"></span><span id="luser"></span><span id="LUSER"></span>*lUser*</span><span class="sxs-lookup"><span data-stu-id="8aa48-109"><span id="lUser"></span><span id="luser"></span><span id="LUSER"></span>*lUser*</span></span>
</dt> <dd>

<span data-ttu-id="8aa48-110">與捕捉視窗相關聯的資料值。</span><span class="sxs-lookup"><span data-stu-id="8aa48-110">Data value to associate with a capture window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8aa48-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="8aa48-111">Return Value</span></span>

<span data-ttu-id="8aa48-112">如果成功，則傳回 **TRUE** ; 如果串流捕捉正在進行，則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="8aa48-112">Returns **TRUE** if successful or **FALSE** if streaming capture is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="8aa48-113">備註</span><span class="sxs-lookup"><span data-stu-id="8aa48-113">Remarks</span></span>

<span data-ttu-id="8aa48-114">此訊息通常是用來指向與捕捉視窗相關聯的資料區塊。</span><span class="sxs-lookup"><span data-stu-id="8aa48-114">Typically this message is used to point to a block of data associated with a capture window.</span></span>

## <a name="requirements"></a><span data-ttu-id="8aa48-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="8aa48-115">Requirements</span></span>



| <span data-ttu-id="8aa48-116">需求</span><span class="sxs-lookup"><span data-stu-id="8aa48-116">Requirement</span></span> | <span data-ttu-id="8aa48-117">值</span><span class="sxs-lookup"><span data-stu-id="8aa48-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8aa48-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8aa48-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8aa48-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8aa48-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="8aa48-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8aa48-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8aa48-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8aa48-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8aa48-122">標頭</span><span class="sxs-lookup"><span data-stu-id="8aa48-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8aa48-123"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="8aa48-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8aa48-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8aa48-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8aa48-125">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="8aa48-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="8aa48-126">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="8aa48-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





