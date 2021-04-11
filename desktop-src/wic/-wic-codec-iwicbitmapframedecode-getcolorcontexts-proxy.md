---
description: GetColorCoNtexts 方法的 Proxy 函式。
ms.assetid: 1925a64e-558d-4931-a3c3-b35d2b92a292
title: IWICBitmapFrameDecode_GetColorCoNtexts_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameDecode_GetColorContexts_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 8e22166e98e4ef276a6bf1d72dfc860cf8fb511e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191290"
---
# <a name="iwicbitmapframedecode_getcolorcontexts_proxy-function"></a><span data-ttu-id="00cc5-103">IWICBitmapFrameDecode \_ GetColorCoNtexts \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="00cc5-103">IWICBitmapFrameDecode\_GetColorContexts\_Proxy function</span></span>

<span data-ttu-id="00cc5-104">[**GetColorCoNtexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="00cc5-104">Proxy function for the [**GetColorContexts**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="00cc5-105">語法</span><span class="sxs-lookup"><span data-stu-id="00cc5-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameDecode_GetColorContexts_Proxy(
  _In_    IWICBitmapFrameDecode *THIS_PTR,
  _In_    UINT                  cCount,
  _Inout_ IWICColorContext      **ppIColorContexts,
  _Out_   UINT                  *pcActualCount
);
```



## <a name="parameters"></a><span data-ttu-id="00cc5-106">參數</span><span class="sxs-lookup"><span data-stu-id="00cc5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00cc5-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="00cc5-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00cc5-108">類型： \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) \** _</span><span class="sxs-lookup"><span data-stu-id="00cc5-108">Type: \**[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\** _</span></span>

<span data-ttu-id="00cc5-109">這個 [_ *IWICBitmapFrameDecode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="00cc5-109">Pointer to this [_ *IWICBitmapFrameDecode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) object.</span></span>

</dd> <dt>

<span data-ttu-id="00cc5-110">*帳戶 c)* \[在\]</span><span class="sxs-lookup"><span data-stu-id="00cc5-110">*cCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00cc5-111">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="00cc5-111">Type: **UINT**</span></span>

<span data-ttu-id="00cc5-112">要取出的色彩內容數目。</span><span class="sxs-lookup"><span data-stu-id="00cc5-112">The number of color contexts to retrieve.</span></span>

<span data-ttu-id="00cc5-113">此值的大小必須等於或小於 *ppIColorCoNtexts* 可用的大小。</span><span class="sxs-lookup"><span data-stu-id="00cc5-113">This value must be the size of, or smaller than, the size available to *ppIColorContexts*.</span></span>

</dd> <dt>

<span data-ttu-id="00cc5-114">*ppIColorCoNtexts* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="00cc5-114">*ppIColorContexts* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="00cc5-115">類型： **[ **IWICColorCoNtext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span><span class="sxs-lookup"><span data-stu-id="00cc5-115">Type: **[**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\*\***</span></span>

<span data-ttu-id="00cc5-116">接收 [**IWICColorCoNtext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) 物件之指標的指標。</span><span class="sxs-lookup"><span data-stu-id="00cc5-116">A pointer that receives a pointer to the [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) objects.</span></span>

</dd> <dt>

<span data-ttu-id="00cc5-117">*pcActualCount* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="00cc5-117">*pcActualCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00cc5-118">類型： \**UINT \** _</span><span class="sxs-lookup"><span data-stu-id="00cc5-118">Type: \**UINT\** _</span></span>

<span data-ttu-id="00cc5-119">指標，接收影像框架中包含的色彩內容數目。</span><span class="sxs-lookup"><span data-stu-id="00cc5-119">A pointer that receives the number of color contexts contained in the image frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00cc5-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="00cc5-120">Return value</span></span>

<span data-ttu-id="00cc5-121">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="00cc5-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="00cc5-122">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="00cc5-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="00cc5-123">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="00cc5-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="00cc5-124">備註</span><span class="sxs-lookup"><span data-stu-id="00cc5-124">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="00cc5-125">需求</span><span class="sxs-lookup"><span data-stu-id="00cc5-125">Requirements</span></span>



| <span data-ttu-id="00cc5-126">需求</span><span class="sxs-lookup"><span data-stu-id="00cc5-126">Requirement</span></span> | <span data-ttu-id="00cc5-127">值</span><span class="sxs-lookup"><span data-stu-id="00cc5-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00cc5-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="00cc5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="00cc5-129">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="00cc5-129">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="00cc5-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="00cc5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="00cc5-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="00cc5-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="00cc5-132">DLL</span><span class="sxs-lookup"><span data-stu-id="00cc5-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00cc5-133"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="00cc5-133"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




