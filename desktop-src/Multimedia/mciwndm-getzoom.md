---
title: 'MCIWNDM_GETZOOM 訊息 (Vfw .h) '
description: MCIWNDM \_ GETZOOM 訊息會抓取 MCI 裝置所使用的目前縮放值。 您可以使用 MCIWndGetZoom 宏明確地傳送此訊息。
ms.assetid: 92db8df2-515a-4616-a0f5-245d466ba379
keywords:
- MCIWNDM_GETZOOM message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_GETZOOM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcb4ae1883787f1b86dcc17f2d4a3e0e0ee29ced
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464981"
---
# <a name="mciwndm_getzoom-message"></a><span data-ttu-id="afaee-105">MCIWNDM \_ GETZOOM 訊息</span><span class="sxs-lookup"><span data-stu-id="afaee-105">MCIWNDM\_GETZOOM message</span></span>

<span data-ttu-id="afaee-106">**MCIWNDM \_ GETZOOM** 訊息會抓取 MCI 裝置所使用的目前縮放值。</span><span class="sxs-lookup"><span data-stu-id="afaee-106">The **MCIWNDM\_GETZOOM** message retrieves the current zoom value used by an MCI device.</span></span> <span data-ttu-id="afaee-107">您可以使用 [**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="afaee-107">You can send this message explicitly or by using the [**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) macro.</span></span>


```C++
MCIWNDM_GETZOOM 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="afaee-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="afaee-108">Return Value</span></span>

<span data-ttu-id="afaee-109">傳回與 [**MCIWNDM \_ SETZOOM**](mciwndm-setzoom.md)搭配使用的最新值。</span><span class="sxs-lookup"><span data-stu-id="afaee-109">Returns the most recent values used with [**MCIWNDM\_SETZOOM**](mciwndm-setzoom.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="afaee-110">備註</span><span class="sxs-lookup"><span data-stu-id="afaee-110">Remarks</span></span>

<span data-ttu-id="afaee-111">傳回值100表示影像未縮放。</span><span class="sxs-lookup"><span data-stu-id="afaee-111">A return value of 100 indicates the image is not zoomed.</span></span> <span data-ttu-id="afaee-112">值為200表示影像會放大至其原始大小的兩倍。</span><span class="sxs-lookup"><span data-stu-id="afaee-112">A value of 200 indicates the image is enlarged to twice its original size.</span></span> <span data-ttu-id="afaee-113">值為50表示影像縮減為其原始大小的一半。</span><span class="sxs-lookup"><span data-stu-id="afaee-113">A value of 50 indicates the image is reduced to half its original size.</span></span>

## <a name="requirements"></a><span data-ttu-id="afaee-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="afaee-114">Requirements</span></span>



| <span data-ttu-id="afaee-115">需求</span><span class="sxs-lookup"><span data-stu-id="afaee-115">Requirement</span></span> | <span data-ttu-id="afaee-116">值</span><span class="sxs-lookup"><span data-stu-id="afaee-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="afaee-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="afaee-117">Minimum supported client</span></span><br/> | <span data-ttu-id="afaee-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="afaee-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="afaee-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="afaee-119">Minimum supported server</span></span><br/> | <span data-ttu-id="afaee-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="afaee-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="afaee-121">標頭</span><span class="sxs-lookup"><span data-stu-id="afaee-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="afaee-122"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="afaee-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afaee-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="afaee-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afaee-124">**MCIWndGetZoom**</span><span class="sxs-lookup"><span data-stu-id="afaee-124">**MCIWndGetZoom**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom)
</dt> <dt>

[<span data-ttu-id="afaee-125">**MCIWNDM \_ SETZOOM**</span><span class="sxs-lookup"><span data-stu-id="afaee-125">**MCIWNDM\_SETZOOM**</span></span>](mciwndm-setzoom.md)
</dt> </dl>

 

 





