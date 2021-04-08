---
title: 'MCIWNDM_CAN_EJECT 訊息 (Vfw .h) '
description: MCIWNDM \_ 可以 \_ 退出訊息，以判斷 MCI 裝置是否可以退出媒體。 您可以使用 MCIWndCanEject 宏明確地傳送此訊息。
ms.assetid: e9bd33c4-0ad8-4c0a-8b75-52011b58904d
keywords:
- MCIWNDM_CAN_EJECT message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_EJECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00ba54c9263e23fdd9830be892e4559ae3755c07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686520"
---
# <a name="mciwndm_can_eject-message"></a><span data-ttu-id="30717-105">MCIWNDM \_ 可以 \_ 退出訊息</span><span class="sxs-lookup"><span data-stu-id="30717-105">MCIWNDM\_CAN\_EJECT message</span></span>

<span data-ttu-id="30717-106">**MCIWNDM \_ 可以 \_ 退出** 訊息，以判斷 MCI 裝置是否可以退出媒體。</span><span class="sxs-lookup"><span data-stu-id="30717-106">The **MCIWNDM\_CAN\_EJECT** message determines if an MCI device can eject its media.</span></span> <span data-ttu-id="30717-107">您可以使用 [**MCIWndCanEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="30717-107">You can send this message explicitly or by using the [**MCIWndCanEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject) macro.</span></span>


```C++
MCIWNDM_CAN_EJECT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="30717-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="30717-108">Return Value</span></span>

<span data-ttu-id="30717-109">如果裝置可以退出媒體，則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="30717-109">Returns **TRUE** if the device can eject its media or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="30717-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="30717-110">Requirements</span></span>



| <span data-ttu-id="30717-111">需求</span><span class="sxs-lookup"><span data-stu-id="30717-111">Requirement</span></span> | <span data-ttu-id="30717-112">值</span><span class="sxs-lookup"><span data-stu-id="30717-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="30717-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="30717-113">Minimum supported client</span></span><br/> | <span data-ttu-id="30717-114">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="30717-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="30717-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="30717-115">Minimum supported server</span></span><br/> | <span data-ttu-id="30717-116">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="30717-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="30717-117">標頭</span><span class="sxs-lookup"><span data-stu-id="30717-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="30717-118"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="30717-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30717-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="30717-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30717-120">**MCIWndCanEject**</span><span class="sxs-lookup"><span data-stu-id="30717-120">**MCIWndCanEject**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject)
</dt> </dl>

 

 





