---
description: 執行 DirectX Video 加速 (DXVA) 解碼作業。
ms.assetid: cb87a087-ca53-470e-ab46-f4022cfd7869
title: 'IDirect3DDXVADevice9：： Execute 方法 (Dxva .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.Execute
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: d624146c32b5f7eaeb4e680cf03878e8d065ee5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974410"
---
# <a name="idirect3ddxvadevice9execute-method"></a><span data-ttu-id="d1900-103">IDirect3DDXVADevice9：： Execute 方法</span><span class="sxs-lookup"><span data-stu-id="d1900-103">IDirect3DDXVADevice9::Execute method</span></span>

<span data-ttu-id="d1900-104">執行 DirectX Video 加速 (DXVA) 解碼作業。</span><span class="sxs-lookup"><span data-stu-id="d1900-104">Performs a DirectX Video Acceleration (DXVA) decoding operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1900-105">語法</span><span class="sxs-lookup"><span data-stu-id="d1900-105">Syntax</span></span>


```C++
HRESULT Execute(
   DWORD          FunctionNum,
   VOID           *pInputData,
   DWORD          InputSize,
   VOID           *OutputData,
   DWORD          OutputSize,
   DWORD          NumBuffers,
   DXVABufferInfo *pBufferInfo
);
```



## <a name="parameters"></a><span data-ttu-id="d1900-106">參數</span><span class="sxs-lookup"><span data-stu-id="d1900-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1900-107">*FunctionNum*</span><span class="sxs-lookup"><span data-stu-id="d1900-107">*FunctionNum*</span></span> 
</dt> <dd>

<span data-ttu-id="d1900-108">包含一或多個 DXVA 函式編號的 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="d1900-108">A **DWORD** that contains one or more DXVA function numbers.</span></span> <span data-ttu-id="d1900-109">如需詳細資訊，請參閱 [DXVA 1.0 規格](/windows-hardware/drivers/display/directx-video-acceleration)。</span><span class="sxs-lookup"><span data-stu-id="d1900-109">For details, refer to the [DXVA 1.0 specification](/windows-hardware/drivers/display/directx-video-acceleration).</span></span>

</dd> <dt>

<span data-ttu-id="d1900-110">*pInputData*</span><span class="sxs-lookup"><span data-stu-id="d1900-110">*pInputData*</span></span> 
</dt> <dd>

<span data-ttu-id="d1900-111">緩衝區的指標，此緩衝區包含解碼作業的輸入資料。</span><span class="sxs-lookup"><span data-stu-id="d1900-111">A pointer to a buffer that contains input data for the decoding operation.</span></span> <span data-ttu-id="d1900-112">這項資料的意義取決於介面型別和函式編號。</span><span class="sxs-lookup"><span data-stu-id="d1900-112">The meaning of this data depends on the surface type and function number.</span></span>

</dd> <dt>

<span data-ttu-id="d1900-113">*InputSize*</span><span class="sxs-lookup"><span data-stu-id="d1900-113">*InputSize*</span></span> 
</dt> <dd>

<span data-ttu-id="d1900-114">輸入資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="d1900-114">The size of the input data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="d1900-115">*OutputData*</span><span class="sxs-lookup"><span data-stu-id="d1900-115">*OutputData*</span></span> 
</dt> <dd>

<span data-ttu-id="d1900-116">影片加速器寫入輸出資料之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="d1900-116">Pointer to a buffer where the video accelerator writes output data.</span></span>

</dd> <dt>

<span data-ttu-id="d1900-117">*OutputSize*</span><span class="sxs-lookup"><span data-stu-id="d1900-117">*OutputSize*</span></span> 
</dt> <dd>

<span data-ttu-id="d1900-118">*OutputData* 緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="d1900-118">The size of the *OutputData* buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="d1900-119">*NumBuffers*</span><span class="sxs-lookup"><span data-stu-id="d1900-119">*NumBuffers*</span></span> 
</dt> <dd>

<span data-ttu-id="d1900-120">*PBufferInfo* 陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="d1900-120">The number of elements in the *pBufferInfo* array.</span></span>

</dd> <dt>

<span data-ttu-id="d1900-121">*pBufferInfo*</span><span class="sxs-lookup"><span data-stu-id="d1900-121">*pBufferInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="d1900-122">[**DXVABufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvabufferinfo)結構陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="d1900-122">A pointer to an array of [**DXVABufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvabufferinfo) structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1900-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="d1900-123">Return value</span></span>

<span data-ttu-id="d1900-124">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="d1900-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d1900-125">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d1900-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1900-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="d1900-126">Requirements</span></span>



| <span data-ttu-id="d1900-127">需求</span><span class="sxs-lookup"><span data-stu-id="d1900-127">Requirement</span></span> | <span data-ttu-id="d1900-128">值</span><span class="sxs-lookup"><span data-stu-id="d1900-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d1900-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d1900-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d1900-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d1900-130">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d1900-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d1900-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d1900-132">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d1900-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d1900-133">標頭</span><span class="sxs-lookup"><span data-stu-id="d1900-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1900-134"><dt>Dxva。h</dt></span><span class="sxs-lookup"><span data-stu-id="d1900-134"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1900-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d1900-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1900-136">**IDirect3DDXVADevice9**</span><span class="sxs-lookup"><span data-stu-id="d1900-136">**IDirect3DDXVADevice9**</span></span>](idirect3ddxvadevice9.md)
</dt> </dl>

 

 
