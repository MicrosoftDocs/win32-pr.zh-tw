---
description: HasAlpha 方法的 Proxy 函式。
ms.assetid: 8af9f588-ac22-40c4-8973-9636951cc9e6
title: IWICPalette_HasAlpha_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_HasAlpha_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 6f9398b2d570efb41048d88ddeeeb76d62f4ca37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944669"
---
# <a name="iwicpalette_hasalpha_proxy-function"></a><span data-ttu-id="632cc-103">IWICPalette \_ HasAlpha \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="632cc-103">IWICPalette\_HasAlpha\_Proxy function</span></span>

<span data-ttu-id="632cc-104">[**HasAlpha**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-hasalpha)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="632cc-104">Proxy function for the [**HasAlpha**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-hasalpha) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="632cc-105">語法</span><span class="sxs-lookup"><span data-stu-id="632cc-105">Syntax</span></span>


```C++
HRESULT IWICPalette_HasAlpha_Proxy(
  _In_  IWICPalette *THIS_PTR,
  _Out_ BOOL        *pfHasAlpha
);
```



## <a name="parameters"></a><span data-ttu-id="632cc-106">參數</span><span class="sxs-lookup"><span data-stu-id="632cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="632cc-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="632cc-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="632cc-108">類型： \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="632cc-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="632cc-109">這個 [_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="632cc-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="632cc-110">*pfHasAlpha* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="632cc-110">*pfHasAlpha* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="632cc-111">類型： \**BOOL \** _</span><span class="sxs-lookup"><span data-stu-id="632cc-111">Type: \**BOOL\** _</span></span>

<span data-ttu-id="632cc-112">`TRUE`如果調色板包含透明色彩，則為收到的指標; 否則為 `FALSE` 。</span><span class="sxs-lookup"><span data-stu-id="632cc-112">Pointer that receives `TRUE` if the palette contains a transparent color; otherwise, `FALSE`.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="632cc-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="632cc-113">Return value</span></span>

<span data-ttu-id="632cc-114">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="632cc-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="632cc-115">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="632cc-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="632cc-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="632cc-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="632cc-117">備註</span><span class="sxs-lookup"><span data-stu-id="632cc-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="632cc-118">需求</span><span class="sxs-lookup"><span data-stu-id="632cc-118">Requirements</span></span>



| <span data-ttu-id="632cc-119">需求</span><span class="sxs-lookup"><span data-stu-id="632cc-119">Requirement</span></span> | <span data-ttu-id="632cc-120">值</span><span class="sxs-lookup"><span data-stu-id="632cc-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="632cc-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="632cc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="632cc-122">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="632cc-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="632cc-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="632cc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="632cc-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="632cc-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="632cc-125">DLL</span><span class="sxs-lookup"><span data-stu-id="632cc-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="632cc-126"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="632cc-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




