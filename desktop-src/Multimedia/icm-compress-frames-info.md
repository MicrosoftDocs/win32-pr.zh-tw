---
title: 'ICM_COMPRESS_FRAMES_INFO 訊息 (Vfw .h) '
description: ICM \_ 壓縮 \_ 框架 \_ 資訊訊息會通知壓縮驅動程式，以設定暫止壓縮的參數。
ms.assetid: d2f6f3b7-dff6-4fef-a642-cb77b00119af
keywords:
- ICM_COMPRESS_FRAMES_INFO message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_COMPRESS_FRAMES_INFO
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbb6df0eab7706ebfc03a5e3069d4323be26ecdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466473"
---
# <a name="icm_compress_frames_info-message"></a><span data-ttu-id="db9e4-104">ICM \_ 壓縮 \_ 框架 \_ 資訊訊息</span><span class="sxs-lookup"><span data-stu-id="db9e4-104">ICM\_COMPRESS\_FRAMES\_INFO message</span></span>

<span data-ttu-id="db9e4-105">**ICM \_ 壓縮 \_ 框架 \_ 資訊** 訊息會通知壓縮驅動程式，以設定暫止壓縮的參數。</span><span class="sxs-lookup"><span data-stu-id="db9e4-105">The **ICM\_COMPRESS\_FRAMES\_INFO** message notifies a compression driver to set the parameters for the pending compression.</span></span>


```C++
ICM_COMPRESS_FRAMES_INFO 
wParam = (DWORD) (LPVOID) &icf; 
lParam = sizeof(ICCOMPRESSFRAMES); 
```



## <a name="parameters"></a><span data-ttu-id="db9e4-106">參數</span><span class="sxs-lookup"><span data-stu-id="db9e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db9e4-107"><span id="icf"></span><span id="ICF"></span>*Icf*</span><span class="sxs-lookup"><span data-stu-id="db9e4-107"><span id="icf"></span><span id="ICF"></span>*icf*</span></span>
</dt> <dd>

<span data-ttu-id="db9e4-108">[**ICCOMPRESSFRAMES**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="db9e4-108">Pointer to an [**ICCOMPRESSFRAMES**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes) structure.</span></span> <span data-ttu-id="db9e4-109">此 **結構** 的 **PutData** 成員不會與此訊息一起使用。</span><span class="sxs-lookup"><span data-stu-id="db9e4-109">The **GetData** and **PutData** members of this structure are not used with this message.</span></span>

</dd> <dt>

<span data-ttu-id="db9e4-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="db9e4-110"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="db9e4-111">[**ICCOMPRESSFRAMES**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes)的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="db9e4-111">Size, in bytes, of [**ICCOMPRESSFRAMES**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db9e4-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="db9e4-112">Return Value</span></span>

<span data-ttu-id="db9e4-113">如果成功，則會傳回 ICERR \_ OK，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="db9e4-113">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="db9e4-114">備註</span><span class="sxs-lookup"><span data-stu-id="db9e4-114">Remarks</span></span>

<span data-ttu-id="db9e4-115">壓縮程式可以使用此訊息來判斷在壓縮時要為每個框架配置多少空間。</span><span class="sxs-lookup"><span data-stu-id="db9e4-115">A compressor can use this message to determine how much space to allocate for each frame while compressing.</span></span>

## <a name="requirements"></a><span data-ttu-id="db9e4-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="db9e4-116">Requirements</span></span>



| <span data-ttu-id="db9e4-117">需求</span><span class="sxs-lookup"><span data-stu-id="db9e4-117">Requirement</span></span> | <span data-ttu-id="db9e4-118">值</span><span class="sxs-lookup"><span data-stu-id="db9e4-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="db9e4-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="db9e4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="db9e4-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="db9e4-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="db9e4-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="db9e4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="db9e4-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="db9e4-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="db9e4-123">標頭</span><span class="sxs-lookup"><span data-stu-id="db9e4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="db9e4-124"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="db9e4-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db9e4-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="db9e4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db9e4-126">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="db9e4-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="db9e4-127">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="db9e4-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





