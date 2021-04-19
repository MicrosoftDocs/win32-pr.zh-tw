---
description: GetBitsPerPixel 方法的 Proxy 函式。
ms.assetid: bb98daeb-3886-473b-9c8e-5c606602249a
title: IWICPixelFormatInfo_GetBitsPerPixel_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPixelFormatInfo_GetBitsPerPixel_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: f8d3469ca7c1eacf1f6755cbf5b6243527639d30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997908"
---
# <a name="iwicpixelformatinfo_getbitsperpixel_proxy-function"></a><span data-ttu-id="ef6b5-103">IWICPixelFormatInfo \_ GetBitsPerPixel \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="ef6b5-103">IWICPixelFormatInfo\_GetBitsPerPixel\_Proxy function</span></span>

<span data-ttu-id="ef6b5-104">[**GetBitsPerPixel**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getbitsperpixel)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="ef6b5-104">Proxy function for the [**GetBitsPerPixel**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getbitsperpixel) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef6b5-105">語法</span><span class="sxs-lookup"><span data-stu-id="ef6b5-105">Syntax</span></span>


```C++
HRESULT IWICPixelFormatInfo_GetBitsPerPixel_Proxy(
  _In_  IWICPixelFormatInfo *THIS_PTR,
  _Out_ UINT                *puiBitsPerPixel
);
```



## <a name="parameters"></a><span data-ttu-id="ef6b5-106">參數</span><span class="sxs-lookup"><span data-stu-id="ef6b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef6b5-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="ef6b5-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef6b5-108">類型： \**[**IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="ef6b5-108">Type: \**[**IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo)\** _</span></span>

<span data-ttu-id="ef6b5-109">這個 [_ *IWICPixelFormatInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="ef6b5-109">Pointer to this [_ *IWICPixelFormatInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="ef6b5-110">*puiBitsPerPixel* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ef6b5-110">*puiBitsPerPixel* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef6b5-111">類型： \**UINT \** _</span><span class="sxs-lookup"><span data-stu-id="ef6b5-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="ef6b5-112">接收像素格式 BPP 的指標。</span><span class="sxs-lookup"><span data-stu-id="ef6b5-112">Pointer that receives the BPP of the pixel format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef6b5-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ef6b5-113">Return value</span></span>

<span data-ttu-id="ef6b5-114">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="ef6b5-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="ef6b5-115">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="ef6b5-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ef6b5-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ef6b5-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef6b5-117">備註</span><span class="sxs-lookup"><span data-stu-id="ef6b5-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="ef6b5-118">需求</span><span class="sxs-lookup"><span data-stu-id="ef6b5-118">Requirements</span></span>



| <span data-ttu-id="ef6b5-119">需求</span><span class="sxs-lookup"><span data-stu-id="ef6b5-119">Requirement</span></span> | <span data-ttu-id="ef6b5-120">值</span><span class="sxs-lookup"><span data-stu-id="ef6b5-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef6b5-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ef6b5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ef6b5-122">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ef6b5-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="ef6b5-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ef6b5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ef6b5-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ef6b5-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="ef6b5-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ef6b5-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef6b5-126"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef6b5-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




