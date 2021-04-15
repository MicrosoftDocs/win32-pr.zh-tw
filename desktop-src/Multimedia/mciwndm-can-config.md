---
title: 'MCIWNDM_CAN_CONFIG 訊息 (Vfw .h) '
description: MCIWNDM \_ 可設定 \_ 訊息可判斷 MCI 裝置是否可顯示 [設定] 對話方塊。 您可以使用 MCIWndCanConfig 宏明確地傳送此訊息。
ms.assetid: f1eb22a8-d0fc-4d2c-a414-392e560cfbed
keywords:
- MCIWNDM_CAN_CONFIG message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_CONFIG
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 816a8c1dfaec6fc7d7854f8873ce05e74e4de6bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466921"
---
# <a name="mciwndm_can_config-message"></a><span data-ttu-id="ecd12-105">MCIWNDM \_ 可以設定 \_ 訊息</span><span class="sxs-lookup"><span data-stu-id="ecd12-105">MCIWNDM\_CAN\_CONFIG message</span></span>

<span data-ttu-id="ecd12-106">**MCIWNDM \_ 可 \_** 設定訊息可判斷 MCI 裝置是否可顯示 [設定] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="ecd12-106">The **MCIWNDM\_CAN\_CONFIG** message determines if an MCI device can display a configuration dialog box.</span></span> <span data-ttu-id="ecd12-107">您可以使用 [**MCIWndCanConfig**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="ecd12-107">You can send this message explicitly or by using the [**MCIWndCanConfig**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig) macro.</span></span>


```C++
MCIWNDM_CAN_CONFIG 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="ecd12-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="ecd12-108">Return Value</span></span>

<span data-ttu-id="ecd12-109">如果裝置支援設定，則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="ecd12-109">Returns **TRUE** if the device supports configuration or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecd12-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="ecd12-110">Requirements</span></span>



| <span data-ttu-id="ecd12-111">需求</span><span class="sxs-lookup"><span data-stu-id="ecd12-111">Requirement</span></span> | <span data-ttu-id="ecd12-112">值</span><span class="sxs-lookup"><span data-stu-id="ecd12-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ecd12-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ecd12-113">Minimum supported client</span></span><br/> | <span data-ttu-id="ecd12-114">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ecd12-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ecd12-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ecd12-115">Minimum supported server</span></span><br/> | <span data-ttu-id="ecd12-116">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ecd12-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ecd12-117">標頭</span><span class="sxs-lookup"><span data-stu-id="ecd12-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecd12-118"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="ecd12-118"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecd12-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ecd12-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecd12-120">**MCIWndCanConfig**</span><span class="sxs-lookup"><span data-stu-id="ecd12-120">**MCIWndCanConfig**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig)
</dt> </dl>

 

 





