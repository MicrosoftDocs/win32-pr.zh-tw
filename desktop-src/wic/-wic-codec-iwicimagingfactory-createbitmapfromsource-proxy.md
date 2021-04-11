---
description: CreateBitmapFromSource 方法的 Proxy 函式。
ms.assetid: 7d000377-1855-4971-b782-4c0bf7968c5f
title: IWICImagingFactory_CreateBitmapFromSource_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromSource_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: a7f7be9ca9eaa8aa14dcaf3617face2dff2f52f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945438"
---
# <a name="iwicimagingfactory_createbitmapfromsource_proxy-function"></a><span data-ttu-id="4936a-103">IWICImagingFactory \_ CreateBitmapFromSource \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="4936a-103">IWICImagingFactory\_CreateBitmapFromSource\_Proxy function</span></span>

<span data-ttu-id="4936a-104">[**CreateBitmapFromSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromsource)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="4936a-104">Proxy function for the [**CreateBitmapFromSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromsource) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4936a-105">語法</span><span class="sxs-lookup"><span data-stu-id="4936a-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapFromSource_Proxy(
  _In_  IWICImagingFactory         *pFactory,
  _In_  IWICBitmapSource           *pIBitmapSource,
  _In_  WICBitmapCreateCacheOption option,
  _Out_ IWICBitmap                 **ppIBitmap
);
```



## <a name="parameters"></a><span data-ttu-id="4936a-106">參數</span><span class="sxs-lookup"><span data-stu-id="4936a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4936a-107">*pFactory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4936a-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4936a-108">類型： \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="4936a-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="4936a-109">_pIBitmapSource \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4936a-109">_pIBitmapSource\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4936a-110">類型： \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="4936a-110">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="4936a-111">要從中建立點陣圖的 [_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) 。</span><span class="sxs-lookup"><span data-stu-id="4936a-111">The [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) to create the bitmap from.</span></span>

</dd> <dt>

<span data-ttu-id="4936a-112">*選項* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4936a-112">*option* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4936a-113">類型： **[ **WICBitmapCreateCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapcreatecacheoption)**</span><span class="sxs-lookup"><span data-stu-id="4936a-113">Type: **[**WICBitmapCreateCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapcreatecacheoption)**</span></span>

<span data-ttu-id="4936a-114">新點陣圖的快取選項。</span><span class="sxs-lookup"><span data-stu-id="4936a-114">The cache options of the new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="4936a-115">*ppIBitmap* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4936a-115">*ppIBitmap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4936a-116">類型： **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span><span class="sxs-lookup"><span data-stu-id="4936a-116">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span></span>

<span data-ttu-id="4936a-117">接收新點陣圖指標的指標。</span><span class="sxs-lookup"><span data-stu-id="4936a-117">A pointer that receives a pointer to the new bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4936a-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="4936a-118">Return value</span></span>

<span data-ttu-id="4936a-119">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4936a-119">Type: **HRESULT**</span></span>

<span data-ttu-id="4936a-120">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="4936a-120">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4936a-121">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4936a-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4936a-122">備註</span><span class="sxs-lookup"><span data-stu-id="4936a-122">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="4936a-123">需求</span><span class="sxs-lookup"><span data-stu-id="4936a-123">Requirements</span></span>



| <span data-ttu-id="4936a-124">需求</span><span class="sxs-lookup"><span data-stu-id="4936a-124">Requirement</span></span> | <span data-ttu-id="4936a-125">值</span><span class="sxs-lookup"><span data-stu-id="4936a-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4936a-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4936a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4936a-127">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4936a-127">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="4936a-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4936a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4936a-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4936a-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="4936a-130">DLL</span><span class="sxs-lookup"><span data-stu-id="4936a-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4936a-131"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4936a-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




