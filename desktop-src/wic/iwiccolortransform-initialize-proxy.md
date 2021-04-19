---
description: 初始化具有 IWICBitmapSource 的 IWICColorTransform，並將它從一個 IWICColorCoNtext 轉換成另一個。
ms.assetid: 68C8EF36-DFFF-4FF3-BD9A-583508F9C2B1
title: IWICColorTransform_Initialize_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICColorTransform_Initialize_Proxy
api_type:
- DllExport
api_location:
- WindowsCodecsExt.dll
ms.openlocfilehash: 29d29bfd925d979897b22711c748083b94673142
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995279"
---
# <a name="iwiccolortransform_initialize_proxy-function"></a><span data-ttu-id="091ed-103">IWICColorTransform \_ Initialize \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="091ed-103">IWICColorTransform\_Initialize\_Proxy function</span></span>

<span data-ttu-id="091ed-104">初始化具有 [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)的 [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) ，並將它從一個 [**IWICColorCoNtext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)轉換成另一個。</span><span class="sxs-lookup"><span data-stu-id="091ed-104">Initializes an [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) with a [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) and transforms it from one [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) to another.</span></span>

## <a name="syntax"></a><span data-ttu-id="091ed-105">語法</span><span class="sxs-lookup"><span data-stu-id="091ed-105">Syntax</span></span>


```C++
HRESULT IWICColorTransform_Initialize_Proxy(
  _In_ IWICColorTransform    *pIColorTransform,
  _In_ IWICBitmapSource      *pIBitmapSource,
  _In_ IWICColorContext      *pIContextSource,
  _In_ IWICColorContext      *pIContextDest,
  _In_ REFWICPixelFormatGUID pixelFmtDest
);
```



## <a name="parameters"></a><span data-ttu-id="091ed-106">參數</span><span class="sxs-lookup"><span data-stu-id="091ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="091ed-107">*pIColorTransform* \[在\]</span><span class="sxs-lookup"><span data-stu-id="091ed-107">*pIColorTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="091ed-108">類型： **[ **IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform)\***</span><span class="sxs-lookup"><span data-stu-id="091ed-108">Type: **[**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform)\***</span></span>

<span data-ttu-id="091ed-109">要初始化的色彩轉換。</span><span class="sxs-lookup"><span data-stu-id="091ed-109">The color transform to initialize.</span></span>

</dd> <dt>

<span data-ttu-id="091ed-110">*pIBitmapSource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="091ed-110">*pIBitmapSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="091ed-111">類型： **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="091ed-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="091ed-112">用來初始化色彩轉換的點陣圖來源。</span><span class="sxs-lookup"><span data-stu-id="091ed-112">The bitmap source used to initialize the color transform.</span></span>

</dd> <dt>

<span data-ttu-id="091ed-113">*pICoNtextSource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="091ed-113">*pIContextSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="091ed-114">類型： **[ **IWICColorCoNtext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***</span><span class="sxs-lookup"><span data-stu-id="091ed-114">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***</span></span>

<span data-ttu-id="091ed-115">色彩內容來源。</span><span class="sxs-lookup"><span data-stu-id="091ed-115">The color context source.</span></span>

</dd> <dt>

<span data-ttu-id="091ed-116">*pICoNtextDest* \[在\]</span><span class="sxs-lookup"><span data-stu-id="091ed-116">*pIContextDest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="091ed-117">類型： **[ **IWICColorCoNtext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***</span><span class="sxs-lookup"><span data-stu-id="091ed-117">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***</span></span>

<span data-ttu-id="091ed-118">色彩內容目的地。</span><span class="sxs-lookup"><span data-stu-id="091ed-118">The color context destination.</span></span>

</dd> <dt>

<span data-ttu-id="091ed-119">*pixelFmtDest* \[在\]</span><span class="sxs-lookup"><span data-stu-id="091ed-119">*pixelFmtDest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="091ed-120">類型： **REFWICPixelFormatGUID**</span><span class="sxs-lookup"><span data-stu-id="091ed-120">Type: **REFWICPixelFormatGUID**</span></span>

<span data-ttu-id="091ed-121">所需像素格式的 GUID。</span><span class="sxs-lookup"><span data-stu-id="091ed-121">The GUID of the desired pixel format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="091ed-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="091ed-122">Return value</span></span>

<span data-ttu-id="091ed-123">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="091ed-123">Type: **HRESULT**</span></span>

<span data-ttu-id="091ed-124">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="091ed-124">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="091ed-125">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="091ed-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="091ed-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="091ed-126">Requirements</span></span>



| <span data-ttu-id="091ed-127">需求</span><span class="sxs-lookup"><span data-stu-id="091ed-127">Requirement</span></span> | <span data-ttu-id="091ed-128">值</span><span class="sxs-lookup"><span data-stu-id="091ed-128">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="091ed-129">DLL</span><span class="sxs-lookup"><span data-stu-id="091ed-129">DLL</span></span><br/> | <dl> <span data-ttu-id="091ed-130"><dt>WindowsCodecsExt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="091ed-130"><dt>WindowsCodecsExt.dll</dt></span></span> </dl> |



 

 




