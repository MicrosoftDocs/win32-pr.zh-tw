---
description: CreateBitmapFromHICON 方法的 Proxy 函式。
ms.assetid: 5df3d9d9-1b23-4f38-b97e-0b77d6db99d8
title: IWICImagingFactory_CreateBitmapFromHICON_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromHICON_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 58f9f37dc27c76a9eaa55d6baec52efbb773343e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978322"
---
# <a name="iwicimagingfactory_createbitmapfromhicon_proxy-function"></a><span data-ttu-id="14fc0-103">IWICImagingFactory \_ CreateBitmapFromHICON \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="14fc0-103">IWICImagingFactory\_CreateBitmapFromHICON\_Proxy function</span></span>

<span data-ttu-id="14fc0-104">[**CreateBitmapFromHICON**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromhicon)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="14fc0-104">Proxy function for the [**CreateBitmapFromHICON**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromhicon) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="14fc0-105">語法</span><span class="sxs-lookup"><span data-stu-id="14fc0-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateBitmapFromHICON_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _In_  HICON              hIcon,
  _Out_ IWICBitmap         **ppIBitmap
);
```



## <a name="parameters"></a><span data-ttu-id="14fc0-106">參數</span><span class="sxs-lookup"><span data-stu-id="14fc0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14fc0-107">*pFactory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="14fc0-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14fc0-108">類型： \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="14fc0-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="14fc0-109">_hIcon \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="14fc0-109">_hIcon\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14fc0-110">類型： **HICON**</span><span class="sxs-lookup"><span data-stu-id="14fc0-110">Type: **HICON**</span></span>

<span data-ttu-id="14fc0-111">用來建立新點陣圖的圖示控制碼。</span><span class="sxs-lookup"><span data-stu-id="14fc0-111">The icon handle to create the new bitmap from.</span></span>

</dd> <dt>

<span data-ttu-id="14fc0-112">*ppIBitmap* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="14fc0-112">*ppIBitmap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14fc0-113">類型： **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span><span class="sxs-lookup"><span data-stu-id="14fc0-113">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***</span></span>

<span data-ttu-id="14fc0-114">接收新點陣圖指標的指標。</span><span class="sxs-lookup"><span data-stu-id="14fc0-114">A pointer that receives a pointer to the new bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14fc0-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="14fc0-115">Return value</span></span>

<span data-ttu-id="14fc0-116">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="14fc0-116">Type: **HRESULT**</span></span>

<span data-ttu-id="14fc0-117">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="14fc0-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="14fc0-118">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="14fc0-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="14fc0-119">備註</span><span class="sxs-lookup"><span data-stu-id="14fc0-119">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="14fc0-120">需求</span><span class="sxs-lookup"><span data-stu-id="14fc0-120">Requirements</span></span>



| <span data-ttu-id="14fc0-121">需求</span><span class="sxs-lookup"><span data-stu-id="14fc0-121">Requirement</span></span> | <span data-ttu-id="14fc0-122">值</span><span class="sxs-lookup"><span data-stu-id="14fc0-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14fc0-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="14fc0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="14fc0-124">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="14fc0-124">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="14fc0-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="14fc0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="14fc0-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="14fc0-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="14fc0-127">DLL</span><span class="sxs-lookup"><span data-stu-id="14fc0-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14fc0-128"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="14fc0-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




