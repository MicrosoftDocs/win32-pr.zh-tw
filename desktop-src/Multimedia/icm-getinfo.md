---
title: 'ICM_GETINFO 訊息 (Vfw .h) '
description: ICM \_ GETINFO 訊息會查詢視訊壓縮驅動程式，以在 ICINFO 結構中傳回本身的描述。
ms.assetid: 8029f247-9777-4a34-9e84-908482094493
keywords:
- ICM_GETINFO message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_GETINFO
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 634803b7dd9a3b8900c35fabedcadb99908c2b31
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966120"
---
# <a name="icm_getinfo-message"></a><span data-ttu-id="b8b75-104">ICM \_ GETINFO 訊息</span><span class="sxs-lookup"><span data-stu-id="b8b75-104">ICM\_GETINFO message</span></span>

<span data-ttu-id="b8b75-105">**ICM \_ GETINFO** 訊息會查詢視訊壓縮驅動程式，以在 [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo)結構中傳回本身的描述。</span><span class="sxs-lookup"><span data-stu-id="b8b75-105">The **ICM\_GETINFO** message queries a video compression driver to return a description of itself in an [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) structure.</span></span>


```C++
ICM_GETINFO 
wParam = (DWORD) (LPVOID) lpicinfo; 
lParam = sizeof(ICINFO); 
```



## <a name="parameters"></a><span data-ttu-id="b8b75-106">參數</span><span class="sxs-lookup"><span data-stu-id="b8b75-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8b75-107"><span id="lpicinfo"></span><span id="LPICINFO"></span>*lpicinfo*</span><span class="sxs-lookup"><span data-stu-id="b8b75-107"><span id="lpicinfo"></span><span id="LPICINFO"></span>*lpicinfo*</span></span>
</dt> <dd>

<span data-ttu-id="b8b75-108">要包含資訊之 **ICINFO** 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="b8b75-108">Pointer to an **ICINFO** structure to contain information.</span></span>

</dd> <dt>

<span data-ttu-id="b8b75-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="b8b75-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="b8b75-110">**ICINFO** 的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="b8b75-110">Size, in bytes, of **ICINFO**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8b75-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b8b75-111">Return Value</span></span>

<span data-ttu-id="b8b75-112">傳回 [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) 的大小（以位元組為單位），如果發生錯誤則傳回零。</span><span class="sxs-lookup"><span data-stu-id="b8b75-112">Returns the size, in bytes, of [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) or zero if an error occurs..</span></span>

## <a name="remarks"></a><span data-ttu-id="b8b75-113">備註</span><span class="sxs-lookup"><span data-stu-id="b8b75-113">Remarks</span></span>

<span data-ttu-id="b8b75-114">一般而言，應用程式會傳送此訊息，以顯示已安裝的壓縮機清單。</span><span class="sxs-lookup"><span data-stu-id="b8b75-114">Typically, applications send this message to display a list of the installed compressors.</span></span>

<span data-ttu-id="b8b75-115">驅動程式應填滿 **szDriver** 以外的 [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo)結構的所有成員。</span><span class="sxs-lookup"><span data-stu-id="b8b75-115">The driver should fill all members of the [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) structure except **szDriver**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8b75-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8b75-116">Requirements</span></span>



| <span data-ttu-id="b8b75-117">需求</span><span class="sxs-lookup"><span data-stu-id="b8b75-117">Requirement</span></span> | <span data-ttu-id="b8b75-118">值</span><span class="sxs-lookup"><span data-stu-id="b8b75-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b8b75-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b8b75-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b8b75-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8b75-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b8b75-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b8b75-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b8b75-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8b75-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b8b75-123">標頭</span><span class="sxs-lookup"><span data-stu-id="b8b75-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8b75-124"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="b8b75-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8b75-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8b75-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8b75-126">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="b8b75-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="b8b75-127">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="b8b75-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





