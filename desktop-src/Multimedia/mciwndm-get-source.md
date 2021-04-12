---
title: 'MCIWNDM_GET_SOURCE 訊息 (Vfw .h) '
description: MCIWNDM \_ 取得 \_ 來源訊息會抓取來源矩形的座標，此來源矩形用於在播放期間裁剪 AVI 檔案的影像。 您可以使用 MCIWndGetSource 宏明確地傳送此訊息。
ms.assetid: d5f25926-5a3d-412e-8248-fbf307583757
keywords:
- MCIWNDM_GET_SOURCE message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_GET_SOURCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85147182d06386efed73229fcdd6c75372244fd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385025"
---
# <a name="mciwndm_get_source-message"></a><span data-ttu-id="3b334-105">MCIWNDM \_ 取得 \_ 來源訊息</span><span class="sxs-lookup"><span data-stu-id="3b334-105">MCIWNDM\_GET\_SOURCE message</span></span>

<span data-ttu-id="3b334-106">**MCIWNDM \_ 取得 \_ 來源** 訊息會抓取來源矩形的座標，此來源矩形用於在播放期間裁剪 AVI 檔案的影像。</span><span class="sxs-lookup"><span data-stu-id="3b334-106">The **MCIWNDM\_GET\_SOURCE** message retrieves the coordinates of the source rectangle used for cropping the images of an AVI file during playback.</span></span> <span data-ttu-id="3b334-107">您可以使用 [**MCIWndGetSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="3b334-107">You can send this message explicitly or by using the [**MCIWndGetSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) macro.</span></span>


```C++
MCIWNDM_GET_SOURCE 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a><span data-ttu-id="3b334-108">參數</span><span class="sxs-lookup"><span data-stu-id="3b334-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b334-109"><span id="prc"></span><span id="PRC"></span>*中國*</span><span class="sxs-lookup"><span data-stu-id="3b334-109"><span id="prc"></span><span id="PRC"></span>*prc*</span></span>
</dt> <dd>

<span data-ttu-id="3b334-110">[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，包含來源矩形的座標。</span><span class="sxs-lookup"><span data-stu-id="3b334-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to contain the coordinates of the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b334-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="3b334-111">Return Value</span></span>

<span data-ttu-id="3b334-112">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="3b334-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b334-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="3b334-113">Requirements</span></span>



| <span data-ttu-id="3b334-114">需求</span><span class="sxs-lookup"><span data-stu-id="3b334-114">Requirement</span></span> | <span data-ttu-id="3b334-115">值</span><span class="sxs-lookup"><span data-stu-id="3b334-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3b334-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3b334-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3b334-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3b334-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3b334-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3b334-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3b334-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3b334-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3b334-120">標頭</span><span class="sxs-lookup"><span data-stu-id="3b334-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b334-121"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="3b334-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b334-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b334-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b334-123">**MCIWndGetSource**</span><span class="sxs-lookup"><span data-stu-id="3b334-123">**MCIWndGetSource**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource)
</dt> </dl>

 

