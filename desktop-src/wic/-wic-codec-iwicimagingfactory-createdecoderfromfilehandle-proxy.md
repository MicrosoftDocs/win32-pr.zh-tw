---
description: CreateDecoderFromFileHandle 方法的 Proxy 函式。
ms.assetid: bc7f8a07-6d82-4d95-88ef-979d571758f4
title: IWICImagingFactory_CreateDecoderFromFileHandle_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateDecoderFromFileHandle_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 15c515bb17641e2e7b70b79552fe3bacf1f1c3fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944440"
---
# <a name="iwicimagingfactory_createdecoderfromfilehandle_proxy-function"></a><span data-ttu-id="5a597-103">IWICImagingFactory \_ CreateDecoderFromFileHandle \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="5a597-103">IWICImagingFactory\_CreateDecoderFromFileHandle\_Proxy function</span></span>

<span data-ttu-id="5a597-104">[**CreateDecoderFromFileHandle**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilehandle)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="5a597-104">Proxy function for the [**CreateDecoderFromFileHandle**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilehandle) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a597-105">語法</span><span class="sxs-lookup"><span data-stu-id="5a597-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateDecoderFromFileHandle_Proxy(
  _In_        IWICImagingFactory *pFactory,
  _In_        ULONG_PTR          hFile,
  _In_  const GUID               *pguidVendor,
  _In_        WICDecodeOptions   metadataOptions,
  _Out_       IWICBitmapDecoder  **ppIDecoder
);
```



## <a name="parameters"></a><span data-ttu-id="5a597-106">參數</span><span class="sxs-lookup"><span data-stu-id="5a597-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a597-107">*pFactory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5a597-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a597-108">類型： \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="5a597-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="5a597-109">_hFile \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5a597-109">_hFile\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a597-110">類型： **ULONG \_ PTR**</span><span class="sxs-lookup"><span data-stu-id="5a597-110">Type: **ULONG\_PTR**</span></span>

<span data-ttu-id="5a597-111">用來建立解碼器的檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="5a597-111">The file handle to create the decoder from.</span></span>

</dd> <dt>

<span data-ttu-id="5a597-112">*pguidVendor* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5a597-112">*pguidVendor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a597-113">類型： \**CONST GUID \** _</span><span class="sxs-lookup"><span data-stu-id="5a597-113">Type: \**const GUID\** _</span></span>

<span data-ttu-id="5a597-114">適用于此解碼器的廠商 GUID。</span><span class="sxs-lookup"><span data-stu-id="5a597-114">The vendor GUID for the decoder.</span></span>

</dd> <dt>

<span data-ttu-id="5a597-115">_metadataOptions \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5a597-115">_metadataOptions\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a597-116">類型： **[ **WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**</span><span class="sxs-lookup"><span data-stu-id="5a597-116">Type: **[**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**</span></span>

<span data-ttu-id="5a597-117">建立解碼器時要使用的 [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) 。</span><span class="sxs-lookup"><span data-stu-id="5a597-117">The [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) to use when creating the decoder.</span></span>

</dd> <dt>

<span data-ttu-id="5a597-118">*ppIDecoder* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5a597-118">*ppIDecoder* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a597-119">類型： **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***</span><span class="sxs-lookup"><span data-stu-id="5a597-119">Type: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***</span></span>

<span data-ttu-id="5a597-120">接收新 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)指標的指標。</span><span class="sxs-lookup"><span data-stu-id="5a597-120">A pointer that receives a pointer to a new [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a597-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="5a597-121">Return value</span></span>

<span data-ttu-id="5a597-122">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5a597-122">Type: **HRESULT**</span></span>

<span data-ttu-id="5a597-123">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="5a597-123">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5a597-124">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5a597-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a597-125">備註</span><span class="sxs-lookup"><span data-stu-id="5a597-125">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="5a597-126">需求</span><span class="sxs-lookup"><span data-stu-id="5a597-126">Requirements</span></span>



| <span data-ttu-id="5a597-127">需求</span><span class="sxs-lookup"><span data-stu-id="5a597-127">Requirement</span></span> | <span data-ttu-id="5a597-128">值</span><span class="sxs-lookup"><span data-stu-id="5a597-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a597-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5a597-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5a597-130">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5a597-130">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="5a597-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5a597-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5a597-132">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5a597-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="5a597-133">DLL</span><span class="sxs-lookup"><span data-stu-id="5a597-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a597-134"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a597-134"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




