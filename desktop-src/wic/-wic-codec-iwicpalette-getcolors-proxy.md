---
description: GetColors 方法的 Proxy 函式。
ms.assetid: 31590de3-f35c-4253-9a80-2f59c795bf3f
title: IWICPalette_GetColors_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_GetColors_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e39e8825b78175fabb5a37e331236e7bf0d9ed73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193715"
---
# <a name="iwicpalette_getcolors_proxy-function"></a><span data-ttu-id="dce1c-103">IWICPalette \_ GetColors \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="dce1c-103">IWICPalette\_GetColors\_Proxy function</span></span>

<span data-ttu-id="dce1c-104">[**GetColors**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-getcolors)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="dce1c-104">Proxy function for the [**GetColors**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-getcolors) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dce1c-105">語法</span><span class="sxs-lookup"><span data-stu-id="dce1c-105">Syntax</span></span>


```C++
HRESULT IWICPalette_GetColors_Proxy(
  _In_  IWICPalette *THIS_PTR,
  _In_  UINT        colorCount,
  _Out_ WICColor    *pColors,
  _Out_ UINT        *pcActualColors
);
```



## <a name="parameters"></a><span data-ttu-id="dce1c-106">參數</span><span class="sxs-lookup"><span data-stu-id="dce1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dce1c-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="dce1c-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dce1c-108">類型： \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="dce1c-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="dce1c-109">這個 [_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="dce1c-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="dce1c-110">*colorCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dce1c-110">*colorCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dce1c-111">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="dce1c-111">Type: **UINT**</span></span>

<span data-ttu-id="dce1c-112">*PColors* 陣列的大小。</span><span class="sxs-lookup"><span data-stu-id="dce1c-112">The size of the *pColors* array.</span></span>

</dd> <dt>

<span data-ttu-id="dce1c-113">*pColors* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="dce1c-113">*pColors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dce1c-114">類型： \**WICColor \** _</span><span class="sxs-lookup"><span data-stu-id="dce1c-114">Type: \**WICColor\** _</span></span>

<span data-ttu-id="dce1c-115">接收調色板色彩的指標。</span><span class="sxs-lookup"><span data-stu-id="dce1c-115">Pointer that receives the colors of the palette.</span></span>

</dd> <dt>

<span data-ttu-id="dce1c-116">_pcActualColors \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dce1c-116">_pcActualColors\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dce1c-117">類型： \**UINT \** _</span><span class="sxs-lookup"><span data-stu-id="dce1c-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="dce1c-118">取得調色板色彩所需的實際大小。</span><span class="sxs-lookup"><span data-stu-id="dce1c-118">The actual size needed to obtain the palette colors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dce1c-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="dce1c-119">Return value</span></span>

<span data-ttu-id="dce1c-120">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="dce1c-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="dce1c-121">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="dce1c-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dce1c-122">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="dce1c-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="dce1c-123">備註</span><span class="sxs-lookup"><span data-stu-id="dce1c-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="dce1c-124">需求</span><span class="sxs-lookup"><span data-stu-id="dce1c-124">Requirements</span></span>



| <span data-ttu-id="dce1c-125">需求</span><span class="sxs-lookup"><span data-stu-id="dce1c-125">Requirement</span></span> | <span data-ttu-id="dce1c-126">值</span><span class="sxs-lookup"><span data-stu-id="dce1c-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dce1c-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dce1c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="dce1c-128">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dce1c-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="dce1c-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dce1c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="dce1c-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dce1c-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="dce1c-131">DLL</span><span class="sxs-lookup"><span data-stu-id="dce1c-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dce1c-132"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="dce1c-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




