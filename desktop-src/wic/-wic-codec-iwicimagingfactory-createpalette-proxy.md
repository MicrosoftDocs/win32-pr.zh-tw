---
description: CreatePalette 方法的 Proxy 函式。
ms.assetid: c83b4239-ce6b-4a4c-ab70-df31dfcdd26c
title: IWICImagingFactory_CreatePalette_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreatePalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 626c05ec5e4e365cf61304c4b33e621967cea5e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106986621"
---
# <a name="iwicimagingfactory_createpalette_proxy-function"></a><span data-ttu-id="d8b7c-103">IWICImagingFactory \_ CreatePalette \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="d8b7c-103">IWICImagingFactory\_CreatePalette\_Proxy function</span></span>

<span data-ttu-id="d8b7c-104">[**CreatePalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createpalette)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-104">Proxy function for the [**CreatePalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createpalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8b7c-105">語法</span><span class="sxs-lookup"><span data-stu-id="d8b7c-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreatePalette_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _Out_ IWICPalette        **ppIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="d8b7c-106">參數</span><span class="sxs-lookup"><span data-stu-id="d8b7c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8b7c-107">*pFactory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d8b7c-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8b7c-108">類型： \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="d8b7c-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="d8b7c-109">_ppIPalette \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d8b7c-109">_ppIPalette\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8b7c-110">類型： **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\*\***</span><span class="sxs-lookup"><span data-stu-id="d8b7c-110">Type: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\*\***</span></span>

<span data-ttu-id="d8b7c-111">接收新 [**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)指標的指標。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-111">A pointer that receives a pointer to a new [**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8b7c-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d8b7c-112">Return value</span></span>

<span data-ttu-id="d8b7c-113">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d8b7c-113">Type: **HRESULT**</span></span>

<span data-ttu-id="d8b7c-114">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d8b7c-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d8b7c-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8b7c-116">備註</span><span class="sxs-lookup"><span data-stu-id="d8b7c-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="d8b7c-117">需求</span><span class="sxs-lookup"><span data-stu-id="d8b7c-117">Requirements</span></span>



| <span data-ttu-id="d8b7c-118">需求</span><span class="sxs-lookup"><span data-stu-id="d8b7c-118">Requirement</span></span> | <span data-ttu-id="d8b7c-119">值</span><span class="sxs-lookup"><span data-stu-id="d8b7c-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8b7c-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d8b7c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d8b7c-121">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d8b7c-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="d8b7c-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d8b7c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d8b7c-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d8b7c-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="d8b7c-124">DLL</span><span class="sxs-lookup"><span data-stu-id="d8b7c-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8b7c-125"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8b7c-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




