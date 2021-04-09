---
title: 'ICM_GETQUALITY 訊息 (Vfw .h) '
description: ICM \_ GETQUALITY 訊息會查詢視訊壓縮驅動程式，以傳回其目前的品質設定。
ms.assetid: 8da99a26-7b2a-4118-89e1-7485915cbdc9
keywords:
- ICM_GETQUALITY message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_GETQUALITY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c4fa2a26e1fe5fa111585ce0a59422a2fe9b072
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935145"
---
# <a name="icm_getquality-message"></a><span data-ttu-id="ec5a5-104">ICM \_ GETQUALITY 訊息</span><span class="sxs-lookup"><span data-stu-id="ec5a5-104">ICM\_GETQUALITY message</span></span>

<span data-ttu-id="ec5a5-105">**ICM \_ GETQUALITY** 訊息會查詢視訊壓縮驅動程式，以傳回其目前的品質設定。</span><span class="sxs-lookup"><span data-stu-id="ec5a5-105">The **ICM\_GETQUALITY** message queries a video compression driver to return its current quality setting.</span></span>


```C++
ICM_GETQUALITY 
wParam = (DWORD) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="ec5a5-106">參數</span><span class="sxs-lookup"><span data-stu-id="ec5a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec5a5-107"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span><span class="sxs-lookup"><span data-stu-id="ec5a5-107"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span></span>
</dt> <dd>

<span data-ttu-id="ec5a5-108">包含目前品質值的位址。</span><span class="sxs-lookup"><span data-stu-id="ec5a5-108">Address to contain the current quality value.</span></span> <span data-ttu-id="ec5a5-109">品質值的範圍是從0到10000。</span><span class="sxs-lookup"><span data-stu-id="ec5a5-109">Quality values range from 0 to 10,000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec5a5-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="ec5a5-110">Return Value</span></span>

<span data-ttu-id="ec5a5-111">\_如果驅動程式支援此訊息或 ICERR 不支援，則會傳回 ICERR OK \_ 。</span><span class="sxs-lookup"><span data-stu-id="ec5a5-111">Returns ICERR\_OK if the driver supports this message or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec5a5-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec5a5-112">Requirements</span></span>



| <span data-ttu-id="ec5a5-113">需求</span><span class="sxs-lookup"><span data-stu-id="ec5a5-113">Requirement</span></span> | <span data-ttu-id="ec5a5-114">值</span><span class="sxs-lookup"><span data-stu-id="ec5a5-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ec5a5-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ec5a5-115">Minimum supported client</span></span><br/> | <span data-ttu-id="ec5a5-116">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec5a5-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ec5a5-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ec5a5-117">Minimum supported server</span></span><br/> | <span data-ttu-id="ec5a5-118">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec5a5-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ec5a5-119">標頭</span><span class="sxs-lookup"><span data-stu-id="ec5a5-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec5a5-120"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="ec5a5-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec5a5-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec5a5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec5a5-122">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="ec5a5-122">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="ec5a5-123">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="ec5a5-123">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





