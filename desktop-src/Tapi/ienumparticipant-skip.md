---
description: Skip 方法會略過列舉順序中的下一個指定元素數目。 這種方法在 Visual Basic 和指令碼語言中是隱藏的。
ms.assetid: 7f641354-c3f5-4eb3-ad1c-98abf7694106
title: 'IEnumParticipant：： Skip 方法 (Confpriv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dc406a69c126c25b1c554679595868a595b839b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995009"
---
# <a name="ienumparticipantskip-method"></a><span data-ttu-id="0f1f1-104">IEnumParticipant：： Skip 方法</span><span class="sxs-lookup"><span data-stu-id="0f1f1-104">IEnumParticipant::Skip method</span></span>

<span data-ttu-id="0f1f1-105">\[**Skip** 無法在 windows Vista、windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="0f1f1-105">\[**Skip** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0f1f1-106">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="0f1f1-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="0f1f1-107">**Skip** 方法會略過列舉順序中的下一個指定元素數目。</span><span class="sxs-lookup"><span data-stu-id="0f1f1-107">The **Skip** method skips over the next specified number of elements in the enumeration sequence.</span></span> <span data-ttu-id="0f1f1-108">這種方法在 Visual Basic 和指令碼語言中是隱藏的。</span><span class="sxs-lookup"><span data-stu-id="0f1f1-108">This method is hidden from Visual Basic and scripting languages.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f1f1-109">語法</span><span class="sxs-lookup"><span data-stu-id="0f1f1-109">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a><span data-ttu-id="0f1f1-110">參數</span><span class="sxs-lookup"><span data-stu-id="0f1f1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f1f1-111">*celt* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0f1f1-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f1f1-112">要略過的元素數目。</span><span class="sxs-lookup"><span data-stu-id="0f1f1-112">Number of elements to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f1f1-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="0f1f1-113">Return value</span></span>

<span data-ttu-id="0f1f1-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="0f1f1-114">This method can return one of these values.</span></span>



| <span data-ttu-id="0f1f1-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="0f1f1-115">Return code</span></span>                                                                                   | <span data-ttu-id="0f1f1-116">Description</span><span class="sxs-lookup"><span data-stu-id="0f1f1-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="0f1f1-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="0f1f1-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0f1f1-118">略過的元素數目 *celt*。</span><span class="sxs-lookup"><span data-stu-id="0f1f1-118">Number of elements skipped was *celt*.</span></span><br/>               |
| <dl> <span data-ttu-id="0f1f1-119"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="0f1f1-119"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="0f1f1-120">未 *celt* 略過的元素數目。</span><span class="sxs-lookup"><span data-stu-id="0f1f1-120">Number of elements skipped was not *celt*.</span></span><br/>           |
| <dl> <span data-ttu-id="0f1f1-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0f1f1-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0f1f1-122">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="0f1f1-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0f1f1-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="0f1f1-123">Requirements</span></span>



| <span data-ttu-id="0f1f1-124">需求</span><span class="sxs-lookup"><span data-stu-id="0f1f1-124">Requirement</span></span> | <span data-ttu-id="0f1f1-125">值</span><span class="sxs-lookup"><span data-stu-id="0f1f1-125">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0f1f1-126">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="0f1f1-126">TAPI version</span></span><br/> | <span data-ttu-id="0f1f1-127">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="0f1f1-127">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="0f1f1-128">標頭</span><span class="sxs-lookup"><span data-stu-id="0f1f1-128">Header</span></span><br/>       | <dl> <span data-ttu-id="0f1f1-129"><dt>Confpriv。h</dt></span><span class="sxs-lookup"><span data-stu-id="0f1f1-129"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="0f1f1-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="0f1f1-130">Library</span></span><br/>      | <dl> <span data-ttu-id="0f1f1-131"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="0f1f1-131"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="0f1f1-132">DLL</span><span class="sxs-lookup"><span data-stu-id="0f1f1-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="0f1f1-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f1f1-133"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="0f1f1-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0f1f1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f1f1-135">**IEnumParticipant**</span><span class="sxs-lookup"><span data-stu-id="0f1f1-135">**IEnumParticipant**</span></span>](ienumparticipant.md)
</dt> <dt>

[<span data-ttu-id="0f1f1-136">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="0f1f1-136">**ITParticipant**</span></span>](itparticipant.md)
</dt> </dl>

 

 




