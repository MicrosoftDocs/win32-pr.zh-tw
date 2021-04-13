---
title: 'WM_CAP_GET_USER_DATA 訊息 (Vfw .h) '
description: WM \_ CAP \_ 取得 \_ 使用者 \_ 資料訊息會 \_ 抓取與捕捉視窗相關聯的長 PTR 資料值。 您可以使用 capGetUserData 宏明確地傳送此訊息。
ms.assetid: f7c121ba-44a1-4916-b602-c53d8332c2af
keywords:
- WM_CAP_GET_USER_DATA message Windows 多媒體
topic_type:
- apiref
api_name:
- WM_CAP_GET_USER_DATA
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02951667600acba115f506a610b167b72b69ea99
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509147"
---
# <a name="wm_cap_get_user_data-message"></a><span data-ttu-id="102ac-105">WM \_ CAP \_ 取得 \_ 使用者 \_ 資料訊息</span><span class="sxs-lookup"><span data-stu-id="102ac-105">WM\_CAP\_GET\_USER\_DATA message</span></span>

<span data-ttu-id="102ac-106">**WM \_ CAP \_ 取得 \_ 使用者 \_ 資料** 訊息會抓取與捕捉視窗相關聯的 **長 \_ PTR** 資料值。</span><span class="sxs-lookup"><span data-stu-id="102ac-106">The **WM\_CAP\_GET\_USER\_DATA** message retrieves a **LONG\_PTR** data value associated with a capture window.</span></span> <span data-ttu-id="102ac-107">您可以使用 [**capGetUserData**](/windows/desktop/api/Vfw/nf-vfw-capgetuserdata) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="102ac-107">You can send this message explicitly or by using the [**capGetUserData**](/windows/desktop/api/Vfw/nf-vfw-capgetuserdata) macro.</span></span>


```C++
WM_CAP_GET_USER_DATA 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="102ac-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="102ac-108">Return Value</span></span>

<span data-ttu-id="102ac-109">傳回先前使用 [**WM \_ CAP \_ SET \_ 使用者 \_ 資料**](wm-cap-set-user-data.md) 訊息儲存的值。</span><span class="sxs-lookup"><span data-stu-id="102ac-109">Returns a value previously saved by using the [**WM\_CAP\_SET\_USER\_DATA**](wm-cap-set-user-data.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="102ac-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="102ac-110">Requirements</span></span>



| <span data-ttu-id="102ac-111">需求</span><span class="sxs-lookup"><span data-stu-id="102ac-111">Requirement</span></span> | <span data-ttu-id="102ac-112">值</span><span class="sxs-lookup"><span data-stu-id="102ac-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="102ac-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="102ac-113">Minimum supported client</span></span><br/> | <span data-ttu-id="102ac-114">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="102ac-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="102ac-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="102ac-115">Minimum supported server</span></span><br/> | <span data-ttu-id="102ac-116">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="102ac-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="102ac-117">標頭</span><span class="sxs-lookup"><span data-stu-id="102ac-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="102ac-118"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="102ac-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="102ac-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="102ac-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="102ac-120">影片捕獲</span><span class="sxs-lookup"><span data-stu-id="102ac-120">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="102ac-121">影片捕獲訊息</span><span class="sxs-lookup"><span data-stu-id="102ac-121">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





