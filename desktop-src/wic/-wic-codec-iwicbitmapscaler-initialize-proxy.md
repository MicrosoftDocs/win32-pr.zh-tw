---
description: Initialize 方法的 Proxy 函式。
ms.assetid: 47a717d2-9aac-4230-bdb3-093212eb5448
title: IWICBitmapScaler_Initialize_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapScaler_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: cc317adc831b0cf0759580d5c6924fb3f0997524
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106999949"
---
# <a name="iwicbitmapscaler_initialize_proxy-function"></a><span data-ttu-id="c8568-103">IWICBitmapScaler \_ Initialize \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="c8568-103">IWICBitmapScaler\_Initialize\_Proxy function</span></span>

<span data-ttu-id="c8568-104">[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapscaler-initialize)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="c8568-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapscaler-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8568-105">語法</span><span class="sxs-lookup"><span data-stu-id="c8568-105">Syntax</span></span>


```C++
HRESULT IWICBitmapScaler_Initialize_Proxy(
  _In_ IWICBitmapScaler           *THIS_PTR,
  _In_ IWICBitmapSource           *pISource,
  _In_ UINT                       uiWidth,
  _In_ UINT                       uiHeight,
  _In_ WICBitmapInterpolationMode mode
);
```



## <a name="parameters"></a><span data-ttu-id="c8568-106">參數</span><span class="sxs-lookup"><span data-stu-id="c8568-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8568-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="c8568-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8568-108">類型： \**[**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) \** _</span><span class="sxs-lookup"><span data-stu-id="c8568-108">Type: \**[**IWICBitmapScaler**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)\** _</span></span>

<span data-ttu-id="c8568-109">這個 [_ *IWICBitmapScaler* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="c8568-109">Pointer to this [_ *IWICBitmapScaler*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapscaler) object.</span></span>

</dd> <dt>

<span data-ttu-id="c8568-110">*pISource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8568-110">*pISource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8568-111">類型： \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="c8568-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="c8568-112">輸入點陣圖來源。</span><span class="sxs-lookup"><span data-stu-id="c8568-112">The input bitmap source.</span></span>

</dd> <dt>

<span data-ttu-id="c8568-113">_uiWidth \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8568-113">_uiWidth\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8568-114">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="c8568-114">Type: **UINT**</span></span>

<span data-ttu-id="c8568-115">目的地寬度。</span><span class="sxs-lookup"><span data-stu-id="c8568-115">The destination width.</span></span>

</dd> <dt>

<span data-ttu-id="c8568-116">*uiHeight* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8568-116">*uiHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8568-117">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="c8568-117">Type: **UINT**</span></span>

<span data-ttu-id="c8568-118">目的地高度。</span><span class="sxs-lookup"><span data-stu-id="c8568-118">The desination height.</span></span>

</dd> <dt>

<span data-ttu-id="c8568-119">*模式* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8568-119">*mode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8568-120">類型： **[ **WICBitmapInterpolationMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapinterpolationmode)**</span><span class="sxs-lookup"><span data-stu-id="c8568-120">Type: **[**WICBitmapInterpolationMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapinterpolationmode)**</span></span>

<span data-ttu-id="c8568-121">調整時要使用的插補模式。</span><span class="sxs-lookup"><span data-stu-id="c8568-121">The interpolation mode to use when scaling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8568-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="c8568-122">Return value</span></span>

<span data-ttu-id="c8568-123">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c8568-123">Type: **HRESULT**</span></span>

<span data-ttu-id="c8568-124">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="c8568-124">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c8568-125">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c8568-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8568-126">備註</span><span class="sxs-lookup"><span data-stu-id="c8568-126">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="c8568-127">需求</span><span class="sxs-lookup"><span data-stu-id="c8568-127">Requirements</span></span>



| <span data-ttu-id="c8568-128">需求</span><span class="sxs-lookup"><span data-stu-id="c8568-128">Requirement</span></span> | <span data-ttu-id="c8568-129">值</span><span class="sxs-lookup"><span data-stu-id="c8568-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8568-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c8568-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c8568-131">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8568-131">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="c8568-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c8568-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c8568-133">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8568-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="c8568-134">DLL</span><span class="sxs-lookup"><span data-stu-id="c8568-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8568-135"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8568-135"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




