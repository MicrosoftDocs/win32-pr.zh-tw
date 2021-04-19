---
description: GetThumbnail 方法的 Proxy 函式。
ms.assetid: 377f8aac-3cdc-44dc-8c60-9b6bce915486
title: IWICBitmapFrameDecode_GetThumbnail_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameDecode_GetThumbnail_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c29b62b4d3839b7cd3db51574f38ab824b215310
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001666"
---
# <a name="iwicbitmapframedecode_getthumbnail_proxy-function"></a><span data-ttu-id="6eca0-103">IWICBitmapFrameDecode \_ GetThumbnail \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="6eca0-103">IWICBitmapFrameDecode\_GetThumbnail\_Proxy function</span></span>

<span data-ttu-id="6eca0-104">[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="6eca0-104">Proxy function for the [**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6eca0-105">語法</span><span class="sxs-lookup"><span data-stu-id="6eca0-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameDecode_GetThumbnail_Proxy(
  _In_  IWICBitmapFrameDecode *THIS_PTR,
  _Out_ IWICBitmapSource      **ppIThumbnail
);
```



## <a name="parameters"></a><span data-ttu-id="6eca0-106">參數</span><span class="sxs-lookup"><span data-stu-id="6eca0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6eca0-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="6eca0-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6eca0-108">類型： \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) \** _</span><span class="sxs-lookup"><span data-stu-id="6eca0-108">Type: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\** _</span></span>

<span data-ttu-id="6eca0-109">這個 [_ *IWICBitmapFrameDecode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="6eca0-109">Pointer to this [_ *IWICBitmapFrameDecode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

</dd> <dt>

<span data-ttu-id="6eca0-110">*ppIThumbnail* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6eca0-110">*ppIThumbnail* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6eca0-111">類型： **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span><span class="sxs-lookup"><span data-stu-id="6eca0-111">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span></span>

<span data-ttu-id="6eca0-112">指標，接收縮圖 [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) 的指標。</span><span class="sxs-lookup"><span data-stu-id="6eca0-112">A pointer that receives a pointer to the [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) of the thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6eca0-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="6eca0-113">Return value</span></span>

<span data-ttu-id="6eca0-114">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6eca0-114">Type: **HRESULT**</span></span>

<span data-ttu-id="6eca0-115">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="6eca0-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6eca0-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6eca0-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6eca0-117">備註</span><span class="sxs-lookup"><span data-stu-id="6eca0-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="6eca0-118">需求</span><span class="sxs-lookup"><span data-stu-id="6eca0-118">Requirements</span></span>



| <span data-ttu-id="6eca0-119">需求</span><span class="sxs-lookup"><span data-stu-id="6eca0-119">Requirement</span></span> | <span data-ttu-id="6eca0-120">值</span><span class="sxs-lookup"><span data-stu-id="6eca0-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6eca0-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6eca0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6eca0-122">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6eca0-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="6eca0-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6eca0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6eca0-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6eca0-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="6eca0-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6eca0-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6eca0-126"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6eca0-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




