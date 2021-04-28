---
description: SetThumbnail 方法的 IWICBitmapFrameEncode_SetThumbnail_Proxy 函數 Proxy 函式。
ms.assetid: 3ad473ec-9218-4ed1-961d-a2aa0d542119
title: IWICBitmapFrameEncode_SetThumbnail_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_SetThumbnail_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 9af9dd2d4f8fe71a6dc94420db17383a5da6da28
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116596"
---
# <a name="iwicbitmapframeencode_setthumbnail_proxy-function"></a><span data-ttu-id="d7d7e-103">IWICBitmapFrameEncode \_ SetThumbnail \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="d7d7e-103">IWICBitmapFrameEncode\_SetThumbnail\_Proxy function</span></span>

<span data-ttu-id="d7d7e-104">[**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="d7d7e-104">Proxy function for the [**SetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7d7e-105">語法</span><span class="sxs-lookup"><span data-stu-id="d7d7e-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_SetThumbnail_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ IWICBitmapSource      *pIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="d7d7e-106">參數</span><span class="sxs-lookup"><span data-stu-id="d7d7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7d7e-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="d7d7e-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7d7e-108">類型： **[ **IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span><span class="sxs-lookup"><span data-stu-id="d7d7e-108">Type: **[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span></span>

<span data-ttu-id="d7d7e-109">這個 [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="d7d7e-109">Pointer to this [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="d7d7e-110">*pIThumbnail* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d7d7e-110">*pIThumbnail* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7d7e-111">類型： **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span><span class="sxs-lookup"><span data-stu-id="d7d7e-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***</span></span>

<span data-ttu-id="d7d7e-112">要做為縮圖使用的點陣圖來源。</span><span class="sxs-lookup"><span data-stu-id="d7d7e-112">The bitmap source to use as the thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7d7e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d7d7e-113">Return value</span></span>

<span data-ttu-id="d7d7e-114">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d7d7e-114">Type: **HRESULT**</span></span>

<span data-ttu-id="d7d7e-115">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="d7d7e-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d7d7e-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d7d7e-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7d7e-117">備註</span><span class="sxs-lookup"><span data-stu-id="d7d7e-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="d7d7e-118">需求</span><span class="sxs-lookup"><span data-stu-id="d7d7e-118">Requirements</span></span>



| <span data-ttu-id="d7d7e-119">需求</span><span class="sxs-lookup"><span data-stu-id="d7d7e-119">Requirement</span></span> | <span data-ttu-id="d7d7e-120">值</span><span class="sxs-lookup"><span data-stu-id="d7d7e-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7d7e-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d7d7e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d7d7e-122">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7d7e-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="d7d7e-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d7d7e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d7d7e-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7d7e-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="d7d7e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d7d7e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7d7e-126"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7d7e-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




