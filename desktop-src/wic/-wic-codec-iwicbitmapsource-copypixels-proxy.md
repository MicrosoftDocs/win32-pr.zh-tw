---
description: CopyPixels 方法的 Proxy 函式。
ms.assetid: 020c11e9-0847-468e-b240-20529f6460cd
title: IWICBitmapSource_CopyPixels_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_CopyPixels_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 5c759bd1731e2f3cbc4da9c40cb590e0f39686de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194411"
---
# <a name="iwicbitmapsource_copypixels_proxy-function"></a><span data-ttu-id="754ac-103">IWICBitmapSource \_ CopyPixels \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="754ac-103">IWICBitmapSource\_CopyPixels\_Proxy function</span></span>

<span data-ttu-id="754ac-104">[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="754ac-104">Proxy function for the [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="754ac-105">語法</span><span class="sxs-lookup"><span data-stu-id="754ac-105">Syntax</span></span>


```C++
HRESULT IWICBitmapSource_CopyPixels_Proxy(
  _In_        IWICBitmapSource *THIS_PTR,
  _In_  const WICRect          *prc,
  _In_        UINT             cbStride,
  _In_        UINT             cbBufferSize,
  _Out_       BYTE             *pbBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="754ac-106">參數</span><span class="sxs-lookup"><span data-stu-id="754ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="754ac-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="754ac-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="754ac-108">類型： \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="754ac-108">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="754ac-109">這個 [_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="754ac-109">Pointer to this [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span>

</dd> <dt>

<span data-ttu-id="754ac-110">*中國* \[在\]</span><span class="sxs-lookup"><span data-stu-id="754ac-110">*prc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="754ac-111">類型： \**Const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \** _</span><span class="sxs-lookup"><span data-stu-id="754ac-111">Type: \**const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect)\** _</span></span>

<span data-ttu-id="754ac-112">要複製的矩形。</span><span class="sxs-lookup"><span data-stu-id="754ac-112">The rectangle to copy.</span></span> <span data-ttu-id="754ac-113">Null 值會指定整個點陣圖。</span><span class="sxs-lookup"><span data-stu-id="754ac-113">A NULL value specifies the entire bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="754ac-114">_cbStride \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="754ac-114">_cbStride\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="754ac-115">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="754ac-115">Type: **UINT**</span></span>

<span data-ttu-id="754ac-116">點陣圖的 stride</span><span class="sxs-lookup"><span data-stu-id="754ac-116">The stride of the bitmap</span></span>

</dd> <dt>

<span data-ttu-id="754ac-117">*cbBufferSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="754ac-117">*cbBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="754ac-118">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="754ac-118">Type: **UINT**</span></span>

<span data-ttu-id="754ac-119">緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="754ac-119">The size of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="754ac-120">*pbBuffer* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="754ac-120">*pbBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="754ac-121">類型： \**BYTE \** _</span><span class="sxs-lookup"><span data-stu-id="754ac-121">Type: \**BYTE\** _</span></span>

<span data-ttu-id="754ac-122">緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="754ac-122">A pointer to the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="754ac-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="754ac-123">Return value</span></span>

<span data-ttu-id="754ac-124">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="754ac-124">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="754ac-125">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="754ac-125">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="754ac-126">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="754ac-126">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="754ac-127">備註</span><span class="sxs-lookup"><span data-stu-id="754ac-127">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="754ac-128">需求</span><span class="sxs-lookup"><span data-stu-id="754ac-128">Requirements</span></span>



| <span data-ttu-id="754ac-129">需求</span><span class="sxs-lookup"><span data-stu-id="754ac-129">Requirement</span></span> | <span data-ttu-id="754ac-130">值</span><span class="sxs-lookup"><span data-stu-id="754ac-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="754ac-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="754ac-131">Minimum supported client</span></span><br/> | <span data-ttu-id="754ac-132">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="754ac-132">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="754ac-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="754ac-133">Minimum supported server</span></span><br/> | <span data-ttu-id="754ac-134">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="754ac-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="754ac-135">DLL</span><span class="sxs-lookup"><span data-stu-id="754ac-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="754ac-136"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="754ac-136"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




