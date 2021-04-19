---
description: CreateNewFrame 方法的 Proxy 函式。
ms.assetid: b23e8689-0fdc-49a7-a004-148b50420127
title: IWICBitmapEncoder_CreateNewFrame_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_CreateNewFrame_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c0ddf0141e5b13e370f199e3f211e74c3a0e6e77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987750"
---
# <a name="iwicbitmapencoder_createnewframe_proxy-function"></a><span data-ttu-id="6c2bf-103">IWICBitmapEncoder \_ CreateNewFrame \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="6c2bf-103">IWICBitmapEncoder\_CreateNewFrame\_Proxy function</span></span>

<span data-ttu-id="6c2bf-104">[**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="6c2bf-104">Proxy function for the [**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c2bf-105">語法</span><span class="sxs-lookup"><span data-stu-id="6c2bf-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_CreateNewFrame_Proxy(
  _In_    IWICBitmapEncoder     *THIS_PTR,
  _Out_   IWICBitmapFrameEncode **ppIFrameEncode,
  _Inout_ IPropertyBag2         **ppIEncoderOptions
);
```



## <a name="parameters"></a><span data-ttu-id="6c2bf-106">參數</span><span class="sxs-lookup"><span data-stu-id="6c2bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c2bf-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="6c2bf-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c2bf-108">類型： \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="6c2bf-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="6c2bf-109">這個 [_ *IWICBitmapEncoder* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="6c2bf-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="6c2bf-110">*ppIFrameEncode* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6c2bf-110">*ppIFrameEncode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c2bf-111">類型： **[ **IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\*\***</span><span class="sxs-lookup"><span data-stu-id="6c2bf-111">Type: **[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\*\***</span></span>

<span data-ttu-id="6c2bf-112">指標，會接收指向新 [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)實例的指標。</span><span class="sxs-lookup"><span data-stu-id="6c2bf-112">A pointer that receives a pointer to the new instance of an [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode).</span></span>

</dd> <dt>

<span data-ttu-id="6c2bf-113">*ppIEncoderOptions* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="6c2bf-113">*ppIEncoderOptions* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c2bf-114">類型： **[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))\*\***</span><span class="sxs-lookup"><span data-stu-id="6c2bf-114">Type: **[IPropertyBag2](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85))\*\***</span></span>

<span data-ttu-id="6c2bf-115">要用於框架初始化的命名屬性。</span><span class="sxs-lookup"><span data-stu-id="6c2bf-115">The named properties to use for frame initialization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c2bf-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="6c2bf-116">Return value</span></span>

<span data-ttu-id="6c2bf-117">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6c2bf-117">Type: **HRESULT**</span></span>

<span data-ttu-id="6c2bf-118">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="6c2bf-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6c2bf-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6c2bf-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c2bf-120">備註</span><span class="sxs-lookup"><span data-stu-id="6c2bf-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="6c2bf-121">需求</span><span class="sxs-lookup"><span data-stu-id="6c2bf-121">Requirements</span></span>



| <span data-ttu-id="6c2bf-122">需求</span><span class="sxs-lookup"><span data-stu-id="6c2bf-122">Requirement</span></span> | <span data-ttu-id="6c2bf-123">值</span><span class="sxs-lookup"><span data-stu-id="6c2bf-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c2bf-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c2bf-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6c2bf-125">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c2bf-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="6c2bf-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c2bf-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6c2bf-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c2bf-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="6c2bf-128">DLL</span><span class="sxs-lookup"><span data-stu-id="6c2bf-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c2bf-129"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c2bf-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

