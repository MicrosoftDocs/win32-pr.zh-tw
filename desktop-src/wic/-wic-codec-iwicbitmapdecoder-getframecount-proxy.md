---
description: GetFrameCount 方法的 Proxy 函式。
ms.assetid: 2103af73-60a2-4c1c-8db2-7dfd474440eb
title: IWICBitmapDecoder_GetFrameCount_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetFrameCount_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 784f362d711f22f5bfe1728f41309cdd7c22e788
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690296"
---
# <a name="iwicbitmapdecoder_getframecount_proxy-function"></a><span data-ttu-id="57e7b-103">IWICBitmapDecoder \_ GetFrameCount \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="57e7b-103">IWICBitmapDecoder\_GetFrameCount\_Proxy function</span></span>

<span data-ttu-id="57e7b-104">[**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="57e7b-104">Proxy function for the [**GetFrameCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="57e7b-105">語法</span><span class="sxs-lookup"><span data-stu-id="57e7b-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetFrameCount_Proxy(
  _In_  IWICBitmapDecoder *THIS_PTR,
  _Out_ UINT              *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="57e7b-106">參數</span><span class="sxs-lookup"><span data-stu-id="57e7b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57e7b-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="57e7b-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57e7b-108">類型： \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="57e7b-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="57e7b-109">這個 [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="57e7b-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="57e7b-110">*pCount* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="57e7b-110">*pCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57e7b-111">類型： \**UINT \** _</span><span class="sxs-lookup"><span data-stu-id="57e7b-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="57e7b-112">指標，接收影像中的總畫面數。</span><span class="sxs-lookup"><span data-stu-id="57e7b-112">A pointer that receives the total number of frames in the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57e7b-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="57e7b-113">Return value</span></span>

<span data-ttu-id="57e7b-114">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="57e7b-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="57e7b-115">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="57e7b-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="57e7b-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="57e7b-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="57e7b-117">備註</span><span class="sxs-lookup"><span data-stu-id="57e7b-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="57e7b-118">需求</span><span class="sxs-lookup"><span data-stu-id="57e7b-118">Requirements</span></span>



| <span data-ttu-id="57e7b-119">需求</span><span class="sxs-lookup"><span data-stu-id="57e7b-119">Requirement</span></span> | <span data-ttu-id="57e7b-120">值</span><span class="sxs-lookup"><span data-stu-id="57e7b-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57e7b-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="57e7b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="57e7b-122">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="57e7b-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="57e7b-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="57e7b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="57e7b-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="57e7b-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="57e7b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="57e7b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57e7b-126"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="57e7b-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




