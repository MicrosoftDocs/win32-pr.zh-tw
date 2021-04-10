---
description: InitializePredefined 方法的 Proxy 函式。
ms.assetid: 78137d43-c32f-4d60-b289-2e2154cf4d1e
title: IWICPalette_InitializePredefined_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_InitializePredefined_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: d65202d9d7800763e15f52ef0eb03b16bc348e78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694540"
---
# <a name="iwicpalette_initializepredefined_proxy-function"></a><span data-ttu-id="8b7c7-103">IWICPalette \_ InitializePredefined \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="8b7c7-103">IWICPalette\_InitializePredefined\_Proxy function</span></span>

<span data-ttu-id="8b7c7-104">[**InitializePredefined**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializepredefined)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="8b7c7-104">Proxy function for the [**InitializePredefined**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializepredefined) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b7c7-105">語法</span><span class="sxs-lookup"><span data-stu-id="8b7c7-105">Syntax</span></span>


```C++
HRESULT IWICPalette_InitializePredefined_Proxy(
  _In_ IWICPalette          *THIS_PTR,
  _In_ WICBitmapPaletteType ePaletteType,
  _In_ BOOL                 fAddTransparentColor
);
```



## <a name="parameters"></a><span data-ttu-id="8b7c7-106">參數</span><span class="sxs-lookup"><span data-stu-id="8b7c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b7c7-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="8b7c7-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b7c7-108">類型： \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="8b7c7-108">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="8b7c7-109">這個 [_ *IWICPalette* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="8b7c7-109">Pointer to this [_ *IWICPalette*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) object.</span></span>

</dd> <dt>

<span data-ttu-id="8b7c7-110">*ePaletteType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8b7c7-110">*ePaletteType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b7c7-111">類型： **[ **WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**</span><span class="sxs-lookup"><span data-stu-id="8b7c7-111">Type: **[**WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**</span></span>

<span data-ttu-id="8b7c7-112">所需的預先定義調色板類型。</span><span class="sxs-lookup"><span data-stu-id="8b7c7-112">The desired pre-defined palette type.</span></span>

</dd> <dt>

<span data-ttu-id="8b7c7-113">*fAddTransparentColor* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8b7c7-113">*fAddTransparentColor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b7c7-114">類型： **BOOL**</span><span class="sxs-lookup"><span data-stu-id="8b7c7-114">Type: **BOOL**</span></span>

<span data-ttu-id="8b7c7-115">要加入至調色板的選擇性透明色彩。</span><span class="sxs-lookup"><span data-stu-id="8b7c7-115">The optional tranparent color to add to the palette.</span></span> <span data-ttu-id="8b7c7-116">如果不需要任何透明色彩，請使用0。</span><span class="sxs-lookup"><span data-stu-id="8b7c7-116">If no transparent color is needed, use 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b7c7-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="8b7c7-117">Return value</span></span>

<span data-ttu-id="8b7c7-118">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8b7c7-118">Type: **HRESULT**</span></span>

<span data-ttu-id="8b7c7-119">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="8b7c7-119">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8b7c7-120">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8b7c7-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b7c7-121">備註</span><span class="sxs-lookup"><span data-stu-id="8b7c7-121">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="8b7c7-122">需求</span><span class="sxs-lookup"><span data-stu-id="8b7c7-122">Requirements</span></span>



| <span data-ttu-id="8b7c7-123">需求</span><span class="sxs-lookup"><span data-stu-id="8b7c7-123">Requirement</span></span> | <span data-ttu-id="8b7c7-124">值</span><span class="sxs-lookup"><span data-stu-id="8b7c7-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b7c7-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8b7c7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8b7c7-126">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8b7c7-126">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="8b7c7-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8b7c7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8b7c7-128">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8b7c7-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="8b7c7-129">DLL</span><span class="sxs-lookup"><span data-stu-id="8b7c7-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b7c7-130"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8b7c7-130"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




