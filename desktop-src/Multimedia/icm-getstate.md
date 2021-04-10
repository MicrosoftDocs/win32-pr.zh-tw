---
title: 'ICM_GETSTATE 訊息 (Vfw .h) '
description: ICM \_ >getstate 訊息會查詢視訊壓縮驅動程式，以在記憶體區塊中傳回其目前的設定，或判斷取出設定資訊所需的記憶體數量。
ms.assetid: 4b77e294-f3aa-45f9-a4f4-f103b83eae8d
keywords:
- ICM_GETSTATE message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_GETSTATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b6a45dcde627a02c1a4a402ea9a2a725f0429a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106548"
---
# <a name="icm_getstate-message"></a><span data-ttu-id="8d8ae-104">ICM \_ >getstate 訊息</span><span class="sxs-lookup"><span data-stu-id="8d8ae-104">ICM\_GETSTATE message</span></span>

<span data-ttu-id="8d8ae-105">**ICM \_ >getstate** 訊息會查詢視訊壓縮驅動程式，以在記憶體區塊中傳回其目前的設定，或判斷取出設定資訊所需的記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="8d8ae-105">The **ICM\_GETSTATE** message queries a video compression driver to return its current configuration in a block of memory or to determine the amount of memory required to retrieve the configuration information.</span></span> <span data-ttu-id="8d8ae-106">您可以使用 [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="8d8ae-106">You can send this message explicitly or by using the [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate) macro.</span></span>


```C++
ICM_GETSTATE 
wParam = (DWORD_PTR) (LPVOID) pv; 
lParam = (DWORD_PTR) cb; 
```



## <a name="parameters"></a><span data-ttu-id="8d8ae-107">參數</span><span class="sxs-lookup"><span data-stu-id="8d8ae-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d8ae-108"><span id="pv"></span><span id="PV"></span>*光伏*</span><span class="sxs-lookup"><span data-stu-id="8d8ae-108"><span id="pv"></span><span id="PV"></span>*pv*</span></span>
</dt> <dd>

<span data-ttu-id="8d8ae-109">包含目前設定資訊之記憶體區塊的指標。</span><span class="sxs-lookup"><span data-stu-id="8d8ae-109">Pointer to a block of memory to contain the current configuration information.</span></span> <span data-ttu-id="8d8ae-110">您可以為此參數指定 **Null** ，以判斷設定資訊所需的記憶體數量，如 [**ICGetStateSize**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize)中所示。</span><span class="sxs-lookup"><span data-stu-id="8d8ae-110">You can specify **NULL** for this parameter to determine the amount of memory required for the configuration information, as in [**ICGetStateSize**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize).</span></span>

</dd> <dt>

<span data-ttu-id="8d8ae-111"><span id="cb"></span><span id="CB"></span>*Cb*</span><span class="sxs-lookup"><span data-stu-id="8d8ae-111"><span id="cb"></span><span id="CB"></span>*cb*</span></span>
</dt> <dd>

<span data-ttu-id="8d8ae-112">記憶體區塊的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="8d8ae-112">Size, in bytes, of the block of memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d8ae-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="8d8ae-113">Return Value</span></span>

<span data-ttu-id="8d8ae-114">如果 *pv* 為 **Null**，則會傳回設定資訊所需的記憶體數量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="8d8ae-114">If *pv* is **NULL**, returns the amount of memory, in bytes, required for configuration information.</span></span>

<span data-ttu-id="8d8ae-115">如果 *pv* 不是 **Null**，則會 \_ 在成功時傳回 ICERR OK，否則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="8d8ae-115">If *pv* is not **NULL**, returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d8ae-116">備註</span><span class="sxs-lookup"><span data-stu-id="8d8ae-116">Remarks</span></span>

<span data-ttu-id="8d8ae-117">用來表示設定資訊的結構是驅動程式特定的，而且是由驅動程式所定義。</span><span class="sxs-lookup"><span data-stu-id="8d8ae-117">The structure used to represent configuration information is driver specific and is defined by the driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d8ae-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="8d8ae-118">Requirements</span></span>



| <span data-ttu-id="8d8ae-119">需求</span><span class="sxs-lookup"><span data-stu-id="8d8ae-119">Requirement</span></span> | <span data-ttu-id="8d8ae-120">值</span><span class="sxs-lookup"><span data-stu-id="8d8ae-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8d8ae-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8d8ae-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8d8ae-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8d8ae-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="8d8ae-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8d8ae-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8d8ae-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8d8ae-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8d8ae-125">標頭</span><span class="sxs-lookup"><span data-stu-id="8d8ae-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d8ae-126"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="8d8ae-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d8ae-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8d8ae-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d8ae-128">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="8d8ae-128">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="8d8ae-129">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="8d8ae-129">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





