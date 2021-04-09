---
title: 'MCIWNDM_GET_DEST 訊息 (Vfw .h) '
description: MCIWNDM \_ 取得目的地訊息會抓取在 \_ 播放期間用來縮放或延展 AVI 檔案影像的目的矩形座標。 您可以使用 MCIWndGetDest 宏明確地傳送此訊息。
ms.assetid: d4d8a3eb-aad4-4435-a23b-7a9c55fc194d
keywords:
- MCIWNDM_GET_DEST message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_GET_DEST
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab5f16b434caef56e6c6aa97bfd767770dc05ee1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024563"
---
# <a name="mciwndm_get_dest-message"></a><span data-ttu-id="962c1-105">MCIWNDM \_ 取得 \_ 目的地訊息</span><span class="sxs-lookup"><span data-stu-id="962c1-105">MCIWNDM\_GET\_DEST message</span></span>

<span data-ttu-id="962c1-106">**MCIWNDM \_ 取得 \_** 目的地訊息會抓取在播放期間用來縮放或延展 AVI 檔案影像的目的矩形座標。</span><span class="sxs-lookup"><span data-stu-id="962c1-106">The **MCIWNDM\_GET\_DEST** message retrieves the coordinates of the destination rectangle used for zooming or stretching the images of an AVI file during playback.</span></span> <span data-ttu-id="962c1-107">您可以使用 [**MCIWndGetDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="962c1-107">You can send this message explicitly or by using the [**MCIWndGetDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest) macro.</span></span>


```C++
MCIWNDM_GET_DEST 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a><span data-ttu-id="962c1-108">參數</span><span class="sxs-lookup"><span data-stu-id="962c1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="962c1-109"><span id="prc"></span><span id="PRC"></span>*中國*</span><span class="sxs-lookup"><span data-stu-id="962c1-109"><span id="prc"></span><span id="PRC"></span>*prc*</span></span>
</dt> <dd>

<span data-ttu-id="962c1-110">[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，用來傳回目的地矩形的座標。</span><span class="sxs-lookup"><span data-stu-id="962c1-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to return the coordinates of the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="962c1-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="962c1-111">Return Value</span></span>

<span data-ttu-id="962c1-112">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="962c1-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="962c1-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="962c1-113">Requirements</span></span>



| <span data-ttu-id="962c1-114">需求</span><span class="sxs-lookup"><span data-stu-id="962c1-114">Requirement</span></span> | <span data-ttu-id="962c1-115">值</span><span class="sxs-lookup"><span data-stu-id="962c1-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="962c1-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="962c1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="962c1-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="962c1-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="962c1-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="962c1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="962c1-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="962c1-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="962c1-120">標頭</span><span class="sxs-lookup"><span data-stu-id="962c1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="962c1-121"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="962c1-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="962c1-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="962c1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="962c1-123">**MCIWndGetDest**</span><span class="sxs-lookup"><span data-stu-id="962c1-123">**MCIWndGetDest**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest)
</dt> </dl>

 

