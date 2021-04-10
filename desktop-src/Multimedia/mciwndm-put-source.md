---
title: 'MCIWNDM_PUT_SOURCE 訊息 (Vfw .h) '
description: MCIWNDM \_ PUT \_ 來源訊息會重新定義來源矩形的座標，在播放期間用於裁剪 AVI 檔案的影像。 您可以使用 MCIWndPutSource 宏明確地傳送此訊息。
ms.assetid: cff95139-0302-4db3-bf2e-559e75257e85
keywords:
- MCIWNDM_PUT_SOURCE message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_PUT_SOURCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5407f420b8def6dda9795e87eb68943c9373b143
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685486"
---
# <a name="mciwndm_put_source-message"></a><span data-ttu-id="ed417-105">MCIWNDM \_ PUT \_ 來源訊息</span><span class="sxs-lookup"><span data-stu-id="ed417-105">MCIWNDM\_PUT\_SOURCE message</span></span>

<span data-ttu-id="ed417-106">**MCIWNDM \_ PUT \_ 來源** 訊息會重新定義來源矩形的座標，在播放期間用於裁剪 AVI 檔案的影像。</span><span class="sxs-lookup"><span data-stu-id="ed417-106">The **MCIWNDM\_PUT\_SOURCE** message redefines the coordinates of the source rectangle used for cropping the images of an AVI file during playback.</span></span> <span data-ttu-id="ed417-107">您可以使用 [**MCIWndPutSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="ed417-107">You can send this message explicitly or by using the [**MCIWndPutSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) macro.</span></span>


```C++
MCIWNDM_PUT_SOURCE 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a><span data-ttu-id="ed417-108">參數</span><span class="sxs-lookup"><span data-stu-id="ed417-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed417-109"><span id="prc"></span><span id="PRC"></span>*中國*</span><span class="sxs-lookup"><span data-stu-id="ed417-109"><span id="prc"></span><span id="PRC"></span>*prc*</span></span>
</dt> <dd>

<span data-ttu-id="ed417-110">[矩形](/previous-versions//ms536136(v=vs.85))結構的指標，其中包含來源矩形的座標。</span><span class="sxs-lookup"><span data-stu-id="ed417-110">Pointer to a [RECT](/previous-versions//ms536136(v=vs.85)) structure containing the coordinates of the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed417-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="ed417-111">Return Value</span></span>

<span data-ttu-id="ed417-112">如果成功則傳回零，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="ed417-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed417-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="ed417-113">Requirements</span></span>



| <span data-ttu-id="ed417-114">需求</span><span class="sxs-lookup"><span data-stu-id="ed417-114">Requirement</span></span> | <span data-ttu-id="ed417-115">值</span><span class="sxs-lookup"><span data-stu-id="ed417-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ed417-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ed417-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ed417-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ed417-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ed417-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ed417-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ed417-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ed417-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ed417-120">標頭</span><span class="sxs-lookup"><span data-stu-id="ed417-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed417-121"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="ed417-121"><dt>Vfw.h</dt></span></span> </dl> |



 

