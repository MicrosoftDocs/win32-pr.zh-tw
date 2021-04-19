---
description: SetSize 方法的 Proxy 函式。
ms.assetid: 28b4967f-4c8a-475c-8f86-c19e5d424a26
title: IWICBitmapFrameEncode_SetSize_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_SetSize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0a8046ede01cdd30d6a30eb81cbc1617531ef1d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978225"
---
# <a name="iwicbitmapframeencode_setsize_proxy-function"></a><span data-ttu-id="bf28c-103">IWICBitmapFrameEncode \_ SetSize \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="bf28c-103">IWICBitmapFrameEncode\_SetSize\_Proxy function</span></span>

<span data-ttu-id="bf28c-104">[**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="bf28c-104">Proxy function for the [**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf28c-105">語法</span><span class="sxs-lookup"><span data-stu-id="bf28c-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_SetSize_Proxy(
  _In_ IWICBitmapFrameEncode *THIS_PTR,
  _In_ UINT                  uiWidth,
  _In_ UINT                  uiHeight
);
```



## <a name="parameters"></a><span data-ttu-id="bf28c-106">參數</span><span class="sxs-lookup"><span data-stu-id="bf28c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf28c-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="bf28c-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf28c-108">類型： \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="bf28c-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="bf28c-109">這個 [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="bf28c-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="bf28c-110">*uiWidth* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bf28c-110">*uiWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf28c-111">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="bf28c-111">Type: **UINT**</span></span>

<span data-ttu-id="bf28c-112">輸出影像的寬度。</span><span class="sxs-lookup"><span data-stu-id="bf28c-112">The width of the output image.</span></span>

</dd> <dt>

<span data-ttu-id="bf28c-113">*uiHeight* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bf28c-113">*uiHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf28c-114">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="bf28c-114">Type: **UINT**</span></span>

<span data-ttu-id="bf28c-115">輸出影像的高度。</span><span class="sxs-lookup"><span data-stu-id="bf28c-115">The height of the output image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf28c-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="bf28c-116">Return value</span></span>

<span data-ttu-id="bf28c-117">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bf28c-117">Type: **HRESULT**</span></span>

<span data-ttu-id="bf28c-118">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="bf28c-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bf28c-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="bf28c-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf28c-120">備註</span><span class="sxs-lookup"><span data-stu-id="bf28c-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="bf28c-121">需求</span><span class="sxs-lookup"><span data-stu-id="bf28c-121">Requirements</span></span>



| <span data-ttu-id="bf28c-122">需求</span><span class="sxs-lookup"><span data-stu-id="bf28c-122">Requirement</span></span> | <span data-ttu-id="bf28c-123">值</span><span class="sxs-lookup"><span data-stu-id="bf28c-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf28c-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bf28c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bf28c-125">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bf28c-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="bf28c-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bf28c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bf28c-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bf28c-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="bf28c-128">DLL</span><span class="sxs-lookup"><span data-stu-id="bf28c-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf28c-129"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf28c-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




