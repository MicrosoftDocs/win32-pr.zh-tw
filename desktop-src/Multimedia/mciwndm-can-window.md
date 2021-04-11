---
title: 'MCIWNDM_CAN_WINDOW 訊息 (Vfw .h) '
description: MCIWNDM \_ 可以 \_ 視窗訊息判斷 MCI 裝置是否支援視窗導向的 mci 命令。 您可以使用 MCIWndCanWindow 宏明確地傳送此訊息。
ms.assetid: bf89c096-1272-441e-9334-2b4215dbc979
keywords:
- MCIWNDM_CAN_WINDOW message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_WINDOW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d638b61093483b6e834b57af1d5c892d77d0f1d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934254"
---
# <a name="mciwndm_can_window-message"></a><span data-ttu-id="cbdbf-105">MCIWNDM \_ 可以是 \_ 視窗訊息</span><span class="sxs-lookup"><span data-stu-id="cbdbf-105">MCIWNDM\_CAN\_WINDOW message</span></span>

<span data-ttu-id="cbdbf-106">**MCIWNDM \_ 可以 \_ 視窗** 訊息判斷 MCI 裝置是否支援視窗導向的 mci 命令。</span><span class="sxs-lookup"><span data-stu-id="cbdbf-106">The **MCIWNDM\_CAN\_WINDOW** message determines if an MCI device supports window-oriented MCI commands.</span></span> <span data-ttu-id="cbdbf-107">您可以使用 [**MCIWndCanWindow**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="cbdbf-107">You can send this message explicitly or by using the [**MCIWndCanWindow**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow) macro.</span></span>


```C++
MCIWNDM_CAN_WINDOW 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="cbdbf-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="cbdbf-108">Return Value</span></span>

<span data-ttu-id="cbdbf-109">如果裝置支援視窗導向的 MCI 命令，則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="cbdbf-109">Returns **TRUE** if the device supports window-oriented MCI commands or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbdbf-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="cbdbf-110">Requirements</span></span>



| <span data-ttu-id="cbdbf-111">需求</span><span class="sxs-lookup"><span data-stu-id="cbdbf-111">Requirement</span></span> | <span data-ttu-id="cbdbf-112">值</span><span class="sxs-lookup"><span data-stu-id="cbdbf-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="cbdbf-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cbdbf-113">Minimum supported client</span></span><br/> | <span data-ttu-id="cbdbf-114">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cbdbf-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="cbdbf-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cbdbf-115">Minimum supported server</span></span><br/> | <span data-ttu-id="cbdbf-116">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cbdbf-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="cbdbf-117">標頭</span><span class="sxs-lookup"><span data-stu-id="cbdbf-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbdbf-118"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="cbdbf-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbdbf-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cbdbf-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbdbf-120">**MCIWndCanWindow**</span><span class="sxs-lookup"><span data-stu-id="cbdbf-120">**MCIWndCanWindow**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow)
</dt> </dl>

 

 





