---
description: 開始處理以建立解碼的圖片。
ms.assetid: 80471cc6-c66d-49d9-8593-780e41ac39b9
title: 'IDirect3DDXVADevice9：： BeginFrame 方法 (Dxva .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.BeginFrame
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 3090d7868316d08fa91f36dffcc938eb31e06a7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974235"
---
# <a name="idirect3ddxvadevice9beginframe-method"></a><span data-ttu-id="72ce4-103">IDirect3DDXVADevice9：： BeginFrame 方法</span><span class="sxs-lookup"><span data-stu-id="72ce4-103">IDirect3DDXVADevice9::BeginFrame method</span></span>

<span data-ttu-id="72ce4-104">開始處理以建立解碼的圖片。</span><span class="sxs-lookup"><span data-stu-id="72ce4-104">Begins the processing to create a decoded picture.</span></span>

## <a name="syntax"></a><span data-ttu-id="72ce4-105">語法</span><span class="sxs-lookup"><span data-stu-id="72ce4-105">Syntax</span></span>


```C++
HRESULT BeginFrame(
   IDirect3DSurface9 *pDstSurface,
   DWORD             SizeInputData,
   VOID              *pInputData,
   DWORD             *pSizeOutputData,
   VOID              *pOutputData
);
```



## <a name="parameters"></a><span data-ttu-id="72ce4-106">參數</span><span class="sxs-lookup"><span data-stu-id="72ce4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72ce4-107">*pDstSurface*</span><span class="sxs-lookup"><span data-stu-id="72ce4-107">*pDstSurface*</span></span> 
</dt> <dd>

<span data-ttu-id="72ce4-108">未壓縮目的介面之 **IDirect3DSurface9** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="72ce4-108">A pointer to the **IDirect3DSurface9** interface of the uncompressed destination surface.</span></span>

</dd> <dt>

<span data-ttu-id="72ce4-109">*SizeInputData*</span><span class="sxs-lookup"><span data-stu-id="72ce4-109">*SizeInputData*</span></span> 
</dt> <dd>

<span data-ttu-id="72ce4-110">*PInputData* 所指定的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="72ce4-110">The size of the buffer specified by *pInputData*, in bytes.</span></span> <span data-ttu-id="72ce4-111">值必須是2。</span><span class="sxs-lookup"><span data-stu-id="72ce4-111">The value must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="72ce4-112">*pInputData*</span><span class="sxs-lookup"><span data-stu-id="72ce4-112">*pInputData*</span></span> 
</dt> <dd>

<span data-ttu-id="72ce4-113">包含影片加速器資料之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="72ce4-113">Pointer to a buffer that contains data for the video accelerator.</span></span> <span data-ttu-id="72ce4-114">這個緩衝區必須包含以零為基底的框架索引，並指定為 **文字** 值。</span><span class="sxs-lookup"><span data-stu-id="72ce4-114">This buffer must contain the zero-based frame index, specified as a **WORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="72ce4-115">*pSizeOutputData*</span><span class="sxs-lookup"><span data-stu-id="72ce4-115">*pSizeOutputData*</span></span> 
</dt> <dd>

<span data-ttu-id="72ce4-116">*POutputData* 所指定的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="72ce4-116">The size of the buffer specified by *pOutputData*, in bytes.</span></span> <span data-ttu-id="72ce4-117">此值必須為零。</span><span class="sxs-lookup"><span data-stu-id="72ce4-117">The value must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="72ce4-118">*pOutputData*</span><span class="sxs-lookup"><span data-stu-id="72ce4-118">*pOutputData*</span></span> 
</dt> <dd>

<span data-ttu-id="72ce4-119">影片加速器可以寫入之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="72ce4-119">Pointer to a buffer that the video accelerator can write to.</span></span> <span data-ttu-id="72ce4-120">將此參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="72ce4-120">Set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72ce4-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="72ce4-121">Return value</span></span>

<span data-ttu-id="72ce4-122">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="72ce4-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="72ce4-123">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="72ce4-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="72ce4-124">備註</span><span class="sxs-lookup"><span data-stu-id="72ce4-124">Remarks</span></span>

<span data-ttu-id="72ce4-125">對於 **BeginFrame** 的每個呼叫，解碼器都必須對 [**IDirect3DDXVADevice9：： EndFrame**](idirect3ddxvadevice9-endframe.md)進行對應的呼叫。</span><span class="sxs-lookup"><span data-stu-id="72ce4-125">For each call to **BeginFrame**, the decoder must make a corresponding call to [**IDirect3DDXVADevice9::EndFrame**](idirect3ddxvadevice9-endframe.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="72ce4-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="72ce4-126">Requirements</span></span>



| <span data-ttu-id="72ce4-127">需求</span><span class="sxs-lookup"><span data-stu-id="72ce4-127">Requirement</span></span> | <span data-ttu-id="72ce4-128">值</span><span class="sxs-lookup"><span data-stu-id="72ce4-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="72ce4-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="72ce4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="72ce4-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="72ce4-130">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="72ce4-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="72ce4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="72ce4-132">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="72ce4-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="72ce4-133">標頭</span><span class="sxs-lookup"><span data-stu-id="72ce4-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="72ce4-134"><dt>Dxva。h</dt></span><span class="sxs-lookup"><span data-stu-id="72ce4-134"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72ce4-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="72ce4-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72ce4-136">**IDirect3DDXVADevice9**</span><span class="sxs-lookup"><span data-stu-id="72ce4-136">**IDirect3DDXVADevice9**</span></span>](idirect3ddxvadevice9.md)
</dt> </dl>

 

 




