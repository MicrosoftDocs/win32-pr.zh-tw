---
title: 'MCIWNDM_CAN_SAVE 訊息 (Vfw .h) '
description: MCIWNDM \_ 可以 \_ 儲存訊息，以判斷 MCI 裝置是否可以儲存資料。 您可以使用 MCIWndCanSave 宏明確地傳送此訊息。
ms.assetid: b4e27190-b095-494b-9ed3-10653bea187b
keywords:
- MCIWNDM_CAN_SAVE message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_SAVE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11b60b8a5d93ac80befc8beeb6665399efe44f1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464617"
---
# <a name="mciwndm_can_save-message"></a><span data-ttu-id="8119f-105">MCIWNDM \_ 可以 \_ 儲存訊息</span><span class="sxs-lookup"><span data-stu-id="8119f-105">MCIWNDM\_CAN\_SAVE message</span></span>

<span data-ttu-id="8119f-106">**MCIWNDM \_ 可以 \_ 儲存** 訊息，以判斷 MCI 裝置是否可以儲存資料。</span><span class="sxs-lookup"><span data-stu-id="8119f-106">The **MCIWNDM\_CAN\_SAVE** message determines if an MCI device can save data.</span></span> <span data-ttu-id="8119f-107">您可以使用 [**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="8119f-107">You can send this message explicitly or by using the [**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave) macro.</span></span>


```C++
MCIWNDM_CAN_SAVE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="8119f-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="8119f-108">Return Value</span></span>

<span data-ttu-id="8119f-109">如果裝置支援儲存，則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="8119f-109">Returns **TRUE** if the device supports saving or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="8119f-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="8119f-110">Requirements</span></span>



| <span data-ttu-id="8119f-111">需求</span><span class="sxs-lookup"><span data-stu-id="8119f-111">Requirement</span></span> | <span data-ttu-id="8119f-112">值</span><span class="sxs-lookup"><span data-stu-id="8119f-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8119f-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8119f-113">Minimum supported client</span></span><br/> | <span data-ttu-id="8119f-114">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8119f-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="8119f-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8119f-115">Minimum supported server</span></span><br/> | <span data-ttu-id="8119f-116">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8119f-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8119f-117">標頭</span><span class="sxs-lookup"><span data-stu-id="8119f-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="8119f-118"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="8119f-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8119f-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8119f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8119f-120">**MCIWndCanSave**</span><span class="sxs-lookup"><span data-stu-id="8119f-120">**MCIWndCanSave**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave)
</dt> </dl>

 

 





