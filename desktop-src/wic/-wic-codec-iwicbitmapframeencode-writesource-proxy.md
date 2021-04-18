---
description: WriteSource 方法的 Proxy 函式。
ms.assetid: d95ad80f-7a26-45a7-8103-2673989143b7
title: IWICBitmapFrameEncode_WriteSource_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_WriteSource_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 9eb5ab9db9341d138c72d350304407966a6293d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195447"
---
# <a name="iwicbitmapframeencode_writesource_proxy-function"></a><span data-ttu-id="a77ea-103">IWICBitmapFrameEncode \_ WriteSource \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="a77ea-103">IWICBitmapFrameEncode\_WriteSource\_Proxy function</span></span>

<span data-ttu-id="a77ea-104">[**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="a77ea-104">Proxy function for the [**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a77ea-105">語法</span><span class="sxs-lookup"><span data-stu-id="a77ea-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_WriteSource_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ IWICBitmapSource      *pIBitmapSource,
  _In_ WICRect               *prc
);
```



## <a name="parameters"></a><span data-ttu-id="a77ea-106">參數</span><span class="sxs-lookup"><span data-stu-id="a77ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a77ea-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="a77ea-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a77ea-108">類型： \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="a77ea-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="a77ea-109">這個 [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="a77ea-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="a77ea-110">*pIBitmapSource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a77ea-110">*pIBitmapSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a77ea-111">類型： \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="a77ea-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="a77ea-112">要編碼的點陣圖來源。</span><span class="sxs-lookup"><span data-stu-id="a77ea-112">The bitmap source to encode.</span></span>

</dd> <dt>

<span data-ttu-id="a77ea-113">_prc \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a77ea-113">_prc\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a77ea-114">類型： \**[**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \** _</span><span class="sxs-lookup"><span data-stu-id="a77ea-114">Type: \**[**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect)\** _</span></span>

<span data-ttu-id="a77ea-115">點陣圖來源的大小矩形。</span><span class="sxs-lookup"><span data-stu-id="a77ea-115">The size rectangle of the bitmap source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a77ea-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="a77ea-116">Return value</span></span>

<span data-ttu-id="a77ea-117">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="a77ea-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="a77ea-118">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="a77ea-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a77ea-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a77ea-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a77ea-120">備註</span><span class="sxs-lookup"><span data-stu-id="a77ea-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="a77ea-121">需求</span><span class="sxs-lookup"><span data-stu-id="a77ea-121">Requirements</span></span>



| <span data-ttu-id="a77ea-122">需求</span><span class="sxs-lookup"><span data-stu-id="a77ea-122">Requirement</span></span> | <span data-ttu-id="a77ea-123">值</span><span class="sxs-lookup"><span data-stu-id="a77ea-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a77ea-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a77ea-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a77ea-125">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a77ea-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="a77ea-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a77ea-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a77ea-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a77ea-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="a77ea-128">DLL</span><span class="sxs-lookup"><span data-stu-id="a77ea-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a77ea-129"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a77ea-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




