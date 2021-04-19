---
description: CreateEncoder 方法的 Proxy 函式。
ms.assetid: e3ffad7f-eb0e-481d-81ee-caf18e14ba59
title: IWICImagingFactory_CreateEncoder_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateEncoder_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 38e5dd19ddc07de42f8be9e8c887a4f412a853b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982473"
---
# <a name="iwicimagingfactory_createencoder_proxy-function"></a><span data-ttu-id="68297-103">IWICImagingFactory \_ CreateEncoder \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="68297-103">IWICImagingFactory\_CreateEncoder\_Proxy function</span></span>

<span data-ttu-id="68297-104">[**CreateEncoder**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createencoder)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="68297-104">Proxy function for the [**CreateEncoder**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createencoder) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="68297-105">語法</span><span class="sxs-lookup"><span data-stu-id="68297-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateEncoder_Proxy(
  _In_           IWICImagingFactory *pFactory,
  _In_           REFGUID            guidContainerFormat,
  _In_opt_ const GUID               *pguidVendor,
  _Out_          IWICBitmapEncoder  **ppIEncoder
);
```



## <a name="parameters"></a><span data-ttu-id="68297-106">參數</span><span class="sxs-lookup"><span data-stu-id="68297-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68297-107">*pFactory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="68297-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68297-108">類型： \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="68297-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="68297-109">_guidContainerFormat \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="68297-109">_guidContainerFormat\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68297-110">類型： **REFGUID**</span><span class="sxs-lookup"><span data-stu-id="68297-110">Type: **REFGUID**</span></span>

<span data-ttu-id="68297-111">所需容器格式的 GUID。</span><span class="sxs-lookup"><span data-stu-id="68297-111">The GUID for the desired container format.</span></span>

</dd> <dt>

<span data-ttu-id="68297-112">*pguidVendor* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="68297-112">*pguidVendor* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="68297-113">類型： \**CONST GUID \** _</span><span class="sxs-lookup"><span data-stu-id="68297-113">Type: \**const GUID\** _</span></span>

<span data-ttu-id="68297-114">編碼器的廠商 GUID。</span><span class="sxs-lookup"><span data-stu-id="68297-114">The vendor GUID for the encoder.</span></span>

</dd> <dt>

<span data-ttu-id="68297-115">_ppIEncoder \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="68297-115">_ppIEncoder\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68297-116">類型： **[ **IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\*\***</span><span class="sxs-lookup"><span data-stu-id="68297-116">Type: **[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\*\***</span></span>

<span data-ttu-id="68297-117">接收新 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)指標的指標。</span><span class="sxs-lookup"><span data-stu-id="68297-117">A pointer that receives a pointer to a new [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68297-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="68297-118">Return value</span></span>

<span data-ttu-id="68297-119">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="68297-119">Type: **HRESULT**</span></span>

<span data-ttu-id="68297-120">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="68297-120">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="68297-121">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="68297-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="68297-122">備註</span><span class="sxs-lookup"><span data-stu-id="68297-122">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="68297-123">需求</span><span class="sxs-lookup"><span data-stu-id="68297-123">Requirements</span></span>



| <span data-ttu-id="68297-124">需求</span><span class="sxs-lookup"><span data-stu-id="68297-124">Requirement</span></span> | <span data-ttu-id="68297-125">值</span><span class="sxs-lookup"><span data-stu-id="68297-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68297-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="68297-126">Minimum supported client</span></span><br/> | <span data-ttu-id="68297-127">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="68297-127">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="68297-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="68297-128">Minimum supported server</span></span><br/> | <span data-ttu-id="68297-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="68297-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="68297-130">DLL</span><span class="sxs-lookup"><span data-stu-id="68297-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68297-131"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="68297-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




