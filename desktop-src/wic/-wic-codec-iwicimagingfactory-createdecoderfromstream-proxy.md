---
description: CreateDecoderFromStream 方法的 Proxy 函式。
ms.assetid: 8395d647-c8c9-4715-b15d-a30755ae0a98
title: IWICImagingFactory_CreateDecoderFromStream_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateDecoderFromStream_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 1f6f84c9c29d10243f1b3bcb2cad43967547eeae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695435"
---
# <a name="iwicimagingfactory_createdecoderfromstream_proxy-function"></a><span data-ttu-id="9471d-103">IWICImagingFactory \_ CreateDecoderFromStream \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="9471d-103">IWICImagingFactory\_CreateDecoderFromStream\_Proxy function</span></span>

<span data-ttu-id="9471d-104">[**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="9471d-104">Proxy function for the [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9471d-105">語法</span><span class="sxs-lookup"><span data-stu-id="9471d-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateDecoderFromStream_Proxy(
  _In_        IWICImagingFactory *pFactory,
  _In_        IStream            *pIStream,
  _In_  const GUID               *pguidVendor,
  _In_        WICDecodeOptions   metadataOptions,
  _Out_       IWICBitmapDecoder  **ppIDecoder
);
```



## <a name="parameters"></a><span data-ttu-id="9471d-106">參數</span><span class="sxs-lookup"><span data-stu-id="9471d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9471d-107">*pFactory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9471d-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9471d-108">類型： \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="9471d-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="9471d-109">_pIStream \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9471d-109">_pIStream\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9471d-110">類型： \**[IStream](/windows/desktop/api/objidl/nn-objidl-istream) \** _</span><span class="sxs-lookup"><span data-stu-id="9471d-110">Type: \**[IStream](/windows/desktop/api/objidl/nn-objidl-istream)\** _</span></span>

<span data-ttu-id="9471d-111">要從中建立解碼器的資料流程。</span><span class="sxs-lookup"><span data-stu-id="9471d-111">The stream to create the decoder from.</span></span>

</dd> <dt>

<span data-ttu-id="9471d-112">_pguidVendor \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9471d-112">_pguidVendor\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9471d-113">類型： \**CONST GUID \** _</span><span class="sxs-lookup"><span data-stu-id="9471d-113">Type: \**const GUID\** _</span></span>

<span data-ttu-id="9471d-114">適用于此解碼器的廠商 GUID。</span><span class="sxs-lookup"><span data-stu-id="9471d-114">The vendor GUID for the decoder .</span></span>

</dd> <dt>

<span data-ttu-id="9471d-115">_metadataOptions \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9471d-115">_metadataOptions\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9471d-116">類型： **[ **WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**</span><span class="sxs-lookup"><span data-stu-id="9471d-116">Type: **[**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**</span></span>

<span data-ttu-id="9471d-117">建立解碼器時要使用的 [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) 。</span><span class="sxs-lookup"><span data-stu-id="9471d-117">The [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) to use when creating the decoder.</span></span>

</dd> <dt>

<span data-ttu-id="9471d-118">*ppIDecoder* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9471d-118">*ppIDecoder* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9471d-119">類型： **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***</span><span class="sxs-lookup"><span data-stu-id="9471d-119">Type: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***</span></span>

<span data-ttu-id="9471d-120">接收新 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)指標的指標。</span><span class="sxs-lookup"><span data-stu-id="9471d-120">A pointer that receives a pointer to a new [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9471d-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="9471d-121">Return value</span></span>

<span data-ttu-id="9471d-122">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9471d-122">Type: **HRESULT**</span></span>

<span data-ttu-id="9471d-123">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="9471d-123">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9471d-124">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9471d-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9471d-125">備註</span><span class="sxs-lookup"><span data-stu-id="9471d-125">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="9471d-126">需求</span><span class="sxs-lookup"><span data-stu-id="9471d-126">Requirements</span></span>



| <span data-ttu-id="9471d-127">需求</span><span class="sxs-lookup"><span data-stu-id="9471d-127">Requirement</span></span> | <span data-ttu-id="9471d-128">值</span><span class="sxs-lookup"><span data-stu-id="9471d-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9471d-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9471d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9471d-130">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9471d-130">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="9471d-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9471d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9471d-132">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9471d-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="9471d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="9471d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9471d-134"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9471d-134"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

