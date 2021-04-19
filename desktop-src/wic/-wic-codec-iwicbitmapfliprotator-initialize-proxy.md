---
description: Initialize 方法的 Proxy 函式。
ms.assetid: 860e8092-054d-489e-8ca1-fec43a039eca
title: IWICBitmapFlipRotator_Initialize_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFlipRotator_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 82a1aa5648edd47d0b635a407adc001c25183b50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970407"
---
# <a name="iwicbitmapfliprotator_initialize_proxy-function"></a><span data-ttu-id="c1147-103">IWICBitmapFlipRotator \_ Initialize \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="c1147-103">IWICBitmapFlipRotator\_Initialize\_Proxy function</span></span>

<span data-ttu-id="c1147-104">[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapfliprotator-initialize)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="c1147-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapfliprotator-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1147-105">語法</span><span class="sxs-lookup"><span data-stu-id="c1147-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFlipRotator_Initialize_Proxy(
  _In_ IWICBitmapFlipRotator     *THIS_PTR,
  _In_ IWICBitmapSource          *pISource,
  _In_ WICBitmapTransformOptions options
);
```



## <a name="parameters"></a><span data-ttu-id="c1147-106">參數</span><span class="sxs-lookup"><span data-stu-id="c1147-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1147-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="c1147-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1147-108">類型： \**[**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) \** _</span><span class="sxs-lookup"><span data-stu-id="c1147-108">Type: \**[**IWICBitmapFlipRotator**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)\** _</span></span>

<span data-ttu-id="c1147-109">這個 [_ *IWICBitmapFlipRotator* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="c1147-109">Pointer to this [_ *IWICBitmapFlipRotator*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapfliprotator) object.</span></span>

</dd> <dt>

<span data-ttu-id="c1147-110">*pISource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c1147-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1147-111">類型： \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="c1147-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="c1147-112">輸入點陣圖來源。</span><span class="sxs-lookup"><span data-stu-id="c1147-112">The input bitmap source.</span></span>

</dd> <dt>

<span data-ttu-id="c1147-113">_options \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1147-113">_options\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1147-114">類型： **[ **WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)**</span><span class="sxs-lookup"><span data-stu-id="c1147-114">Type: **[**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)**</span></span>

<span data-ttu-id="c1147-115">要翻轉或旋轉影像的 [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) 。</span><span class="sxs-lookup"><span data-stu-id="c1147-115">The [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) to flip or rotate the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1147-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="c1147-116">Return value</span></span>

<span data-ttu-id="c1147-117">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c1147-117">Type: **HRESULT**</span></span>

<span data-ttu-id="c1147-118">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="c1147-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c1147-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c1147-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1147-120">備註</span><span class="sxs-lookup"><span data-stu-id="c1147-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="c1147-121">需求</span><span class="sxs-lookup"><span data-stu-id="c1147-121">Requirements</span></span>



| <span data-ttu-id="c1147-122">需求</span><span class="sxs-lookup"><span data-stu-id="c1147-122">Requirement</span></span> | <span data-ttu-id="c1147-123">值</span><span class="sxs-lookup"><span data-stu-id="c1147-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1147-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c1147-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c1147-125">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c1147-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="c1147-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c1147-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c1147-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c1147-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="c1147-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c1147-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1147-129"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c1147-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




