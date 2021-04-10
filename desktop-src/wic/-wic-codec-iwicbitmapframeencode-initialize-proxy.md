---
description: Initialize 方法的 Proxy 函式。
ms.assetid: af9e204c-7072-47b8-84eb-47a754968d5b
title: IWICBitmapFrameEncode_Initialize_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: da9192409636de96dbd9d35d9614df2c926c9032
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690287"
---
# <a name="iwicbitmapframeencode_initialize_proxy-function"></a><span data-ttu-id="bb937-103">IWICBitmapFrameEncode \_ Initialize \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="bb937-103">IWICBitmapFrameEncode\_Initialize\_Proxy function</span></span>

<span data-ttu-id="bb937-104">[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="bb937-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb937-105">語法</span><span class="sxs-lookup"><span data-stu-id="bb937-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_Initialize_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ IPropertyBag2         *pIEncoderOptions
);
```



## <a name="parameters"></a><span data-ttu-id="bb937-106">參數</span><span class="sxs-lookup"><span data-stu-id="bb937-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb937-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="bb937-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb937-108">類型： \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="bb937-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="bb937-109">這個 [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="bb937-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="bb937-110">*pIEncoderOptions* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bb937-110">*pIEncoderOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb937-111">類型： \**[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) \** _</span><span class="sxs-lookup"><span data-stu-id="bb937-111">Type: \**[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))\** _</span></span>

<span data-ttu-id="bb937-112">要用於 [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)初始化的屬性集。</span><span class="sxs-lookup"><span data-stu-id="bb937-112">The set of properties to use for [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) initialization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb937-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="bb937-113">Return value</span></span>

<span data-ttu-id="bb937-114">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bb937-114">Type: **HRESULT**</span></span>

<span data-ttu-id="bb937-115">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="bb937-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bb937-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="bb937-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb937-117">備註</span><span class="sxs-lookup"><span data-stu-id="bb937-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="bb937-118">需求</span><span class="sxs-lookup"><span data-stu-id="bb937-118">Requirements</span></span>



| <span data-ttu-id="bb937-119">需求</span><span class="sxs-lookup"><span data-stu-id="bb937-119">Requirement</span></span> | <span data-ttu-id="bb937-120">值</span><span class="sxs-lookup"><span data-stu-id="bb937-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb937-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bb937-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bb937-122">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bb937-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="bb937-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bb937-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bb937-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bb937-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="bb937-125">DLL</span><span class="sxs-lookup"><span data-stu-id="bb937-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb937-126"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb937-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

