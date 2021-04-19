---
description: CreateFastMetadataEncoderFromFrameDecode 方法的 Proxy 函式。
ms.assetid: 0edc3387-47e9-401c-9153-76c8c32b52de
title: IWICImagingFactory_CreateFastMetadataEncoderFromFrameDecode_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateFastMetadataEncoderFromFrameDecode_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 101bb6aca30f3511a8eb370afa8eb8fd6dda1c21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996949"
---
# <a name="iwicimagingfactory_createfastmetadataencoderfromframedecode_proxy-function"></a><span data-ttu-id="ae297-103">IWICImagingFactory \_ CreateFastMetadataEncoderFromFrameDecode \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="ae297-103">IWICImagingFactory\_CreateFastMetadataEncoderFromFrameDecode\_Proxy function</span></span>

<span data-ttu-id="ae297-104">[**CreateFastMetadataEncoderFromFrameDecode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createfastmetadataencoderfromframedecode)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="ae297-104">Proxy function for the [**CreateFastMetadataEncoderFromFrameDecode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createfastmetadataencoderfromframedecode) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae297-105">語法</span><span class="sxs-lookup"><span data-stu-id="ae297-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateFastMetadataEncoderFromFrameDecode_Proxy(
  _In_  IWICImagingFactory      *pFactory,
  _In_  IWICBitmapFrameDecode   *pIFrameDecoder,
  _Out_ IWICFastMetadataEncoder **ppIFME
);
```



## <a name="parameters"></a><span data-ttu-id="ae297-106">參數</span><span class="sxs-lookup"><span data-stu-id="ae297-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae297-107">*pFactory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ae297-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae297-108">類型： \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="ae297-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="ae297-109">_pIFrameDecoder \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae297-109">_pIFrameDecoder\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae297-110">類型： \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) \** _</span><span class="sxs-lookup"><span data-stu-id="ae297-110">Type: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\** _</span></span>

<span data-ttu-id="ae297-111">用來建立 [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)的 [_ *IWICBitmapFrameDecode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) 。</span><span class="sxs-lookup"><span data-stu-id="ae297-111">The [_ *IWICBitmapFrameDecode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) to create the [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) from.</span></span>

</dd> <dt>

<span data-ttu-id="ae297-112">*ppIFME* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ae297-112">*ppIFME* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae297-113">類型： **[ **IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)\*\***</span><span class="sxs-lookup"><span data-stu-id="ae297-113">Type: **[**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)\*\***</span></span>

<span data-ttu-id="ae297-114">接收新 [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)指標的指標。</span><span class="sxs-lookup"><span data-stu-id="ae297-114">A pointer that receives a pointer to a new [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae297-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="ae297-115">Return value</span></span>

<span data-ttu-id="ae297-116">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ae297-116">Type: **HRESULT**</span></span>

<span data-ttu-id="ae297-117">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="ae297-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ae297-118">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ae297-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae297-119">備註</span><span class="sxs-lookup"><span data-stu-id="ae297-119">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="ae297-120">需求</span><span class="sxs-lookup"><span data-stu-id="ae297-120">Requirements</span></span>



| <span data-ttu-id="ae297-121">需求</span><span class="sxs-lookup"><span data-stu-id="ae297-121">Requirement</span></span> | <span data-ttu-id="ae297-122">值</span><span class="sxs-lookup"><span data-stu-id="ae297-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae297-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ae297-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ae297-124">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ae297-124">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="ae297-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ae297-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ae297-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ae297-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="ae297-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ae297-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae297-128"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae297-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




