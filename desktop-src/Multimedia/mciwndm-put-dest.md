---
title: 'MCIWNDM_PUT_DEST 訊息 (Vfw .h) '
description: MCIWNDM \_ PUT \_ DEST 訊息會在播放期間，重新定義用於縮放或延展 AVI 檔案影像的目的矩形座標。 您可以使用 MCIWndPutDest 宏明確地傳送此訊息。
ms.assetid: 0b13d473-ef93-41a2-bbb2-09fbf264493e
keywords:
- MCIWNDM_PUT_DEST message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_PUT_DEST
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba150f450f71c3593976f98c9935233918becd70
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686270"
---
# <a name="mciwndm_put_dest-message"></a><span data-ttu-id="c2a2b-105">MCIWNDM \_ PUT \_ DEST 訊息</span><span class="sxs-lookup"><span data-stu-id="c2a2b-105">MCIWNDM\_PUT\_DEST message</span></span>

<span data-ttu-id="c2a2b-106">**MCIWNDM \_ PUT \_ DEST** 訊息會在播放期間，重新定義用於縮放或延展 AVI 檔案影像的目的矩形座標。</span><span class="sxs-lookup"><span data-stu-id="c2a2b-106">The **MCIWNDM\_PUT\_DEST** message redefines the coordinates of the destination rectangle used for zooming or stretching the images of an AVI file during playback.</span></span> <span data-ttu-id="c2a2b-107">您可以使用 [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="c2a2b-107">You can send this message explicitly or by using the [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) macro.</span></span>


```C++
MCIWNDM_PUT_DEST 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a><span data-ttu-id="c2a2b-108">參數</span><span class="sxs-lookup"><span data-stu-id="c2a2b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2a2b-109"><span id="prc"></span><span id="PRC"></span>*中國*</span><span class="sxs-lookup"><span data-stu-id="c2a2b-109"><span id="prc"></span><span id="PRC"></span>*prc*</span></span>
</dt> <dd>

<span data-ttu-id="c2a2b-110">[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，其中包含目的地矩形的座標。</span><span class="sxs-lookup"><span data-stu-id="c2a2b-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure containing the coordinates of the destination rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2a2b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c2a2b-111">Return Value</span></span>

<span data-ttu-id="c2a2b-112">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="c2a2b-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2a2b-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="c2a2b-113">Requirements</span></span>



| <span data-ttu-id="c2a2b-114">需求</span><span class="sxs-lookup"><span data-stu-id="c2a2b-114">Requirement</span></span> | <span data-ttu-id="c2a2b-115">值</span><span class="sxs-lookup"><span data-stu-id="c2a2b-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c2a2b-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c2a2b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c2a2b-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c2a2b-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c2a2b-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c2a2b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c2a2b-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c2a2b-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c2a2b-120">標頭</span><span class="sxs-lookup"><span data-stu-id="c2a2b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2a2b-121"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="c2a2b-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2a2b-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c2a2b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2a2b-123">**MCIWndPutDest**</span><span class="sxs-lookup"><span data-stu-id="c2a2b-123">**MCIWndPutDest**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest)
</dt> </dl>

 

