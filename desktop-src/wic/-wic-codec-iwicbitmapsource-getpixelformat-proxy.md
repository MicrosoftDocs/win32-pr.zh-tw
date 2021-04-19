---
description: GetPixelFormat 方法的 Proxy 函式。
ms.assetid: 0879bfb7-0175-4275-a093-a69b39c66a41
title: IWICBitmapSource_GetPixelFormat_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_GetPixelFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ff795dd028c8d8f1e18a944df60a87f1e7cee670
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979008"
---
# <a name="iwicbitmapsource_getpixelformat_proxy-function"></a><span data-ttu-id="ad2ca-103">IWICBitmapSource \_ GetPixelFormat \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="ad2ca-103">IWICBitmapSource\_GetPixelFormat\_Proxy function</span></span>

<span data-ttu-id="ad2ca-104">[**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="ad2ca-104">Proxy function for the [**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad2ca-105">語法</span><span class="sxs-lookup"><span data-stu-id="ad2ca-105">Syntax</span></span>


```C++
HRESULT IWICBitmapSource_GetPixelFormat_Proxy(
  _In_  IWICBitmapSource   *THIS_PTR,
  _Out_ WICPixelFormatGUID *pPixelFormat
);
```



## <a name="parameters"></a><span data-ttu-id="ad2ca-106">參數</span><span class="sxs-lookup"><span data-stu-id="ad2ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad2ca-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="ad2ca-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad2ca-108">類型： \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="ad2ca-108">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="ad2ca-109">這個 [_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="ad2ca-109">Pointer to this [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span>

</dd> <dt>

<span data-ttu-id="ad2ca-110">*pPixelFormat* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ad2ca-110">*pPixelFormat* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad2ca-111">類型： \**WICPixelFormatGUID \** _</span><span class="sxs-lookup"><span data-stu-id="ad2ca-111">Type: \**WICPixelFormatGUID\** _</span></span>

<span data-ttu-id="ad2ca-112">用來接收點陣圖儲存位置之像素格式 GUID 的指標。</span><span class="sxs-lookup"><span data-stu-id="ad2ca-112">A pointer that receives the pixel format GUID the bitmap is stored in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad2ca-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ad2ca-113">Return value</span></span>

<span data-ttu-id="ad2ca-114">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="ad2ca-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="ad2ca-115">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="ad2ca-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ad2ca-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ad2ca-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad2ca-117">備註</span><span class="sxs-lookup"><span data-stu-id="ad2ca-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="ad2ca-118">需求</span><span class="sxs-lookup"><span data-stu-id="ad2ca-118">Requirements</span></span>



| <span data-ttu-id="ad2ca-119">需求</span><span class="sxs-lookup"><span data-stu-id="ad2ca-119">Requirement</span></span> | <span data-ttu-id="ad2ca-120">值</span><span class="sxs-lookup"><span data-stu-id="ad2ca-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad2ca-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ad2ca-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ad2ca-122">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ad2ca-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="ad2ca-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ad2ca-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ad2ca-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ad2ca-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="ad2ca-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ad2ca-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad2ca-126"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad2ca-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




