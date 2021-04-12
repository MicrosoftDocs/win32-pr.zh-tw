---
title: 'ICM_GETDEFAULTQUALITY 訊息 (Vfw .h) '
description: ICM \_ GETDEFAULTQUALITY 訊息會查詢視訊壓縮驅動程式，以提供其預設品質設定。 您可以使用 ICGetDefaultQuality 宏明確地傳送此訊息。
ms.assetid: bba7f451-52c2-4684-a7c9-e4b05cb946c5
keywords:
- ICM_GETDEFAULTQUALITY message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_GETDEFAULTQUALITY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4350539851ca720e3538d297f955a56fedfc4a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464629"
---
# <a name="icm_getdefaultquality-message"></a><span data-ttu-id="2ce42-105">ICM \_ GETDEFAULTQUALITY 訊息</span><span class="sxs-lookup"><span data-stu-id="2ce42-105">ICM\_GETDEFAULTQUALITY message</span></span>

<span data-ttu-id="2ce42-106">**ICM \_ GETDEFAULTQUALITY** 訊息會查詢視訊壓縮驅動程式，以提供其預設品質設定。</span><span class="sxs-lookup"><span data-stu-id="2ce42-106">The **ICM\_GETDEFAULTQUALITY** message queries a video compression driver to provide its default quality setting.</span></span> <span data-ttu-id="2ce42-107">您可以使用 [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="2ce42-107">You can send this message explicitly or by using the [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) macro.</span></span>


```C++
ICM_GETDEFAULTQUALITY 
wParam = (DWORD_PTR) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="2ce42-108">參數</span><span class="sxs-lookup"><span data-stu-id="2ce42-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ce42-109"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span><span class="sxs-lookup"><span data-stu-id="2ce42-109"><span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*</span></span>
</dt> <dd>

<span data-ttu-id="2ce42-110">包含預設品質值的位址。</span><span class="sxs-lookup"><span data-stu-id="2ce42-110">Address to contain the default quality value.</span></span> <span data-ttu-id="2ce42-111">品質值的範圍是從0到10000。</span><span class="sxs-lookup"><span data-stu-id="2ce42-111">Quality values range from 0 to 10,000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ce42-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="2ce42-112">Return Value</span></span>

<span data-ttu-id="2ce42-113">\_如果驅動程式支援此訊息或 ICERR 不支援，則會傳回 ICERR OK \_ 。</span><span class="sxs-lookup"><span data-stu-id="2ce42-113">Returns ICERR\_OK if the driver supports this message or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ce42-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="2ce42-114">Requirements</span></span>



| <span data-ttu-id="2ce42-115">需求</span><span class="sxs-lookup"><span data-stu-id="2ce42-115">Requirement</span></span> | <span data-ttu-id="2ce42-116">值</span><span class="sxs-lookup"><span data-stu-id="2ce42-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2ce42-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2ce42-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2ce42-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2ce42-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2ce42-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2ce42-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2ce42-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2ce42-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2ce42-121">標頭</span><span class="sxs-lookup"><span data-stu-id="2ce42-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ce42-122"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="2ce42-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ce42-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2ce42-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ce42-124">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="2ce42-124">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="2ce42-125">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="2ce42-125">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





