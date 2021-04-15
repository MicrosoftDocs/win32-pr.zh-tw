---
title: 'MCIWNDM_CAN_RECORD 訊息 (Vfw .h) '
description: MCIWNDM \_ 可以 \_ 記錄訊息，判斷 MCI 裝置是否支援錄製。 您可以使用 MCIWndCanRecord 宏明確地傳送此訊息。
ms.assetid: b5a789fa-6a88-487d-a374-8f4798ee5a62
keywords:
- MCIWNDM_CAN_RECORD message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_RECORD
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2acbc9efa3ca973c12112a599d1202ad936107a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466644"
---
# <a name="mciwndm_can_record-message"></a><span data-ttu-id="8774b-105">MCIWNDM \_ 可以 \_ 記錄訊息</span><span class="sxs-lookup"><span data-stu-id="8774b-105">MCIWNDM\_CAN\_RECORD message</span></span>

<span data-ttu-id="8774b-106">**MCIWNDM \_ 可以 \_ 記錄** 訊息，判斷 MCI 裝置是否支援錄製。</span><span class="sxs-lookup"><span data-stu-id="8774b-106">The **MCIWNDM\_CAN\_RECORD** message determines if an MCI device supports recording.</span></span> <span data-ttu-id="8774b-107">您可以使用 [**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="8774b-107">You can send this message explicitly or by using the [**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) macro.</span></span>


```C++
MCIWNDM_CAN_RECORD 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="8774b-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="8774b-108">Return Value</span></span>

<span data-ttu-id="8774b-109">如果裝置支援錄製則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="8774b-109">Returns **TRUE** if the device supports recording or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="8774b-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="8774b-110">Requirements</span></span>



| <span data-ttu-id="8774b-111">需求</span><span class="sxs-lookup"><span data-stu-id="8774b-111">Requirement</span></span> | <span data-ttu-id="8774b-112">值</span><span class="sxs-lookup"><span data-stu-id="8774b-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8774b-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8774b-113">Minimum supported client</span></span><br/> | <span data-ttu-id="8774b-114">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8774b-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="8774b-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8774b-115">Minimum supported server</span></span><br/> | <span data-ttu-id="8774b-116">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8774b-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8774b-117">標頭</span><span class="sxs-lookup"><span data-stu-id="8774b-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="8774b-118"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="8774b-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8774b-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8774b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8774b-120">**MCIWndCanRecord**</span><span class="sxs-lookup"><span data-stu-id="8774b-120">**MCIWndCanRecord**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord)
</dt> </dl>

 

 





