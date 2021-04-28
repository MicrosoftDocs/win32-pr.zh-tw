---
description: GetColorCoNtexts 方法的 IWICBitmapDecoder_GetColorCoNtexts_Proxy 函數 Proxy 函式。
ms.assetid: 2a6db3bd-d3e1-4e87-a04d-0d1c3ea858fb
title: IWICBitmapDecoder_GetColorCoNtexts_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetColorContexts_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e550ca4ebd863e58a4bd285c48a2a01aad059b03
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086256"
---
# <a name="iwicbitmapdecoder_getcolorcontexts_proxy-function"></a><span data-ttu-id="708c6-103">IWICBitmapDecoder \_ GetColorCoNtexts \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="708c6-103">IWICBitmapDecoder\_GetColorContexts\_Proxy function</span></span>

<span data-ttu-id="708c6-104">[**GetColorCoNtexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcolorcontexts)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="708c6-104">Proxy function for the [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcolorcontexts) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="708c6-105">語法</span><span class="sxs-lookup"><span data-stu-id="708c6-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetColorContexts_Proxy(
  _In_    IWICBitmapDecoder *THIS_PTR,
  _In_    UINT              cCount,
  _Inout_ IWICColorContext  **ppIColorContexts,
  _Out_   UINT              *pcActualCount
);
```



## <a name="parameters"></a><span data-ttu-id="708c6-106">參數</span><span class="sxs-lookup"><span data-stu-id="708c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="708c6-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="708c6-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="708c6-108">類型： **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***</span><span class="sxs-lookup"><span data-stu-id="708c6-108">Type: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***</span></span>

<span data-ttu-id="708c6-109">這個 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="708c6-109">Pointer to this [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="708c6-110">*帳戶 c)* \[在\]</span><span class="sxs-lookup"><span data-stu-id="708c6-110">*cCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="708c6-111">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="708c6-111">Type: **UINT**</span></span>

<span data-ttu-id="708c6-112">要取出的色彩內容數目。</span><span class="sxs-lookup"><span data-stu-id="708c6-112">The number of color contexts to retrieve.</span></span>

<span data-ttu-id="708c6-113">此值的大小必須等於或小於 *ppIColorCoNtexts* 可用的大小。</span><span class="sxs-lookup"><span data-stu-id="708c6-113">This value must be the size of, or smaller than, the size available to *ppIColorContexts*.</span></span>

</dd> <dt>

<span data-ttu-id="708c6-114">*ppIColorCoNtexts* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="708c6-114">*ppIColorContexts* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="708c6-115">類型： **[ **IWICColorCoNtext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span><span class="sxs-lookup"><span data-stu-id="708c6-115">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span></span>

<span data-ttu-id="708c6-116">接收 [**IWICColorCoNtext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)指標的指標。</span><span class="sxs-lookup"><span data-stu-id="708c6-116">A pointer that receives a pointer to the [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext).</span></span>

</dd> <dt>

<span data-ttu-id="708c6-117">*pcActualCount* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="708c6-117">*pcActualCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="708c6-118">類型： **UINT \***</span><span class="sxs-lookup"><span data-stu-id="708c6-118">Type: **UINT\***</span></span>

<span data-ttu-id="708c6-119">指標，接收影像中包含的色彩內容數目。</span><span class="sxs-lookup"><span data-stu-id="708c6-119">A pointer that receives the number of color contexts contained in the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="708c6-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="708c6-120">Return value</span></span>

<span data-ttu-id="708c6-121">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="708c6-121">Type: **HRESULT**</span></span>

<span data-ttu-id="708c6-122">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="708c6-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="708c6-123">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="708c6-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="708c6-124">備註</span><span class="sxs-lookup"><span data-stu-id="708c6-124">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="708c6-125">需求</span><span class="sxs-lookup"><span data-stu-id="708c6-125">Requirements</span></span>



| <span data-ttu-id="708c6-126">需求</span><span class="sxs-lookup"><span data-stu-id="708c6-126">Requirement</span></span> | <span data-ttu-id="708c6-127">值</span><span class="sxs-lookup"><span data-stu-id="708c6-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="708c6-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="708c6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="708c6-129">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="708c6-129">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="708c6-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="708c6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="708c6-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="708c6-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="708c6-132">DLL</span><span class="sxs-lookup"><span data-stu-id="708c6-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="708c6-133"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="708c6-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




