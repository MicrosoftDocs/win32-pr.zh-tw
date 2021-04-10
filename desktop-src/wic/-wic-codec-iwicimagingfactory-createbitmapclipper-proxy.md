---
description: CreateBitmapClipper 方法的 Proxy 函式。
ms.assetid: 163a8d7b-f22b-4ab5-9dba-00b0cdaab440
title: IWICImagingFactory_CreateBitmapClipper_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapClipper_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: fb722622ce9a8b3ad3144bcf9ea53942c8e611aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944992"
---
# <a name="iwicimagingfactory_createbitmapclipper_proxy-function"></a><span data-ttu-id="09481-103">IWICImagingFactory \_ CreateBitmapClipper \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="09481-103">IWICImagingFactory\_CreateBitmapClipper\_Proxy function</span></span>

<span data-ttu-id="09481-104">[**CreateBitmapClipper**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapclipper)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="09481-104">Proxy function for the [**CreateBitmapClipper**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapclipper) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="09481-105">語法</span><span class="sxs-lookup"><span data-stu-id="09481-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapClipper_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _Out_ IWICBitmapClipper  **ppIBitmapClipper
);
```



## <a name="parameters"></a><span data-ttu-id="09481-106">參數</span><span class="sxs-lookup"><span data-stu-id="09481-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09481-107">*pFactory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="09481-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09481-108">類型： \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="09481-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="09481-109">_ppIBitmapClipper \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="09481-109">_ppIBitmapClipper\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="09481-110">類型： **[ **IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)\*\***</span><span class="sxs-lookup"><span data-stu-id="09481-110">Type: **[**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)\*\***</span></span>

<span data-ttu-id="09481-111">接收新 [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper)指標的指標。</span><span class="sxs-lookup"><span data-stu-id="09481-111">A pointer that receives a pointer to a new [**IWICBitmapClipper**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapclipper).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09481-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="09481-112">Return value</span></span>

<span data-ttu-id="09481-113">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="09481-113">Type: **HRESULT**</span></span>

<span data-ttu-id="09481-114">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="09481-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="09481-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="09481-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="09481-116">備註</span><span class="sxs-lookup"><span data-stu-id="09481-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="09481-117">需求</span><span class="sxs-lookup"><span data-stu-id="09481-117">Requirements</span></span>



| <span data-ttu-id="09481-118">需求</span><span class="sxs-lookup"><span data-stu-id="09481-118">Requirement</span></span> | <span data-ttu-id="09481-119">值</span><span class="sxs-lookup"><span data-stu-id="09481-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09481-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="09481-120">Minimum supported client</span></span><br/> | <span data-ttu-id="09481-121">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="09481-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="09481-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="09481-122">Minimum supported server</span></span><br/> | <span data-ttu-id="09481-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="09481-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="09481-124">DLL</span><span class="sxs-lookup"><span data-stu-id="09481-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09481-125"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="09481-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




