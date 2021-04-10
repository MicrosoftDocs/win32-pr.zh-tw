---
title: 'MCIWNDM_PLAYREVERSE 訊息 (Vfw .h) '
description: MCIWNDM \_ PLAYREVERSE 訊息會以反向方向播放目前的內容，從目前位置開始，結束于內容的開頭，或直到另一個命令停止播放為止。
ms.assetid: 93a22454-eca6-453f-abbe-6cf20198dbad
keywords:
- MCIWNDM_PLAYREVERSE message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_PLAYREVERSE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84b0a2e230e3c57e8314e455be5dfbc5cea2c013
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093788"
---
# <a name="mciwndm_playreverse-message"></a><span data-ttu-id="cd247-104">MCIWNDM \_ PLAYREVERSE 訊息</span><span class="sxs-lookup"><span data-stu-id="cd247-104">MCIWNDM\_PLAYREVERSE message</span></span>

<span data-ttu-id="cd247-105">**MCIWNDM \_ PLAYREVERSE** 訊息會以反向方向播放目前的內容，從目前位置開始，結束于內容的開頭，或直到另一個命令停止播放為止。</span><span class="sxs-lookup"><span data-stu-id="cd247-105">The **MCIWNDM\_PLAYREVERSE** message plays the current content in the reverse direction, beginning at the current position and ending at the beginning of the content or until another command stops playback.</span></span> <span data-ttu-id="cd247-106">您可以使用 [**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="cd247-106">You can send this message explicitly or by using the [**MCIWndPlayReverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) macro.</span></span>


```C++
MCIWNDM_PLAYREVERSE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="cd247-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="cd247-107">Return Value</span></span>

<span data-ttu-id="cd247-108">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="cd247-108">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd247-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="cd247-109">Requirements</span></span>



| <span data-ttu-id="cd247-110">需求</span><span class="sxs-lookup"><span data-stu-id="cd247-110">Requirement</span></span> | <span data-ttu-id="cd247-111">值</span><span class="sxs-lookup"><span data-stu-id="cd247-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="cd247-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cd247-112">Minimum supported client</span></span><br/> | <span data-ttu-id="cd247-113">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cd247-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="cd247-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cd247-114">Minimum supported server</span></span><br/> | <span data-ttu-id="cd247-115">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cd247-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="cd247-116">標頭</span><span class="sxs-lookup"><span data-stu-id="cd247-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd247-117"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="cd247-117"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd247-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cd247-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd247-119">**MCIWndPlayReverse**</span><span class="sxs-lookup"><span data-stu-id="cd247-119">**MCIWndPlayReverse**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse)
</dt> </dl>

 

 





