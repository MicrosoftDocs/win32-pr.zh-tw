---
description: CreateBitmapFlipRotator 方法的 Proxy 函式。
ms.assetid: 1dc55744-8ae1-4d8b-9ffd-735ee45ceb47
title: IWICImagingFactory_CreateBitmapFlipRotator_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFlipRotator_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: dea33ea75ad9d9626b327ee0173abc2f28a3e417
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980618"
---
# <a name="iwicimagingfactory_createbitmapfliprotator_proxy-function"></a><span data-ttu-id="e6cac-103">IWICImagingFactory \_ CreateBitmapFlipRotator \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="e6cac-103">IWICImagingFactory\_CreateBitmapFlipRotator\_Proxy function</span></span>

<span data-ttu-id="e6cac-104">[**CreateBitmapFlipRotator**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfliprotator)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="e6cac-104">Proxy function for the [**CreateBitmapFlipRotator**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfliprotator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6cac-105">語法</span><span class="sxs-lookup"><span data-stu-id="e6cac-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapFlipRotator_Proxy(
  _In_  IWICImagingFactory    *pFactory,
  _Out_ IWICBitmapFlipRotator **ppIBitmapFlipRotator
);
```



## <a name="parameters"></a><span data-ttu-id="e6cac-106">參數</span><span class="sxs-lookup"><span data-stu-id="e6cac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6cac-107">*pFactory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e6cac-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6cac-108">類型： \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="e6cac-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="e6cac-109">_ppIBitmapFlipRotator \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e6cac-109">_ppIBitmapFlipRotator\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6cac-110">類型： **[ **IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)\*\***</span><span class="sxs-lookup"><span data-stu-id="e6cac-110">Type: **[**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)\*\***</span></span>

<span data-ttu-id="e6cac-111">接收新 [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)指標的指標。</span><span class="sxs-lookup"><span data-stu-id="e6cac-111">A pointer that receives a pointer to a new [**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6cac-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="e6cac-112">Return value</span></span>

<span data-ttu-id="e6cac-113">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e6cac-113">Type: **HRESULT**</span></span>

<span data-ttu-id="e6cac-114">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="e6cac-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e6cac-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e6cac-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6cac-116">備註</span><span class="sxs-lookup"><span data-stu-id="e6cac-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="e6cac-117">需求</span><span class="sxs-lookup"><span data-stu-id="e6cac-117">Requirements</span></span>



| <span data-ttu-id="e6cac-118">需求</span><span class="sxs-lookup"><span data-stu-id="e6cac-118">Requirement</span></span> | <span data-ttu-id="e6cac-119">值</span><span class="sxs-lookup"><span data-stu-id="e6cac-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6cac-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e6cac-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e6cac-121">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e6cac-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="e6cac-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e6cac-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e6cac-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e6cac-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="e6cac-124">DLL</span><span class="sxs-lookup"><span data-stu-id="e6cac-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6cac-125"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6cac-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




