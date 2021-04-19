---
title: 'MCIWNDM_CAN_PLAY 訊息 (Vfw .h) '
description: MCIWNDM \_ 可以 \_ 播放訊息，判斷 MCI 裝置是否可以播放某個其他種類的資料檔或內容。 您可以使用 MCIWndCanPlay 宏明確地傳送此訊息。
ms.assetid: dbb742b0-b8ab-4b80-96da-c4823a4747c9
keywords:
- MCIWNDM_CAN_PLAY message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_PLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 043a0fc15260f7448df8d009a6b468616244269d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106973303"
---
# <a name="mciwndm_can_play-message"></a><span data-ttu-id="f1832-105">MCIWNDM \_ 可以 \_ 播放訊息</span><span class="sxs-lookup"><span data-stu-id="f1832-105">MCIWNDM\_CAN\_PLAY message</span></span>

<span data-ttu-id="f1832-106">**MCIWNDM \_ 可以 \_ 播放** 訊息，判斷 MCI 裝置是否可以播放某個其他種類的資料檔或內容。</span><span class="sxs-lookup"><span data-stu-id="f1832-106">The **MCIWNDM\_CAN\_PLAY** message determines if an MCI device can play a data file or content of some other kind.</span></span> <span data-ttu-id="f1832-107">您可以使用 [**MCIWndCanPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="f1832-107">You can send this message explicitly or by using the [**MCIWndCanPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay) macro.</span></span>


```C++
MCIWNDM_CAN_PLAY 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="f1832-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="f1832-108">Return Value</span></span>

<span data-ttu-id="f1832-109">如果裝置支援播放資料則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="f1832-109">Returns **TRUE** if the device supports playing the data or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1832-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1832-110">Requirements</span></span>



| <span data-ttu-id="f1832-111">需求</span><span class="sxs-lookup"><span data-stu-id="f1832-111">Requirement</span></span> | <span data-ttu-id="f1832-112">值</span><span class="sxs-lookup"><span data-stu-id="f1832-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f1832-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f1832-113">Minimum supported client</span></span><br/> | <span data-ttu-id="f1832-114">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1832-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f1832-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f1832-115">Minimum supported server</span></span><br/> | <span data-ttu-id="f1832-116">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1832-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f1832-117">標頭</span><span class="sxs-lookup"><span data-stu-id="f1832-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1832-118"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="f1832-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1832-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f1832-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1832-120">**MCIWndCanPlay**</span><span class="sxs-lookup"><span data-stu-id="f1832-120">**MCIWndCanPlay**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay)
</dt> </dl>

 

 





