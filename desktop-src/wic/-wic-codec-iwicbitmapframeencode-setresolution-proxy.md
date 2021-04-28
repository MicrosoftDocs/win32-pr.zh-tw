---
description: SetResolution 方法的 IWICBitmapFrameEncode_SetResolution_Proxy 函數 Proxy 函式。
ms.assetid: dc8df5bb-c38b-4be3-a4c6-60e7d5e1cd1b
title: IWICBitmapFrameEncode_SetResolution_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_SetResolution_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 632d6e797d499c4c5468505a4cee49e088ab025a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116606"
---
# <a name="iwicbitmapframeencode_setresolution_proxy-function"></a><span data-ttu-id="74c6f-103">IWICBitmapFrameEncode \_ SetResolution \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="74c6f-103">IWICBitmapFrameEncode\_SetResolution\_Proxy function</span></span>

<span data-ttu-id="74c6f-104">[**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="74c6f-104">Proxy function for the [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="74c6f-105">語法</span><span class="sxs-lookup"><span data-stu-id="74c6f-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_SetResolution_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ double                dpiX,
  _In_ double                dpiY
);
```



## <a name="parameters"></a><span data-ttu-id="74c6f-106">參數</span><span class="sxs-lookup"><span data-stu-id="74c6f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74c6f-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="74c6f-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74c6f-108">類型： **[ **IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span><span class="sxs-lookup"><span data-stu-id="74c6f-108">Type: **[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***</span></span>

<span data-ttu-id="74c6f-109">這個 [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="74c6f-109">Pointer to this [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="74c6f-110">*DPIX* \[在\]</span><span class="sxs-lookup"><span data-stu-id="74c6f-110">*dpiX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74c6f-111">類型： **double**</span><span class="sxs-lookup"><span data-stu-id="74c6f-111">Type: **double**</span></span>

<span data-ttu-id="74c6f-112">水準解析度值。</span><span class="sxs-lookup"><span data-stu-id="74c6f-112">The horizontal resolution value.</span></span>

</dd> <dt>

<span data-ttu-id="74c6f-113">*DPIY* \[在\]</span><span class="sxs-lookup"><span data-stu-id="74c6f-113">*dpiY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74c6f-114">類型： **double**</span><span class="sxs-lookup"><span data-stu-id="74c6f-114">Type: **double**</span></span>

<span data-ttu-id="74c6f-115">垂直解析度值。</span><span class="sxs-lookup"><span data-stu-id="74c6f-115">The vertical resolution value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74c6f-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="74c6f-116">Return value</span></span>

<span data-ttu-id="74c6f-117">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="74c6f-117">Type: **HRESULT**</span></span>

<span data-ttu-id="74c6f-118">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="74c6f-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="74c6f-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="74c6f-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="74c6f-120">備註</span><span class="sxs-lookup"><span data-stu-id="74c6f-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="74c6f-121">需求</span><span class="sxs-lookup"><span data-stu-id="74c6f-121">Requirements</span></span>



| <span data-ttu-id="74c6f-122">需求</span><span class="sxs-lookup"><span data-stu-id="74c6f-122">Requirement</span></span> | <span data-ttu-id="74c6f-123">值</span><span class="sxs-lookup"><span data-stu-id="74c6f-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74c6f-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="74c6f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="74c6f-125">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="74c6f-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="74c6f-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="74c6f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="74c6f-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="74c6f-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="74c6f-128">DLL</span><span class="sxs-lookup"><span data-stu-id="74c6f-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74c6f-129"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="74c6f-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




