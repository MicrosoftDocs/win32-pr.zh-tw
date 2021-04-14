---
title: 'ICM_GETDEFAULTKEYFRAMERATE 訊息 (Vfw .h) '
description: ICM \_ GETDEFAULTKEYFRAMERATE 訊息會查詢視訊壓縮驅動程式，以取得其預設 (或慣用) 的主要畫面格間距。 您可以使用 ICGetDefaulteyFrameRate 宏明確地傳送此訊息。
ms.assetid: 2ebe37cc-3ec2-4b52-bd8f-71c44b704647
keywords:
- ICM_GETDEFAULTKEYFRAMERATE message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_GETDEFAULTKEYFRAMERATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64f2796ca1c2de10222330217a0e1deb7883baa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384770"
---
# <a name="icm_getdefaultkeyframerate-message"></a><span data-ttu-id="803c6-105">ICM \_ GETDEFAULTKEYFRAMERATE 訊息</span><span class="sxs-lookup"><span data-stu-id="803c6-105">ICM\_GETDEFAULTKEYFRAMERATE message</span></span>

<span data-ttu-id="803c6-106">**ICM \_ GETDEFAULTKEYFRAMERATE** 訊息會查詢視訊壓縮驅動程式，以取得其預設 (或慣用) 的主要畫面格間距。</span><span class="sxs-lookup"><span data-stu-id="803c6-106">The **ICM\_GETDEFAULTKEYFRAMERATE** message queries a video compression driver for its default (or preferred) key-frame spacing.</span></span> <span data-ttu-id="803c6-107">您可以使用 [**ICGetDefaulteyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="803c6-107">You can send this message explicitly or by using the [**ICGetDefaulteyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) macro.</span></span>


```C++
ICM_GETDEFAULTKEYFRAMERATE 
wParam = (DWORD_PTR) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="803c6-108">參數</span><span class="sxs-lookup"><span data-stu-id="803c6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="803c6-109"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span><span class="sxs-lookup"><span data-stu-id="803c6-109"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span></span>
</dt> <dd>

<span data-ttu-id="803c6-110">要包含慣用主要畫面格間距的位址。</span><span class="sxs-lookup"><span data-stu-id="803c6-110">Address to contain the preferred key-frame spacing.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="803c6-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="803c6-111">Return Value</span></span>

<span data-ttu-id="803c6-112">\_如果驅動程式支援此訊息或 ICERR 不支援，則會傳回 ICERR OK \_ 。</span><span class="sxs-lookup"><span data-stu-id="803c6-112">Returns ICERR\_OK if the driver supports this message or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="803c6-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="803c6-113">Requirements</span></span>



| <span data-ttu-id="803c6-114">需求</span><span class="sxs-lookup"><span data-stu-id="803c6-114">Requirement</span></span> | <span data-ttu-id="803c6-115">值</span><span class="sxs-lookup"><span data-stu-id="803c6-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="803c6-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="803c6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="803c6-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="803c6-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="803c6-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="803c6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="803c6-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="803c6-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="803c6-120">標頭</span><span class="sxs-lookup"><span data-stu-id="803c6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="803c6-121"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="803c6-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="803c6-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="803c6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="803c6-123">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="803c6-123">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="803c6-124">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="803c6-124">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





