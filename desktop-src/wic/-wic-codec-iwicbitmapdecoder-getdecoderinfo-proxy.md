---
description: GetDecoderInfo 方法的 Proxy 函式。
ms.assetid: 4117492e-d652-4c72-9979-cc4e554a6fd8
title: IWICBitmapDecoder_GetDecoderInfo_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetDecoderInfo_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 4ca3e234bc6bbff8899b88c89169a59d9838350b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468972"
---
# <a name="iwicbitmapdecoder_getdecoderinfo_proxy-function"></a><span data-ttu-id="d190f-103">IWICBitmapDecoder \_ GetDecoderInfo \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="d190f-103">IWICBitmapDecoder\_GetDecoderInfo\_Proxy function</span></span>

<span data-ttu-id="d190f-104">[**GetDecoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="d190f-104">Proxy function for the [**GetDecoderInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d190f-105">語法</span><span class="sxs-lookup"><span data-stu-id="d190f-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetDecoderInfo_Proxy(
  _In_  IWICBitmapDecoder     *THIS_PTR,
  _Out_ IWICBitmapDecoderInfo **ppIDecoderInfo
);
```



## <a name="parameters"></a><span data-ttu-id="d190f-106">參數</span><span class="sxs-lookup"><span data-stu-id="d190f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d190f-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="d190f-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d190f-108">類型： \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="d190f-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="d190f-109">這個 [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="d190f-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="d190f-110">*ppIDecoderInfo* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d190f-110">*ppIDecoderInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d190f-111">類型： **[ **IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo)\*\***</span><span class="sxs-lookup"><span data-stu-id="d190f-111">Type: **[**IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo)\*\***</span></span>

<span data-ttu-id="d190f-112">接收 [**IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo)指標的指標。</span><span class="sxs-lookup"><span data-stu-id="d190f-112">A pointer that receives a pointer to an [**IWICBitmapDecoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoderinfo).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d190f-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d190f-113">Return value</span></span>

<span data-ttu-id="d190f-114">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d190f-114">Type: **HRESULT**</span></span>

<span data-ttu-id="d190f-115">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="d190f-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d190f-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d190f-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d190f-117">備註</span><span class="sxs-lookup"><span data-stu-id="d190f-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="d190f-118">需求</span><span class="sxs-lookup"><span data-stu-id="d190f-118">Requirements</span></span>



| <span data-ttu-id="d190f-119">需求</span><span class="sxs-lookup"><span data-stu-id="d190f-119">Requirement</span></span> | <span data-ttu-id="d190f-120">值</span><span class="sxs-lookup"><span data-stu-id="d190f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d190f-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d190f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d190f-122">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d190f-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="d190f-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d190f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d190f-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d190f-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="d190f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d190f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d190f-126"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d190f-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




