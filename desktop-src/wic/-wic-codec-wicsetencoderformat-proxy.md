---
description: 用於協調編碼器之像素格式和調色板的 Proxy 函式。
ms.assetid: 01179598-ba40-4aed-a7c4-888cb4e851f4
title: WICSetEncoderFormat_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICSetEncoderFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 7ea0988d29d1d9ed04668dfbe8ce86b97af6534a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974722"
---
# <a name="wicsetencoderformat_proxy-function"></a><span data-ttu-id="9d9ca-103">WICSetEncoderFormat \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="9d9ca-103">WICSetEncoderFormat\_Proxy function</span></span>

<span data-ttu-id="9d9ca-104">用於協調編碼器之像素格式和調色板的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="9d9ca-104">Proxy function for negotiating the pixel format and the palette for the encoder.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d9ca-105">語法</span><span class="sxs-lookup"><span data-stu-id="9d9ca-105">Syntax</span></span>


```C++
HRESULT WICSetEncoderFormat_Proxy(
  _In_  IWICBitmapSource      *pSourceIn,
  _In_  IWICPalette           *pIPalette,
  _In_  IWICBitmapFrameEncode *pIFrameEncode,
  _Out_ IWICBitmapSource      **ppSourceOut
);
```



## <a name="parameters"></a><span data-ttu-id="9d9ca-106">參數</span><span class="sxs-lookup"><span data-stu-id="9d9ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d9ca-107">*pSourceIn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9d9ca-107">*pSourceIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d9ca-108">類型： \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="9d9ca-108">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="9d9ca-109">來源點陣圖的指標。</span><span class="sxs-lookup"><span data-stu-id="9d9ca-109">Pointer to the source bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="9d9ca-110">_pIPalette \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9d9ca-110">_pIPalette\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d9ca-111">類型： \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="9d9ca-111">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="9d9ca-112">要用於編碼之調色板的指標。</span><span class="sxs-lookup"><span data-stu-id="9d9ca-112">Pointer to the palette to use for encoding.</span></span>

</dd> <dt>

<span data-ttu-id="9d9ca-113">_pIFrameEncode \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9d9ca-113">_pIFrameEncode\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d9ca-114">類型： \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="9d9ca-114">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="9d9ca-115">框架編碼物件的指標。</span><span class="sxs-lookup"><span data-stu-id="9d9ca-115">Pointer to the frame encode object.</span></span>

</dd> <dt>

<span data-ttu-id="9d9ca-116">_ppSourceOut \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="9d9ca-116">_ppSourceOut\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d9ca-117">類型： **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span><span class="sxs-lookup"><span data-stu-id="9d9ca-117">Type: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***</span></span>

<span data-ttu-id="9d9ca-118">接收輸出來源指標的指標。</span><span class="sxs-lookup"><span data-stu-id="9d9ca-118">Pointer that receives a pointer to the output source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d9ca-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="9d9ca-119">Return value</span></span>

<span data-ttu-id="9d9ca-120">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9d9ca-120">Type: **HRESULT**</span></span>

<span data-ttu-id="9d9ca-121">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="9d9ca-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9d9ca-122">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9d9ca-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d9ca-123">備註</span><span class="sxs-lookup"><span data-stu-id="9d9ca-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="9d9ca-124">需求</span><span class="sxs-lookup"><span data-stu-id="9d9ca-124">Requirements</span></span>



| <span data-ttu-id="9d9ca-125">需求</span><span class="sxs-lookup"><span data-stu-id="9d9ca-125">Requirement</span></span> | <span data-ttu-id="9d9ca-126">值</span><span class="sxs-lookup"><span data-stu-id="9d9ca-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d9ca-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9d9ca-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9d9ca-128">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9d9ca-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="9d9ca-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9d9ca-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9d9ca-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9d9ca-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="9d9ca-131">DLL</span><span class="sxs-lookup"><span data-stu-id="9d9ca-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d9ca-132"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9d9ca-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




