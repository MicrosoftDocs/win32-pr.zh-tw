---
description: GetResolution 方法的 Proxy 函式。
ms.assetid: 5e261c2b-534a-4875-a84f-7251d54f15c6
title: IWICBitmapSource_GetResolution_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_GetResolution_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0bcd63c01bf99e426cdbf5044223a40308fb5e9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193138"
---
# <a name="iwicbitmapsource_getresolution_proxy-function"></a><span data-ttu-id="6c8ae-103">IWICBitmapSource \_ GetResolution \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="6c8ae-103">IWICBitmapSource\_GetResolution\_Proxy function</span></span>

<span data-ttu-id="6c8ae-104">[**GetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="6c8ae-104">Proxy function for the [**GetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c8ae-105">語法</span><span class="sxs-lookup"><span data-stu-id="6c8ae-105">Syntax</span></span>


```C++
HRESULT IWICBitmapSource_GetResolution_Proxy(
  _In_  IWICBitmapSource *THIS_PTR,
  _Out_ double           *pDpiX,
  _Out_ double           *pDpiY
);
```



## <a name="parameters"></a><span data-ttu-id="6c8ae-106">參數</span><span class="sxs-lookup"><span data-stu-id="6c8ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c8ae-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="6c8ae-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c8ae-108">類型： \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="6c8ae-108">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="6c8ae-109">這個 [_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="6c8ae-109">Pointer to this [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span>

</dd> <dt>

<span data-ttu-id="6c8ae-110">*pDpiX* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6c8ae-110">*pDpiX* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c8ae-111">類型： \**double \** _</span><span class="sxs-lookup"><span data-stu-id="6c8ae-111">Type: \**double\** _</span></span>

<span data-ttu-id="6c8ae-112">接收 X 軸 DPI 解析度的指標。</span><span class="sxs-lookup"><span data-stu-id="6c8ae-112">A pointer that receives the x-axis dpi resolution.</span></span>

</dd> <dt>

<span data-ttu-id="6c8ae-113">_pDpiY \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6c8ae-113">_pDpiY\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c8ae-114">類型： \**double \** _</span><span class="sxs-lookup"><span data-stu-id="6c8ae-114">Type: \**double\** _</span></span>

<span data-ttu-id="6c8ae-115">接收 y 軸 DPI 解析度的指標。</span><span class="sxs-lookup"><span data-stu-id="6c8ae-115">A pointer that receives the y-axis dpi resolution.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c8ae-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="6c8ae-116">Return value</span></span>

<span data-ttu-id="6c8ae-117">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="6c8ae-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="6c8ae-118">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="6c8ae-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6c8ae-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6c8ae-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c8ae-120">備註</span><span class="sxs-lookup"><span data-stu-id="6c8ae-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="6c8ae-121">需求</span><span class="sxs-lookup"><span data-stu-id="6c8ae-121">Requirements</span></span>



| <span data-ttu-id="6c8ae-122">需求</span><span class="sxs-lookup"><span data-stu-id="6c8ae-122">Requirement</span></span> | <span data-ttu-id="6c8ae-123">值</span><span class="sxs-lookup"><span data-stu-id="6c8ae-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c8ae-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c8ae-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6c8ae-125">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c8ae-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="6c8ae-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c8ae-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6c8ae-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c8ae-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="6c8ae-128">DLL</span><span class="sxs-lookup"><span data-stu-id="6c8ae-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c8ae-129"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c8ae-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




