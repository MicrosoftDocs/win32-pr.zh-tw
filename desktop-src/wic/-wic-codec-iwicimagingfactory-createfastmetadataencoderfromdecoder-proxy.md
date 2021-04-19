---
description: CreateFastMetadataEncoderFromDecoder 方法的 Proxy 函式。
ms.assetid: eae7ed9c-9205-4e41-91b2-461fd1f5d093
title: IWICImagingFactory_CreateFastMetadataEncoderFromDecoder_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateFastMetadataEncoderFromDecoder_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: cdeb682139feb03c19cd66e999b6e3b8b7b366d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000129"
---
# <a name="iwicimagingfactory_createfastmetadataencoderfromdecoder_proxy-function"></a><span data-ttu-id="ed38f-103">IWICImagingFactory \_ CreateFastMetadataEncoderFromDecoder \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="ed38f-103">IWICImagingFactory\_CreateFastMetadataEncoderFromDecoder\_Proxy function</span></span>

<span data-ttu-id="ed38f-104">[**CreateFastMetadataEncoderFromDecoder**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createfastmetadataencoderfromdecoder)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="ed38f-104">Proxy function for the [**CreateFastMetadataEncoderFromDecoder**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createfastmetadataencoderfromdecoder) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed38f-105">語法</span><span class="sxs-lookup"><span data-stu-id="ed38f-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateFastMetadataEncoderFromDecoder_Proxy(
  _In_  IWICImagingFactory      *pFactory,
  _In_  IWICBitmapDecoder       *pIDecoder,
  _Out_ IWICFastMetadataEncoder **ppIFME
);
```



## <a name="parameters"></a><span data-ttu-id="ed38f-106">參數</span><span class="sxs-lookup"><span data-stu-id="ed38f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed38f-107">*pFactory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ed38f-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed38f-108">類型： \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="ed38f-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="ed38f-109">_pIDecoder \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed38f-109">_pIDecoder\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed38f-110">類型： \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="ed38f-110">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="ed38f-111">用來建立 [_ *IWICFastMetadataEncoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)的解碼器。</span><span class="sxs-lookup"><span data-stu-id="ed38f-111">The decoder to create the [_ *IWICFastMetadataEncoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) from.</span></span>

</dd> <dt>

<span data-ttu-id="ed38f-112">*ppIFME* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ed38f-112">*ppIFME* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed38f-113">類型： **[ **IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)\*\***</span><span class="sxs-lookup"><span data-stu-id="ed38f-113">Type: **[**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)\*\***</span></span>

<span data-ttu-id="ed38f-114">接收新 [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)指標的指標。</span><span class="sxs-lookup"><span data-stu-id="ed38f-114">A pointer that receives a pointer to the new [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed38f-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="ed38f-115">Return value</span></span>

<span data-ttu-id="ed38f-116">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ed38f-116">Type: **HRESULT**</span></span>

<span data-ttu-id="ed38f-117">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="ed38f-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ed38f-118">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ed38f-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed38f-119">備註</span><span class="sxs-lookup"><span data-stu-id="ed38f-119">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="ed38f-120">需求</span><span class="sxs-lookup"><span data-stu-id="ed38f-120">Requirements</span></span>



| <span data-ttu-id="ed38f-121">需求</span><span class="sxs-lookup"><span data-stu-id="ed38f-121">Requirement</span></span> | <span data-ttu-id="ed38f-122">值</span><span class="sxs-lookup"><span data-stu-id="ed38f-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed38f-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ed38f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ed38f-124">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ed38f-124">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="ed38f-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ed38f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ed38f-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ed38f-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="ed38f-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ed38f-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed38f-128"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ed38f-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




