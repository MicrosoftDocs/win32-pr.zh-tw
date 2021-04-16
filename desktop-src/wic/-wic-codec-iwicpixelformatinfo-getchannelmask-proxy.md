---
description: GetChannelMask 方法的 Proxy 函式。
ms.assetid: c96e6078-4648-4333-8a25-bcb03a2cd50b
title: IWICPixelFormatInfo_GetChannelMask_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPixelFormatInfo_GetChannelMask_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0db2c14e89aba2b13cb95209b81f6d0da5d9d949
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194783"
---
# <a name="iwicpixelformatinfo_getchannelmask_proxy-function"></a><span data-ttu-id="33575-103">IWICPixelFormatInfo \_ GetChannelMask \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="33575-103">IWICPixelFormatInfo\_GetChannelMask\_Proxy function</span></span>

<span data-ttu-id="33575-104">[**GetChannelMask**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getchannelmask)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="33575-104">Proxy function for the [**GetChannelMask**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getchannelmask) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="33575-105">語法</span><span class="sxs-lookup"><span data-stu-id="33575-105">Syntax</span></span>


```C++
HRESULT IWICPixelFormatInfo_GetChannelMask_Proxy(
  _In_    IWICPixelFormatInfo *THIS_PTR,
  _In_    UINT                uiChannelIndex,
  _In_    UINT                cbMaskBuffer,
  _Inout_ BYTE                *pbMaskBuffer,
  _Out_   UINT                *pcbActual
);
```



## <a name="parameters"></a><span data-ttu-id="33575-106">參數</span><span class="sxs-lookup"><span data-stu-id="33575-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33575-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="33575-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33575-108">類型： \**[**IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="33575-108">Type: \**[**IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo)\** _</span></span>

<span data-ttu-id="33575-109">這個 [_ *IWICPixelFormatInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="33575-109">Pointer to this [_ *IWICPixelFormatInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="33575-110">*uiChannelIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="33575-110">*uiChannelIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33575-111">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="33575-111">Type: **UINT**</span></span>

<span data-ttu-id="33575-112">要取出之通道遮罩的索引。</span><span class="sxs-lookup"><span data-stu-id="33575-112">The index to the channel mask to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="33575-113">*cbMaskBuffer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="33575-113">*cbMaskBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33575-114">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="33575-114">Type: **UINT**</span></span>

<span data-ttu-id="33575-115">*PbMaskBuffer* 緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="33575-115">The size of the *pbMaskBuffer* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="33575-116">*pbMaskBuffer* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="33575-116">*pbMaskBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="33575-117">類型： \**BYTE \** _</span><span class="sxs-lookup"><span data-stu-id="33575-117">Type: \**BYTE\** _</span></span>

<span data-ttu-id="33575-118">遮罩緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="33575-118">Pointer to the mask buffer.</span></span>

</dd> <dt>

<span data-ttu-id="33575-119">_pcbActual \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="33575-119">_pcbActual\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="33575-120">類型： \**UINT \** _</span><span class="sxs-lookup"><span data-stu-id="33575-120">Type: \**UINT\** _</span></span>

<span data-ttu-id="33575-121">取得通道遮罩所需的實際緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="33575-121">The actual buffer size needed to obtain the channel mask.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33575-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="33575-122">Return value</span></span>

<span data-ttu-id="33575-123">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="33575-123">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="33575-124">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="33575-124">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="33575-125">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="33575-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="33575-126">備註</span><span class="sxs-lookup"><span data-stu-id="33575-126">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="33575-127">需求</span><span class="sxs-lookup"><span data-stu-id="33575-127">Requirements</span></span>



| <span data-ttu-id="33575-128">需求</span><span class="sxs-lookup"><span data-stu-id="33575-128">Requirement</span></span> | <span data-ttu-id="33575-129">值</span><span class="sxs-lookup"><span data-stu-id="33575-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33575-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="33575-130">Minimum supported client</span></span><br/> | <span data-ttu-id="33575-131">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="33575-131">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="33575-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="33575-132">Minimum supported server</span></span><br/> | <span data-ttu-id="33575-133">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="33575-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="33575-134">DLL</span><span class="sxs-lookup"><span data-stu-id="33575-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33575-135"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="33575-135"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




