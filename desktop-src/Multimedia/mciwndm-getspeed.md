---
title: 'MCIWNDM_GETSPEED 訊息 (Vfw .h) '
description: MCIWNDM \_ GETSPEED 訊息會捕獲 MCI 裝置的播放速度。 您可以使用 MCIWndGetSpeed 宏明確地傳送此訊息。
ms.assetid: d10a8f88-e85e-449b-8655-bb0832031d59
keywords:
- MCIWNDM_GETSPEED message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_GETSPEED
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c84a8ebb3e97d4543f68f3a237add8eed7706ae2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466781"
---
# <a name="mciwndm_getspeed-message"></a><span data-ttu-id="d5c7e-105">MCIWNDM \_ GETSPEED 訊息</span><span class="sxs-lookup"><span data-stu-id="d5c7e-105">MCIWNDM\_GETSPEED message</span></span>

<span data-ttu-id="d5c7e-106">**MCIWNDM \_ GETSPEED** 訊息會捕獲 MCI 裝置的播放速度。</span><span class="sxs-lookup"><span data-stu-id="d5c7e-106">The **MCIWNDM\_GETSPEED** message retrieves the playback speed of an MCI device.</span></span> <span data-ttu-id="d5c7e-107">您可以使用 [**MCIWndGetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="d5c7e-107">You can send this message explicitly or by using the [**MCIWndGetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed) macro.</span></span>


```C++
MCIWNDM_GETSPEED 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="d5c7e-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="d5c7e-108">Return Value</span></span>

<span data-ttu-id="d5c7e-109">如果成功，則傳回播放速度。</span><span class="sxs-lookup"><span data-stu-id="d5c7e-109">Returns the playback speed if successful.</span></span> <span data-ttu-id="d5c7e-110">正常速度的值是1000。</span><span class="sxs-lookup"><span data-stu-id="d5c7e-110">The value for normal speed is 1000.</span></span> <span data-ttu-id="d5c7e-111">較大的值表示速度更快，較小的值表示速度較慢。</span><span class="sxs-lookup"><span data-stu-id="d5c7e-111">Larger values indicate faster speeds, smaller values indicate slower speeds.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5c7e-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="d5c7e-112">Requirements</span></span>



| <span data-ttu-id="d5c7e-113">需求</span><span class="sxs-lookup"><span data-stu-id="d5c7e-113">Requirement</span></span> | <span data-ttu-id="d5c7e-114">值</span><span class="sxs-lookup"><span data-stu-id="d5c7e-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d5c7e-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d5c7e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d5c7e-116">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d5c7e-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d5c7e-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d5c7e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d5c7e-118">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d5c7e-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d5c7e-119">標頭</span><span class="sxs-lookup"><span data-stu-id="d5c7e-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5c7e-120"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="d5c7e-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5c7e-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d5c7e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5c7e-122">**MCIWndGetSpeed**</span><span class="sxs-lookup"><span data-stu-id="d5c7e-122">**MCIWndGetSpeed**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed)
</dt> </dl>

 

 





