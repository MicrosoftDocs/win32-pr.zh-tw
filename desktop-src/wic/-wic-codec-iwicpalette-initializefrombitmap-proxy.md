---
description: InitializeFromBitmap 方法的 Proxy 函式。
ms.assetid: 9559a56d-7201-4b39-a3cd-9c0e4eac611a
title: IWICPalette_InitializeFromBitmap_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_InitializeFromBitmap_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: cf5e119acf1efca948281a02f61d8954f4e08818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980709"
---
# <a name="iwicpalette_initializefrombitmap_proxy-function"></a><span data-ttu-id="b5874-103">IWICPalette \_ InitializeFromBitmap \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="b5874-103">IWICPalette\_InitializeFromBitmap\_Proxy function</span></span>

<span data-ttu-id="b5874-104">[**InitializeFromBitmap**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializefrombitmap)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="b5874-104">Proxy function for the [**InitializeFromBitmap**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializefrombitmap) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5874-105">語法</span><span class="sxs-lookup"><span data-stu-id="b5874-105">Syntax</span></span>


```C++
HRESULT IWICPalette_InitializeFromBitmap_Proxy(
  _In_ IWICPalette      *THIS_PTR,
  _In_ IWICBitmapSource *pISurface,
  _In_ UINT             colorCount,
  _In_ BOOL             fAddTransparentColor
);
```



## <a name="parameters"></a><span data-ttu-id="b5874-106">參數</span><span class="sxs-lookup"><span data-stu-id="b5874-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5874-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="b5874-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5874-108">類型： \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="b5874-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="b5874-109">這個 [_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="b5874-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="b5874-110">*pISurface* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b5874-110">*pISurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5874-111">類型： \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="b5874-111">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="b5874-112">來源點陣圖的指標。</span><span class="sxs-lookup"><span data-stu-id="b5874-112">Pointer to the source bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="b5874-113">_colorCount \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5874-113">_colorCount\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5874-114">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="b5874-114">Type: **UINT**</span></span>

<span data-ttu-id="b5874-115">用來初始化調色板的色彩數目。</span><span class="sxs-lookup"><span data-stu-id="b5874-115">The number of colors to initialize the palette with.</span></span>

</dd> <dt>

<span data-ttu-id="b5874-116">*fAddTransparentColor* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b5874-116">*fAddTransparentColor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5874-117">類型： **BOOL**</span><span class="sxs-lookup"><span data-stu-id="b5874-117">Type: **BOOL**</span></span>

<span data-ttu-id="b5874-118">值，指出是否要加入透明色彩。</span><span class="sxs-lookup"><span data-stu-id="b5874-118">A value to indicate whether to add a transparent color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5874-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="b5874-119">Return value</span></span>

<span data-ttu-id="b5874-120">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b5874-120">Type: **HRESULT**</span></span>

<span data-ttu-id="b5874-121">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="b5874-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b5874-122">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b5874-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5874-123">備註</span><span class="sxs-lookup"><span data-stu-id="b5874-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="b5874-124">需求</span><span class="sxs-lookup"><span data-stu-id="b5874-124">Requirements</span></span>



| <span data-ttu-id="b5874-125">需求</span><span class="sxs-lookup"><span data-stu-id="b5874-125">Requirement</span></span> | <span data-ttu-id="b5874-126">值</span><span class="sxs-lookup"><span data-stu-id="b5874-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5874-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b5874-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b5874-128">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b5874-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="b5874-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b5874-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b5874-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b5874-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="b5874-131">DLL</span><span class="sxs-lookup"><span data-stu-id="b5874-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5874-132"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5874-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




