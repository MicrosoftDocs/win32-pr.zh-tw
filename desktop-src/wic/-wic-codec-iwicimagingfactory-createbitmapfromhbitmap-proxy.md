---
description: CreateBitmapFromHBITMAP 方法的 Proxy 函式。
ms.assetid: e4e9a6b4-00d9-4f87-aeec-f2c02c3f44ab
title: IWICImagingFactory_CreateBitmapFromHBITMAP_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromHBITMAP_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 6599a9699e6fb83c1678cd0360f906cc8e0668c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975248"
---
# <a name="iwicimagingfactory_createbitmapfromhbitmap_proxy-function"></a><span data-ttu-id="78b5d-103">IWICImagingFactory \_ CreateBitmapFromHBITMAP \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="78b5d-103">IWICImagingFactory\_CreateBitmapFromHBITMAP\_Proxy function</span></span>

<span data-ttu-id="78b5d-104">[**CreateBitmapFromHBITMAP**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromhbitmap)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="78b5d-104">Proxy function for the [**CreateBitmapFromHBITMAP**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromhbitmap) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="78b5d-105">語法</span><span class="sxs-lookup"><span data-stu-id="78b5d-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapFromHBITMAP_Proxy(
  _In_  IWICImagingFactory          *pFactory,
  _In_  HBITMAP                     hBitmap,
  _In_  HPALETTE                    hPalette,
  _In_  WICBitmapAlphaChannelOption options,
  _Out_ IWICBitmap                  **ppIBitmap
);
```



## <a name="parameters"></a><span data-ttu-id="78b5d-106">參數</span><span class="sxs-lookup"><span data-stu-id="78b5d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78b5d-107">*pFactory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="78b5d-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78b5d-108">類型： \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="78b5d-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="78b5d-109">_hBitmap \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78b5d-109">_hBitmap\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78b5d-110">類型： **HBITMAP**</span><span class="sxs-lookup"><span data-stu-id="78b5d-110">Type: **HBITMAP**</span></span>

<span data-ttu-id="78b5d-111">用來建立點陣圖的點陣圖控制碼。</span><span class="sxs-lookup"><span data-stu-id="78b5d-111">A bitmap handle to create the bitmap from.</span></span>

</dd> <dt>

<span data-ttu-id="78b5d-112">*hPalette* \[在\]</span><span class="sxs-lookup"><span data-stu-id="78b5d-112">*hPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78b5d-113">類型： **HPALETTE**</span><span class="sxs-lookup"><span data-stu-id="78b5d-113">Type: **HPALETTE**</span></span>

<span data-ttu-id="78b5d-114">用來建立點陣圖的調色板控制碼。</span><span class="sxs-lookup"><span data-stu-id="78b5d-114">A palette handle used to create the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="78b5d-115">*選項* \[在\]</span><span class="sxs-lookup"><span data-stu-id="78b5d-115">*options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78b5d-116">類型： **[ **WICBitmapAlphaChannelOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapalphachanneloption)**</span><span class="sxs-lookup"><span data-stu-id="78b5d-116">Type: **[**WICBitmapAlphaChannelOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapalphachanneloption)**</span></span>

<span data-ttu-id="78b5d-117">用來建立點陣圖的 Alpha 通道選項。</span><span class="sxs-lookup"><span data-stu-id="78b5d-117">The alpha channel options to create the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="78b5d-118">*ppIBitmap* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="78b5d-118">*ppIBitmap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="78b5d-119">類型： **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span><span class="sxs-lookup"><span data-stu-id="78b5d-119">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span></span>

<span data-ttu-id="78b5d-120">接收新點陣圖指標的指標。</span><span class="sxs-lookup"><span data-stu-id="78b5d-120">A pointer that receives a pointer to the new bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78b5d-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="78b5d-121">Return value</span></span>

<span data-ttu-id="78b5d-122">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="78b5d-122">Type: **HRESULT**</span></span>

<span data-ttu-id="78b5d-123">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="78b5d-123">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="78b5d-124">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="78b5d-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="78b5d-125">備註</span><span class="sxs-lookup"><span data-stu-id="78b5d-125">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="78b5d-126">需求</span><span class="sxs-lookup"><span data-stu-id="78b5d-126">Requirements</span></span>



| <span data-ttu-id="78b5d-127">需求</span><span class="sxs-lookup"><span data-stu-id="78b5d-127">Requirement</span></span> | <span data-ttu-id="78b5d-128">值</span><span class="sxs-lookup"><span data-stu-id="78b5d-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78b5d-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="78b5d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="78b5d-130">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="78b5d-130">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="78b5d-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="78b5d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="78b5d-132">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="78b5d-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="78b5d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="78b5d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78b5d-134"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="78b5d-134"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




