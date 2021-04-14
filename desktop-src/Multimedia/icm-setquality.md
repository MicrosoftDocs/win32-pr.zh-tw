---
title: 'ICM_SETQUALITY 訊息 (Vfw .h) '
description: ICM \_ SETQUALITY 訊息提供的視訊壓縮驅動程式具有要在壓縮期間使用的品質等級。
ms.assetid: 487ff1de-7178-440a-b38d-0b82a30d7297
keywords:
- ICM_SETQUALITY message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_SETQUALITY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a1523996ad336e64d4b34143cc26cd8d0937d5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385298"
---
# <a name="icm_setquality-message"></a><span data-ttu-id="0ddda-104">ICM \_ SETQUALITY 訊息</span><span class="sxs-lookup"><span data-stu-id="0ddda-104">ICM\_SETQUALITY message</span></span>

<span data-ttu-id="0ddda-105">**ICM \_ SETQUALITY** 訊息提供的視訊壓縮驅動程式具有要在壓縮期間使用的品質等級。</span><span class="sxs-lookup"><span data-stu-id="0ddda-105">The **ICM\_SETQUALITY** message provides a video compression driver with a quality level to use during compression.</span></span>


```C++
ICM_SETQUALITY 
wParam = (DWORD) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="0ddda-106">參數</span><span class="sxs-lookup"><span data-stu-id="0ddda-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ddda-107"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span><span class="sxs-lookup"><span data-stu-id="0ddda-107"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span></span>
</dt> <dd>

<span data-ttu-id="0ddda-108">新的品質值。</span><span class="sxs-lookup"><span data-stu-id="0ddda-108">New quality value.</span></span> <span data-ttu-id="0ddda-109">品質值的範圍是從0到10000。</span><span class="sxs-lookup"><span data-stu-id="0ddda-109">Quality values range from 0 to 10,000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ddda-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="0ddda-110">Return Value</span></span>

<span data-ttu-id="0ddda-111">\_如果驅動程式支援此訊息或 ICERR 不支援，則會傳回 ICERR OK \_ 。</span><span class="sxs-lookup"><span data-stu-id="0ddda-111">Returns ICERR\_OK if the driver supports this message or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ddda-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="0ddda-112">Requirements</span></span>



| <span data-ttu-id="0ddda-113">需求</span><span class="sxs-lookup"><span data-stu-id="0ddda-113">Requirement</span></span> | <span data-ttu-id="0ddda-114">值</span><span class="sxs-lookup"><span data-stu-id="0ddda-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0ddda-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0ddda-115">Minimum supported client</span></span><br/> | <span data-ttu-id="0ddda-116">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0ddda-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="0ddda-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0ddda-117">Minimum supported server</span></span><br/> | <span data-ttu-id="0ddda-118">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0ddda-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0ddda-119">標頭</span><span class="sxs-lookup"><span data-stu-id="0ddda-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ddda-120"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="0ddda-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ddda-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0ddda-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ddda-122">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="0ddda-122">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="0ddda-123">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="0ddda-123">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





