---
description: CreateBitmap 方法的 Proxy 函式。
ms.assetid: 5647521b-231d-4819-97ab-4dfb5f796211
title: IWICImagingFactory_CreateBitmap_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmap_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 56684de0280ae27bf2ec1e900bd718faec4733fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983838"
---
# <a name="iwicimagingfactory_createbitmap_proxy-function"></a><span data-ttu-id="cc3f3-103">IWICImagingFactory \_ CreateBitmap \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="cc3f3-103">IWICImagingFactory\_CreateBitmap\_Proxy function</span></span>

<span data-ttu-id="cc3f3-104">[**CreateBitmap**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmap)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="cc3f3-104">Proxy function for the [**CreateBitmap**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmap) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc3f3-105">語法</span><span class="sxs-lookup"><span data-stu-id="cc3f3-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmap_Proxy(
  _In_  IWICImagingFactory         *pFactory,
  _In_  UINT                       uiWidth,
  _In_  UINT                       uiHeight,
  _In_  REFWICPixelFormatGUID      pixelFormat,
  _In_  WICBitmapCreateCacheOption option,
  _Out_ IWICBitmap                 **ppIBitmap
);
```



## <a name="parameters"></a><span data-ttu-id="cc3f3-106">參數</span><span class="sxs-lookup"><span data-stu-id="cc3f3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc3f3-107">*pFactory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cc3f3-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc3f3-108">類型： \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="cc3f3-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="cc3f3-109">_uiWidth \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cc3f3-109">_uiWidth\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc3f3-110">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="cc3f3-110">Type: **UINT**</span></span>

<span data-ttu-id="cc3f3-111">新點陣圖的寬度。</span><span class="sxs-lookup"><span data-stu-id="cc3f3-111">The width of the new bitmap .</span></span>

</dd> <dt>

<span data-ttu-id="cc3f3-112">*uiHeight* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cc3f3-112">*uiHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc3f3-113">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="cc3f3-113">Type: **UINT**</span></span>

<span data-ttu-id="cc3f3-114">新點陣圖的高度。</span><span class="sxs-lookup"><span data-stu-id="cc3f3-114">The height of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="cc3f3-115">*pixelFormat* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cc3f3-115">*pixelFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc3f3-116">類型： **REFWICPixelFormatGUID**</span><span class="sxs-lookup"><span data-stu-id="cc3f3-116">Type: **REFWICPixelFormatGUID**</span></span>

<span data-ttu-id="cc3f3-117">新點陣圖的像素格式。</span><span class="sxs-lookup"><span data-stu-id="cc3f3-117">The pixel format of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="cc3f3-118">*選項* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cc3f3-118">*option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc3f3-119">類型： **[ **WICBitmapCreateCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapcreatecacheoption)**</span><span class="sxs-lookup"><span data-stu-id="cc3f3-119">Type: **[**WICBitmapCreateCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapcreatecacheoption)**</span></span>

<span data-ttu-id="cc3f3-120">新點陣圖的快取建立選項。</span><span class="sxs-lookup"><span data-stu-id="cc3f3-120">The cache creation options of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="cc3f3-121">*ppIBitmap* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="cc3f3-121">*ppIBitmap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc3f3-122">類型： **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span><span class="sxs-lookup"><span data-stu-id="cc3f3-122">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span></span>

<span data-ttu-id="cc3f3-123">接收新點陣圖指標的指標。</span><span class="sxs-lookup"><span data-stu-id="cc3f3-123">A pointer that receives a pointer to the new bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc3f3-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="cc3f3-124">Return value</span></span>

<span data-ttu-id="cc3f3-125">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="cc3f3-125">Type: **HRESULT**</span></span>

<span data-ttu-id="cc3f3-126">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="cc3f3-126">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cc3f3-127">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="cc3f3-127">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc3f3-128">備註</span><span class="sxs-lookup"><span data-stu-id="cc3f3-128">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="cc3f3-129">需求</span><span class="sxs-lookup"><span data-stu-id="cc3f3-129">Requirements</span></span>



| <span data-ttu-id="cc3f3-130">需求</span><span class="sxs-lookup"><span data-stu-id="cc3f3-130">Requirement</span></span> | <span data-ttu-id="cc3f3-131">值</span><span class="sxs-lookup"><span data-stu-id="cc3f3-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc3f3-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cc3f3-132">Minimum supported client</span></span><br/> | <span data-ttu-id="cc3f3-133">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cc3f3-133">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="cc3f3-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cc3f3-134">Minimum supported server</span></span><br/> | <span data-ttu-id="cc3f3-135">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cc3f3-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="cc3f3-136">DLL</span><span class="sxs-lookup"><span data-stu-id="cc3f3-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc3f3-137"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc3f3-137"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




