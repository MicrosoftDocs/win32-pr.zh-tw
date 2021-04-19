---
description: CreateBitmapFromMemory 方法的 Proxy 函式。
ms.assetid: 5aa455d5-23e3-4738-b028-b84da0fb0c50
title: IWICImagingFactory_CreateBitmapFromMemory_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromMemory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 79893952bb6dcdbab6c4a1cea4f57355831d31c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106999929"
---
# <a name="iwicimagingfactory_createbitmapfrommemory_proxy-function"></a><span data-ttu-id="2aacd-103">IWICImagingFactory \_ CreateBitmapFromMemory \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="2aacd-103">IWICImagingFactory\_CreateBitmapFromMemory\_Proxy function</span></span>

<span data-ttu-id="2aacd-104">[**CreateBitmapFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfrommemory)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="2aacd-104">Proxy function for the [**CreateBitmapFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfrommemory) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2aacd-105">語法</span><span class="sxs-lookup"><span data-stu-id="2aacd-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapFromMemory_Proxy(
  _In_  IWICImagingFactory    *pFactory,
  _In_  UINT                  uiWidth,
  _In_  UINT                  uiHeight,
  _In_  REFWICPixelFormatGUID pixelFormat,
  _In_  UINT                  cbStride,
  _In_  UINT                  cbBufferSize,
  _In_  BYTE                  *pbBuffer,
  _Out_ IWICBitmap            **ppIBitmap
);
```



## <a name="parameters"></a><span data-ttu-id="2aacd-106">參數</span><span class="sxs-lookup"><span data-stu-id="2aacd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2aacd-107">*pFactory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2aacd-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2aacd-108">類型： \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="2aacd-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="2aacd-109">_uiWidth \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2aacd-109">_uiWidth\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2aacd-110">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="2aacd-110">Type: **UINT**</span></span>

<span data-ttu-id="2aacd-111">新點陣圖的寬度。</span><span class="sxs-lookup"><span data-stu-id="2aacd-111">The width of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="2aacd-112">*uiHeight* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2aacd-112">*uiHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2aacd-113">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="2aacd-113">Type: **UINT**</span></span>

<span data-ttu-id="2aacd-114">新點陣圖的高度。</span><span class="sxs-lookup"><span data-stu-id="2aacd-114">The height of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="2aacd-115">*pixelFormat* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2aacd-115">*pixelFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2aacd-116">類型： **REFWICPixelFormatGUID**</span><span class="sxs-lookup"><span data-stu-id="2aacd-116">Type: **REFWICPixelFormatGUID**</span></span>

<span data-ttu-id="2aacd-117">新點陣圖的像素格式。</span><span class="sxs-lookup"><span data-stu-id="2aacd-117">The pixel format of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="2aacd-118">*cbStride* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2aacd-118">*cbStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2aacd-119">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="2aacd-119">Type: **UINT**</span></span>

<span data-ttu-id="2aacd-120">指定圖元資料的 [*stride*](/windows) 。</span><span class="sxs-lookup"><span data-stu-id="2aacd-120">The [*stride*](/windows) of the given pixel data.</span></span>

</dd> <dt>

<span data-ttu-id="2aacd-121">*cbBufferSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2aacd-121">*cbBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2aacd-122">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="2aacd-122">Type: **UINT**</span></span>

<span data-ttu-id="2aacd-123">*PbBuffer* 的大小。</span><span class="sxs-lookup"><span data-stu-id="2aacd-123">The size of *pbBuffer*.</span></span>

</dd> <dt>

<span data-ttu-id="2aacd-124">*pbBuffer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2aacd-124">*pbBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2aacd-125">類型： \**BYTE \** _</span><span class="sxs-lookup"><span data-stu-id="2aacd-125">Type: \**BYTE\** _</span></span>

<span data-ttu-id="2aacd-126">用來建立點陣圖的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="2aacd-126">The buffer used to create the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="2aacd-127">_ppIBitmap \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2aacd-127">_ppIBitmap\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2aacd-128">類型： **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span><span class="sxs-lookup"><span data-stu-id="2aacd-128">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span></span>

<span data-ttu-id="2aacd-129">接收新點陣圖指標的指標。</span><span class="sxs-lookup"><span data-stu-id="2aacd-129">A pointer that receives a pointer to the new bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2aacd-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="2aacd-130">Return value</span></span>

<span data-ttu-id="2aacd-131">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2aacd-131">Type: **HRESULT**</span></span>

<span data-ttu-id="2aacd-132">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="2aacd-132">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2aacd-133">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2aacd-133">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2aacd-134">備註</span><span class="sxs-lookup"><span data-stu-id="2aacd-134">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="2aacd-135">需求</span><span class="sxs-lookup"><span data-stu-id="2aacd-135">Requirements</span></span>



| <span data-ttu-id="2aacd-136">需求</span><span class="sxs-lookup"><span data-stu-id="2aacd-136">Requirement</span></span> | <span data-ttu-id="2aacd-137">值</span><span class="sxs-lookup"><span data-stu-id="2aacd-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2aacd-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2aacd-138">Minimum supported client</span></span><br/> | <span data-ttu-id="2aacd-139">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2aacd-139">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="2aacd-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2aacd-140">Minimum supported server</span></span><br/> | <span data-ttu-id="2aacd-141">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2aacd-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="2aacd-142">DLL</span><span class="sxs-lookup"><span data-stu-id="2aacd-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2aacd-143"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2aacd-143"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

