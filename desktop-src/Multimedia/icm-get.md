---
title: 'ICM_GET 訊息 (Vfw .h) '
description: ICM \_ GET 訊息會從視訊壓縮驅動程式抓取應用程式定義的 DWORD 值。
ms.assetid: 288c0053-16a1-4547-b748-da218a0b588c
keywords:
- ICM_GET message Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_GET
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e23cd994546be41b5f938331b2dc632897635c32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685656"
---
# <a name="icm_get-message"></a><span data-ttu-id="735d9-104">ICM \_ GET 訊息</span><span class="sxs-lookup"><span data-stu-id="735d9-104">ICM\_GET message</span></span>

<span data-ttu-id="735d9-105">**ICM \_ GET** 訊息會從視訊壓縮驅動程式抓取應用程式定義的 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="735d9-105">The **ICM\_GET** message retrieves an application-defined **DWORD** value from a video compression driver.</span></span>


```C++
ICM_GET 
wParam = (DWORD) (LPVOID) pv; 
lParam = (DWORD) cb; 
```



## <a name="parameters"></a><span data-ttu-id="735d9-106">參數</span><span class="sxs-lookup"><span data-stu-id="735d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="735d9-107"><span id="pv"></span><span id="PV"></span>*光伏*</span><span class="sxs-lookup"><span data-stu-id="735d9-107"><span id="pv"></span><span id="PV"></span>*pv*</span></span>
</dt> <dd>

<span data-ttu-id="735d9-108">要以目前狀態填滿之記憶體區塊的指標。</span><span class="sxs-lookup"><span data-stu-id="735d9-108">Pointer to a block of memory to be filled with the current state.</span></span> <span data-ttu-id="735d9-109">您也可以指定 **Null** 來判斷狀態資訊所需的記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="735d9-109">You can also specify **NULL** to determine the amount of memory required by the state information.</span></span>

</dd> <dt>

<span data-ttu-id="735d9-110"><span id="cb"></span><span id="CB"></span>*Cb*</span><span class="sxs-lookup"><span data-stu-id="735d9-110"><span id="cb"></span><span id="CB"></span>*cb*</span></span>
</dt> <dd>

<span data-ttu-id="735d9-111">記憶體區塊的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="735d9-111">Size, in bytes, of the block of memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="735d9-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="735d9-112">Return Value</span></span>

<span data-ttu-id="735d9-113">傳回儲存狀態資訊所需的記憶體數量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="735d9-113">Returns the amount of memory, in bytes, required to store the status information.</span></span>

## <a name="remarks"></a><span data-ttu-id="735d9-114">備註</span><span class="sxs-lookup"><span data-stu-id="735d9-114">Remarks</span></span>

<span data-ttu-id="735d9-115">用來代表狀態資訊的結構是驅動程式特定的，而且是由驅動程式所定義。</span><span class="sxs-lookup"><span data-stu-id="735d9-115">The structure used to represent state information is driver specific and is defined by the driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="735d9-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="735d9-116">Requirements</span></span>



| <span data-ttu-id="735d9-117">需求</span><span class="sxs-lookup"><span data-stu-id="735d9-117">Requirement</span></span> | <span data-ttu-id="735d9-118">值</span><span class="sxs-lookup"><span data-stu-id="735d9-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="735d9-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="735d9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="735d9-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="735d9-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="735d9-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="735d9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="735d9-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="735d9-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="735d9-123">標頭</span><span class="sxs-lookup"><span data-stu-id="735d9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="735d9-124"><dt>Vfw。h</dt></span><span class="sxs-lookup"><span data-stu-id="735d9-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="735d9-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="735d9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="735d9-126">影片壓縮管理員</span><span class="sxs-lookup"><span data-stu-id="735d9-126">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="735d9-127">影片壓縮訊息</span><span class="sxs-lookup"><span data-stu-id="735d9-127">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





