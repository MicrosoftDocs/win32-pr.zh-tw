---
title: 'MCIWNDM_SETSPEED 訊息 (Vfw .h) '
description: MCIWNDM \_ SETSPEED 訊息會設定 MCI 裝置的播放速度。 您可以使用 MCIWndSetSpeed 宏明確地傳送此訊息。
ms.assetid: 7658dd25-dc68-4bd1-b995-df06b509be16
keywords:
- MCIWNDM_SETSPEED message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_SETSPEED
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 282bb3a2e135b674605be55aaccaa455d30edbcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934681"
---
# <a name="mciwndm_setspeed-message"></a><span data-ttu-id="fbb2d-105">MCIWNDM \_ SETSPEED 訊息</span><span class="sxs-lookup"><span data-stu-id="fbb2d-105">MCIWNDM\_SETSPEED message</span></span>

<span data-ttu-id="fbb2d-106">**MCIWNDM \_ SETSPEED** 訊息會設定 MCI 裝置的播放速度。</span><span class="sxs-lookup"><span data-stu-id="fbb2d-106">The **MCIWNDM\_SETSPEED** message sets the playback speed of an MCI device.</span></span> <span data-ttu-id="fbb2d-107">您可以使用 [**MCIWndSetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="fbb2d-107">You can send this message explicitly or by using the [**MCIWndSetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed) macro.</span></span>


```C++
MCIWNDM_SETSPEED 
wParam = 0; 
lParam = (LPARAM) (UINT) iSpeed; 
```



## <a name="parameters"></a><span data-ttu-id="fbb2d-108">參數</span><span class="sxs-lookup"><span data-stu-id="fbb2d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbb2d-109"><span id="iSpeed"></span><span id="ispeed"></span><span id="ISPEED"></span>*iSpeed*</span><span class="sxs-lookup"><span data-stu-id="fbb2d-109"><span id="iSpeed"></span><span id="ispeed"></span><span id="ISPEED"></span>*iSpeed*</span></span>
</dt> <dd>

<span data-ttu-id="fbb2d-110">播放速度。</span><span class="sxs-lookup"><span data-stu-id="fbb2d-110">Playback speed.</span></span> <span data-ttu-id="fbb2d-111">指定1000的一般速度、更大的值以加快速度，以及較小的值以加快速度。</span><span class="sxs-lookup"><span data-stu-id="fbb2d-111">Specify 1000 for normal speed, larger values for faster speeds, and smaller values for slower speeds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbb2d-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="fbb2d-112">Return Value</span></span>

<span data-ttu-id="fbb2d-113">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="fbb2d-113">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbb2d-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="fbb2d-114">Requirements</span></span>



| <span data-ttu-id="fbb2d-115">需求</span><span class="sxs-lookup"><span data-stu-id="fbb2d-115">Requirement</span></span> | <span data-ttu-id="fbb2d-116">值</span><span class="sxs-lookup"><span data-stu-id="fbb2d-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="fbb2d-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fbb2d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fbb2d-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fbb2d-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="fbb2d-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fbb2d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fbb2d-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fbb2d-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="fbb2d-121">標頭</span><span class="sxs-lookup"><span data-stu-id="fbb2d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbb2d-122"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="fbb2d-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbb2d-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fbb2d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbb2d-124">**MCIWndSetSpeed**</span><span class="sxs-lookup"><span data-stu-id="fbb2d-124">**MCIWndSetSpeed**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed)
</dt> </dl>

 

 





