---
title: 'MCIWNDM_SETZOOM 訊息 (Vfw .h) '
description: MCIWNDM \_ SETZOOM 訊息會根據縮放因數調整影片影像的大小。 這個 marco 會調整 MCIWnd 視窗的大小，同時維持固定的長寬比。 您可以使用 MCIWndSetZoom 宏明確地傳送此訊息。
ms.assetid: c899b678-5ba7-4f0a-9ef9-c5370b3b4ea8
keywords:
- MCIWNDM_SETZOOM message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_SETZOOM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80ecb513735c4e62266892e8ad55c7bf5daca151
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464508"
---
# <a name="mciwndm_setzoom-message"></a><span data-ttu-id="2ae28-106">MCIWNDM \_ SETZOOM 訊息</span><span class="sxs-lookup"><span data-stu-id="2ae28-106">MCIWNDM\_SETZOOM message</span></span>

<span data-ttu-id="2ae28-107">**MCIWNDM \_ SETZOOM** 訊息會根據縮放因數調整影片影像的大小。</span><span class="sxs-lookup"><span data-stu-id="2ae28-107">The **MCIWNDM\_SETZOOM** message resizes a video image according to a zoom factor.</span></span> <span data-ttu-id="2ae28-108">這個 marco 會調整 MCIWnd 視窗的大小，同時維持固定的長寬比。</span><span class="sxs-lookup"><span data-stu-id="2ae28-108">This marco adjusts the size of an MCIWnd window while maintaining a constant aspect ratio.</span></span> <span data-ttu-id="2ae28-109">您可以使用 [**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="2ae28-109">You can send this message explicitly or by using the [**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) macro.</span></span>


```C++
MCIWNDM_SETZOOM 
wParam = 0; 
lParam = (LPARAM) (UINT) iZoom; 
```



## <a name="parameters"></a><span data-ttu-id="2ae28-110">參數</span><span class="sxs-lookup"><span data-stu-id="2ae28-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ae28-111"><span id="iZoom"></span><span id="izoom"></span><span id="IZOOM"></span>*iZoom*</span><span class="sxs-lookup"><span data-stu-id="2ae28-111"><span id="iZoom"></span><span id="izoom"></span><span id="IZOOM"></span>*iZoom*</span></span>
</dt> <dd>

<span data-ttu-id="2ae28-112">以原始影像的百分比表示的縮放因數。</span><span class="sxs-lookup"><span data-stu-id="2ae28-112">Zoom factor expressed as a percentage of the original image.</span></span> <span data-ttu-id="2ae28-113">指定100以其所撰寫的大小顯示影像，200以在其正常大小的兩倍顯示影像，或以50顯示影像的大小為一半。</span><span class="sxs-lookup"><span data-stu-id="2ae28-113">Specify 100 to display the image at its authored size, 200 to display the image at twice its normal size, or 50 to display the image at half its normal size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ae28-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="2ae28-114">Return Value</span></span>

<span data-ttu-id="2ae28-115">此訊息不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="2ae28-115">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ae28-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="2ae28-116">Requirements</span></span>



| <span data-ttu-id="2ae28-117">需求</span><span class="sxs-lookup"><span data-stu-id="2ae28-117">Requirement</span></span> | <span data-ttu-id="2ae28-118">值</span><span class="sxs-lookup"><span data-stu-id="2ae28-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2ae28-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2ae28-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2ae28-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2ae28-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2ae28-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2ae28-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2ae28-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2ae28-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2ae28-123">標頭</span><span class="sxs-lookup"><span data-stu-id="2ae28-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ae28-124"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="2ae28-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ae28-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2ae28-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ae28-126">**MCIWndSetZoom**</span><span class="sxs-lookup"><span data-stu-id="2ae28-126">**MCIWndSetZoom**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom)
</dt> </dl>

 

 





