---
description: GetThumbnail 方法的 IWICBitmapDecoder_GetThumbnail_Proxy 函數 Proxy 函式。
ms.assetid: 37a6ba78-0d1b-47f6-9b12-8ad123c8ee86
title: IWICBitmapDecoder_GetThumbnail_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetThumbnail_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 3fb4d6ae050772bb6392e1d94c88ef5bfc23d2ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100606"
---
# <a name="iwicbitmapdecoder_getthumbnail_proxy-function"></a><span data-ttu-id="9058b-103">IWICBitmapDecoder \_ GetThumbnail \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="9058b-103">IWICBitmapDecoder\_GetThumbnail\_Proxy function</span></span>

<span data-ttu-id="9058b-104">[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="9058b-104">Proxy function for the [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9058b-105">語法</span><span class="sxs-lookup"><span data-stu-id="9058b-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetThumbnail_Proxy(
  _In_  IWICBitmapDecoder *THIS_PTR,
  _Out_ IWICBitmapSource  **ppIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="9058b-106">參數</span><span class="sxs-lookup"><span data-stu-id="9058b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9058b-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="9058b-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9058b-108">類型： **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***</span><span class="sxs-lookup"><span data-stu-id="9058b-108">Type: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***</span></span>

<span data-ttu-id="9058b-109">這個 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="9058b-109">Pointer to this [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="9058b-110">*ppIThumbnail* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9058b-110">*ppIThumbnail* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9058b-111">類型： **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span><span class="sxs-lookup"><span data-stu-id="9058b-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span></span>

<span data-ttu-id="9058b-112">指標，接收縮圖 [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) 的指標。</span><span class="sxs-lookup"><span data-stu-id="9058b-112">A pointer that receives a pointer to the [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) of the thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9058b-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="9058b-113">Return value</span></span>

<span data-ttu-id="9058b-114">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9058b-114">Type: **HRESULT**</span></span>

<span data-ttu-id="9058b-115">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="9058b-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9058b-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9058b-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9058b-117">備註</span><span class="sxs-lookup"><span data-stu-id="9058b-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="9058b-118">需求</span><span class="sxs-lookup"><span data-stu-id="9058b-118">Requirements</span></span>



| <span data-ttu-id="9058b-119">需求</span><span class="sxs-lookup"><span data-stu-id="9058b-119">Requirement</span></span> | <span data-ttu-id="9058b-120">值</span><span class="sxs-lookup"><span data-stu-id="9058b-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9058b-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9058b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9058b-122">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9058b-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="9058b-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9058b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9058b-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9058b-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="9058b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9058b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9058b-126"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9058b-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




