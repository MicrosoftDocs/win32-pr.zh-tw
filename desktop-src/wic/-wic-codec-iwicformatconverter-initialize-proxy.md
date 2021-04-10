---
description: Initialize 方法的 Proxy 函式。
ms.assetid: 26112d52-95e2-4c67-83fc-cf5e28712730
title: IWICFormatConverter_Initialize_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICFormatConverter_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 6450c1a508507db73e44ef8b88b4f94970ac6004
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194410"
---
# <a name="iwicformatconverter_initialize_proxy-function"></a><span data-ttu-id="4b899-103">IWICFormatConverter \_ Initialize \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="4b899-103">IWICFormatConverter\_Initialize\_Proxy function</span></span>

<span data-ttu-id="4b899-104">[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="4b899-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b899-105">語法</span><span class="sxs-lookup"><span data-stu-id="4b899-105">Syntax</span></span>


```C++
HRESULT IWICFormatConverter_Initialize_Proxy(
  _In_ IWICFormatConverter   *THIS_PTR,
  _In_ IWICBitmapSource      *pISource,
  _In_ REFWICPixelFormatGUID dstFormat,
  _In_ WICBitmapDitherType   dither,
  _In_ IWICPalette           *pIPalette,
  _In_ double                alphaThresholdPercent,
  _In_ WICBitmapPaletteType  paletteTranslate
);
```



## <a name="parameters"></a><span data-ttu-id="4b899-106">參數</span><span class="sxs-lookup"><span data-stu-id="4b899-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b899-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="4b899-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b899-108">類型： \**[**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) \** _</span><span class="sxs-lookup"><span data-stu-id="4b899-108">Type: \**[**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)\** _</span></span>

<span data-ttu-id="4b899-109">這個 [_ *IWICFormatConverter* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="4b899-109">Pointer to this [_ *IWICFormatConverter*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter) object.</span></span>

</dd> <dt>

<span data-ttu-id="4b899-110">*pISource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4b899-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b899-111">類型： \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="4b899-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="4b899-112">要轉換的輸入點陣圖</span><span class="sxs-lookup"><span data-stu-id="4b899-112">The input bitmap to convert</span></span>

</dd> <dt>

<span data-ttu-id="4b899-113">_dstFormat \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4b899-113">_dstFormat\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b899-114">類型： **REFWICPixelFormatGUID**</span><span class="sxs-lookup"><span data-stu-id="4b899-114">Type: **REFWICPixelFormatGUID**</span></span>

<span data-ttu-id="4b899-115">目的地像素格式 GUID。</span><span class="sxs-lookup"><span data-stu-id="4b899-115">The destination pixel format GUID.</span></span>

</dd> <dt>

<span data-ttu-id="4b899-116">*遞色* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4b899-116">*dither* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b899-117">類型： **[ **WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype)**</span><span class="sxs-lookup"><span data-stu-id="4b899-117">Type: **[**WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype)**</span></span>

<span data-ttu-id="4b899-118">用於轉換的 [**WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype) 。</span><span class="sxs-lookup"><span data-stu-id="4b899-118">The [**WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype) used for conversion.</span></span>

</dd> <dt>

<span data-ttu-id="4b899-119">*pIPalette* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4b899-119">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b899-120">類型： \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="4b899-120">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="4b899-121">用於轉換的調色板。</span><span class="sxs-lookup"><span data-stu-id="4b899-121">The palette to use for conversion.</span></span>

</dd> <dt>

<span data-ttu-id="4b899-122">_AlphaThresholdPercent \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4b899-122">_alphaThresholdPercent\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b899-123">類型： **double**</span><span class="sxs-lookup"><span data-stu-id="4b899-123">Type: **double**</span></span>

<span data-ttu-id="4b899-124">要用於轉換的 Alpha 臨界值。</span><span class="sxs-lookup"><span data-stu-id="4b899-124">The alpha threshold to use for conversion.</span></span>

</dd> <dt>

<span data-ttu-id="4b899-125">*paletteTranslate* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4b899-125">*paletteTranslate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b899-126">類型： **[ **WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**</span><span class="sxs-lookup"><span data-stu-id="4b899-126">Type: **[**WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**</span></span>

<span data-ttu-id="4b899-127">用於轉換的調色板轉譯類型。</span><span class="sxs-lookup"><span data-stu-id="4b899-127">The palette translation type to use for conversion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b899-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="4b899-128">Return value</span></span>

<span data-ttu-id="4b899-129">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4b899-129">Type: **HRESULT**</span></span>

<span data-ttu-id="4b899-130">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="4b899-130">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4b899-131">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4b899-131">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b899-132">備註</span><span class="sxs-lookup"><span data-stu-id="4b899-132">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="4b899-133">需求</span><span class="sxs-lookup"><span data-stu-id="4b899-133">Requirements</span></span>



| <span data-ttu-id="4b899-134">需求</span><span class="sxs-lookup"><span data-stu-id="4b899-134">Requirement</span></span> | <span data-ttu-id="4b899-135">值</span><span class="sxs-lookup"><span data-stu-id="4b899-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b899-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4b899-136">Minimum supported client</span></span><br/> | <span data-ttu-id="4b899-137">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4b899-137">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="4b899-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4b899-138">Minimum supported server</span></span><br/> | <span data-ttu-id="4b899-139">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4b899-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="4b899-140">DLL</span><span class="sxs-lookup"><span data-stu-id="4b899-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b899-141"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4b899-141"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




