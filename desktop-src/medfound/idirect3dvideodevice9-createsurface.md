---
description: 建立適用于 DirectX Video 加速 (DXVA) 解碼的壓縮表面。
ms.assetid: 2bb8c99d-1151-4f6d-869f-2c1a592e76af
title: 'IDirect3DVideoDevice9：： CreateSurface 方法 (Dxva .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.CreateSurface
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: d9e87c9767619241fd6228bb6b0a531249dd2d7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115212"
---
# <a name="idirect3dvideodevice9createsurface-method"></a><span data-ttu-id="1204d-103">IDirect3DVideoDevice9：： CreateSurface 方法</span><span class="sxs-lookup"><span data-stu-id="1204d-103">IDirect3DVideoDevice9::CreateSurface method</span></span>

<span data-ttu-id="1204d-104">建立適用于 DirectX Video 加速 (DXVA) 解碼的壓縮表面。</span><span class="sxs-lookup"><span data-stu-id="1204d-104">Creates a compressed surface for DirectX Video Acceleration (DXVA) decoding.</span></span>

<span data-ttu-id="1204d-105">若要取得介面需求，請呼叫 [**IDirect3DVideoDevice9：： GetDXVACompressedBufferInfo**](idirect3dvideodevice9-getdxvacompressedbufferinfo.md) ，並檢查傳回的 [**DXVACompBufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) 結構。</span><span class="sxs-lookup"><span data-stu-id="1204d-105">To get the surface requirements, call [**IDirect3DVideoDevice9::GetDXVACompressedBufferInfo**](idirect3dvideodevice9-getdxvacompressedbufferinfo.md) and examine the returned [**DXVACompBufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="1204d-106">語法</span><span class="sxs-lookup"><span data-stu-id="1204d-106">Syntax</span></span>


```C++
HRESULT CreateSurface(
   UINT              Width,
   UINT              Height,
   UINT              BackBuffers,
   D3DFORMAT         Format,
   D3DPOOL           Pool,
   DWORD             Usage,
   IDirect3DSurface9 **ppSurface,
   HANDLE            *pSharedHandle
);
```



## <a name="parameters"></a><span data-ttu-id="1204d-107">參數</span><span class="sxs-lookup"><span data-stu-id="1204d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1204d-108">*寬度*</span><span class="sxs-lookup"><span data-stu-id="1204d-108">*Width*</span></span> 
</dt> <dd>

<span data-ttu-id="1204d-109">介面的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="1204d-109">The width of the surface, in pixels.</span></span> <span data-ttu-id="1204d-110">將此參數設定為等於 **DXVACompBufferInfo. WidthToCreate**。</span><span class="sxs-lookup"><span data-stu-id="1204d-110">Set this parameter equal to **DXVACompBufferInfo.WidthToCreate**.</span></span>

</dd> <dt>

<span data-ttu-id="1204d-111">*高度*</span><span class="sxs-lookup"><span data-stu-id="1204d-111">*Height*</span></span> 
</dt> <dd>

<span data-ttu-id="1204d-112">介面的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="1204d-112">The height of the surface, in pixels.</span></span> <span data-ttu-id="1204d-113">將此參數設定為等於 **DXVACompBufferInfo. HeightToCreate**。</span><span class="sxs-lookup"><span data-stu-id="1204d-113">Set this parameter equal to **DXVACompBufferInfo.HeightToCreate**.</span></span>

</dd> <dt>

<span data-ttu-id="1204d-114">*BackBuffers*</span><span class="sxs-lookup"><span data-stu-id="1204d-114">*BackBuffers*</span></span> 
</dt> <dd>

<span data-ttu-id="1204d-115">背景緩衝區的數目。</span><span class="sxs-lookup"><span data-stu-id="1204d-115">The number of back buffers.</span></span> <span data-ttu-id="1204d-116">這個參數可以是零。</span><span class="sxs-lookup"><span data-stu-id="1204d-116">This parameter can be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1204d-117">*格式*</span><span class="sxs-lookup"><span data-stu-id="1204d-117">*Format*</span></span> 
</dt> <dd>

<span data-ttu-id="1204d-118">像素格式，指定為 **D3DFORMAT** 值。</span><span class="sxs-lookup"><span data-stu-id="1204d-118">The pixel format, specified as a **D3DFORMAT** value.</span></span> <span data-ttu-id="1204d-119">請將此參數設定為 **DXVACompBufferInfo 格式**。</span><span class="sxs-lookup"><span data-stu-id="1204d-119">Set this parameter equal to **DXVACompBufferInfo.Format**.</span></span>

</dd> <dt>

<span data-ttu-id="1204d-120">*集區*</span><span class="sxs-lookup"><span data-stu-id="1204d-120">*Pool*</span></span> 
</dt> <dd>

<span data-ttu-id="1204d-121">要在其中建立介面的記憶體集區，指定為 **D3DPOOL** 值。</span><span class="sxs-lookup"><span data-stu-id="1204d-121">The memory pool in which to create the surface, specified as a **D3DPOOL** value.</span></span> <span data-ttu-id="1204d-122">將此參數設定為等於 **DXVACompBufferInfo**。</span><span class="sxs-lookup"><span data-stu-id="1204d-122">Set this parameter equal to **DXVACompBufferInfo.Pool**.</span></span>

</dd> <dt>

<span data-ttu-id="1204d-123">*使用量*</span><span class="sxs-lookup"><span data-stu-id="1204d-123">*Usage*</span></span> 
</dt> <dd>

<span data-ttu-id="1204d-124">一或多個 **D3DUSAGE** 常數的位 **or** 。</span><span class="sxs-lookup"><span data-stu-id="1204d-124">A bitwise **OR** of one or more **D3DUSAGE** constants.</span></span> <span data-ttu-id="1204d-125">將此參數設定為等於 **DXVACompBufferInfo。**</span><span class="sxs-lookup"><span data-stu-id="1204d-125">Set this parameter equal to **DXVACompBufferInfo.Usage**.</span></span>

</dd> <dt>

<span data-ttu-id="1204d-126">*ppSurface*</span><span class="sxs-lookup"><span data-stu-id="1204d-126">*ppSurface*</span></span> 
</dt> <dd>

<span data-ttu-id="1204d-127">接收 **IDirect3DSurface9** 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="1204d-127">Receives a pointer to the **IDirect3DSurface9** interface.</span></span> <span data-ttu-id="1204d-128">呼叫端必須釋放介面。</span><span class="sxs-lookup"><span data-stu-id="1204d-128">The caller must release the interface.</span></span>

</dd> <dt>

<span data-ttu-id="1204d-129">*pSharedHandle*</span><span class="sxs-lookup"><span data-stu-id="1204d-129">*pSharedHandle*</span></span> 
</dt> <dd>

<span data-ttu-id="1204d-130">保留的。</span><span class="sxs-lookup"><span data-stu-id="1204d-130">Reserved.</span></span> <span data-ttu-id="1204d-131">設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="1204d-131">Set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1204d-132">傳回值</span><span class="sxs-lookup"><span data-stu-id="1204d-132">Return value</span></span>

<span data-ttu-id="1204d-133">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="1204d-133">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1204d-134">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1204d-134">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1204d-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="1204d-135">Requirements</span></span>



| <span data-ttu-id="1204d-136">需求</span><span class="sxs-lookup"><span data-stu-id="1204d-136">Requirement</span></span> | <span data-ttu-id="1204d-137">值</span><span class="sxs-lookup"><span data-stu-id="1204d-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="1204d-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1204d-138">Minimum supported client</span></span><br/> | <span data-ttu-id="1204d-139">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1204d-139">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1204d-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1204d-140">Minimum supported server</span></span><br/> | <span data-ttu-id="1204d-141">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1204d-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1204d-142">標頭</span><span class="sxs-lookup"><span data-stu-id="1204d-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="1204d-143"><dt>Dxva。h</dt></span><span class="sxs-lookup"><span data-stu-id="1204d-143"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1204d-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1204d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1204d-145">**IDirect3DVideoDevice9**</span><span class="sxs-lookup"><span data-stu-id="1204d-145">**IDirect3DVideoDevice9**</span></span>](idirect3dvideodevice9.md)
</dt> </dl>

 

 




