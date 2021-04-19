---
description: 取得硬體加速解碼所需之壓縮緩衝區的相關資訊。
ms.assetid: 5a9fb077-fd79-4faa-a0f8-b3ac987adf36
title: 'IDirect3DVideoDevice9：： GetDXVACompressedBufferInfo 方法 (Dxva .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVACompressedBufferInfo
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 2bd2dcdd931ac8778e4f1c11f1479fe54e23d1b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977189"
---
# <a name="idirect3dvideodevice9getdxvacompressedbufferinfo-method"></a><span data-ttu-id="e9273-103">IDirect3DVideoDevice9：： GetDXVACompressedBufferInfo 方法</span><span class="sxs-lookup"><span data-stu-id="e9273-103">IDirect3DVideoDevice9::GetDXVACompressedBufferInfo method</span></span>

<span data-ttu-id="e9273-104">取得硬體加速解碼所需之壓縮緩衝區的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e9273-104">Gets information about the compressed buffers needed for hardware-accelerated decoding.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9273-105">語法</span><span class="sxs-lookup"><span data-stu-id="e9273-105">Syntax</span></span>


```C++
HRESULT GetDXVACompressedBufferInfo(
   GUID               *pGuid,
   DXVAUncompDataInfo *pUncompData,
   DWORD              *pNumBuffers,
   DXVACompBufferInfo *pBufferInfo
);
```



## <a name="parameters"></a><span data-ttu-id="e9273-106">參數</span><span class="sxs-lookup"><span data-stu-id="e9273-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9273-107">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="e9273-107">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="e9273-108">指定 DXVA 設定檔之 GUID 的指標。</span><span class="sxs-lookup"><span data-stu-id="e9273-108">Pointer to a GUID that specifies the DXVA profile.</span></span> <span data-ttu-id="e9273-109">若要取得支援的配置檔案清單，請呼叫 [**IDirect3DVideoDevice9：： GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md)。</span><span class="sxs-lookup"><span data-stu-id="e9273-109">To get a list of supported profiles, call [**IDirect3DVideoDevice9::GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).</span></span>

</dd> <dt>

<span data-ttu-id="e9273-110">*pUncompData*</span><span class="sxs-lookup"><span data-stu-id="e9273-110">*pUncompData*</span></span> 
</dt> <dd>

<span data-ttu-id="e9273-111">[**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo)結構的指標，指定未壓縮資料的大小和像素格式。</span><span class="sxs-lookup"><span data-stu-id="e9273-111">Pointer to a [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) structure that specifies the size and pixel format of the uncompressed data.</span></span>

</dd> <dt>

<span data-ttu-id="e9273-112">*pNumBuffers*</span><span class="sxs-lookup"><span data-stu-id="e9273-112">*pNumBuffers*</span></span> 
</dt> <dd>

<span data-ttu-id="e9273-113">在 [輸入] 上，指定 *pBufferInfo* 陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="e9273-113">On input, specifies the number of elements in the *pBufferInfo* array.</span></span> <span data-ttu-id="e9273-114">如果 *pBufferInfo* 為 **Null**，的值 `*pNumBuffers` 必須是零。</span><span class="sxs-lookup"><span data-stu-id="e9273-114">If *pBufferInfo* is **NULL**, the value of `*pNumBuffers` must be zero.</span></span>

<span data-ttu-id="e9273-115">在輸出中，如果 *pBufferInfo* 為 **Null**，則 *pNumBuffers* 會接收要配置的陣列大小。</span><span class="sxs-lookup"><span data-stu-id="e9273-115">On output, if *pBufferInfo* is **NULL**, *pNumBuffers* receives the size of array to allocate.</span></span> <span data-ttu-id="e9273-116">否則， *pNumBuffers* 會接收復制到 *pBufferInfo* 陣列的實際元素數目。</span><span class="sxs-lookup"><span data-stu-id="e9273-116">Otherwise, *pNumBuffers* receives the actual number of elements that are copied to the *pBufferInfo* array.</span></span>

</dd> <dt>

<span data-ttu-id="e9273-117">*pBufferInfo*</span><span class="sxs-lookup"><span data-stu-id="e9273-117">*pBufferInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="e9273-118">[**DXVACompBufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo)結構陣列的位址或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e9273-118">Address of an array of [**DXVACompBufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) structures or **NULL**.</span></span> <span data-ttu-id="e9273-119">如果此值為非 **Null**，則方法會將 **DXVACompBufferInfo** 結構清單複製到這個陣列。</span><span class="sxs-lookup"><span data-stu-id="e9273-119">If the value is non-**NULL**, the method copies a list of **DXVACompBufferInfo** structures to this array.</span></span> <span data-ttu-id="e9273-120">每個結構都對應于影片加速器所使用的一種壓縮資料緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e9273-120">Each structure corresponds to one type of compressed data buffer that is used by the video accelerator.</span></span>

<span data-ttu-id="e9273-121">呼叫這個方法之前，請先將所有陣列元素設定為零。</span><span class="sxs-lookup"><span data-stu-id="e9273-121">Set all of the array elements to zero before calling this method.</span></span>

<span data-ttu-id="e9273-122">每個陣列索引都對應至 DXVA 中定義的其中一個 DXVA 介面類別型。</span><span class="sxs-lookup"><span data-stu-id="e9273-122">Each array index corresponds to one of the DXVA surface types defined in dxva.h.</span></span> <span data-ttu-id="e9273-123">影片加速器會傳回 **DXVA \_ NUM \_ 類型的 \_ 複合 \_ 緩衝區** 陣列專案清單。</span><span class="sxs-lookup"><span data-stu-id="e9273-123">The video accelerator returns a list of up to **DXVA\_NUM\_TYPES\_COMP\_BUFFERS** array entries.</span></span> <span data-ttu-id="e9273-124">如需詳細資訊，請參閱 [DXVA 1.0 規格](/windows-hardware/drivers/display/directx-video-acceleration)，第3.4 節「緩衝區描述清單」。</span><span class="sxs-lookup"><span data-stu-id="e9273-124">For details, refer to the [DXVA 1.0 specification](/windows-hardware/drivers/display/directx-video-acceleration), section 3.4, "Buffer Description List."</span></span> <span data-ttu-id="e9273-125">如果 DXVA 設定檔沒有使用特定的緩衝區類型，則該索引的專案會包含所有值的零。</span><span class="sxs-lookup"><span data-stu-id="e9273-125">If a particular buffer type is not used by the DXVA profile, the entry at that index contains zeros for all values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9273-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="e9273-126">Return value</span></span>

<span data-ttu-id="e9273-127">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="e9273-127">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e9273-128">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e9273-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9273-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9273-129">Requirements</span></span>



| <span data-ttu-id="e9273-130">需求</span><span class="sxs-lookup"><span data-stu-id="e9273-130">Requirement</span></span> | <span data-ttu-id="e9273-131">值</span><span class="sxs-lookup"><span data-stu-id="e9273-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e9273-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e9273-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e9273-133">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e9273-133">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e9273-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e9273-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e9273-135">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e9273-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e9273-136">標頭</span><span class="sxs-lookup"><span data-stu-id="e9273-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9273-137"><dt>Dxva。h</dt></span><span class="sxs-lookup"><span data-stu-id="e9273-137"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9273-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9273-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9273-139">**IDirect3DVideoDevice9**</span><span class="sxs-lookup"><span data-stu-id="e9273-139">**IDirect3DVideoDevice9**</span></span>](idirect3dvideodevice9.md)
</dt> </dl>

 

 
