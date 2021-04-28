---
description: SetPalette 方法的 IWICBitmap_SetPalette_Proxy 函數 Proxy 函式。
ms.assetid: 3fd60833-7f21-4654-883a-2dd88c403bc8
title: IWICBitmap_SetPalette_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmap_SetPalette_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: fc8d6181cf9fe9313755fd52d54319f266f4cae6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086406"
---
# <a name="iwicbitmap_setpalette_proxy-function"></a><span data-ttu-id="c32d0-103">IWICBitmap \_ SetPalette \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="c32d0-103">IWICBitmap\_SetPalette\_Proxy function</span></span>

<span data-ttu-id="c32d0-104">[**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setpalette)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="c32d0-104">Proxy function for the [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setpalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c32d0-105">語法</span><span class="sxs-lookup"><span data-stu-id="c32d0-105">Syntax</span></span>


```C++
HRESULT IWICBitmap_SetPalette_Proxy(
  _In_ IWICBitmap  *THIS_PTR,
  _In_ IWICPalette *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="c32d0-106">參數</span><span class="sxs-lookup"><span data-stu-id="c32d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c32d0-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="c32d0-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c32d0-108">類型： **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\***</span><span class="sxs-lookup"><span data-stu-id="c32d0-108">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\***</span></span>

<span data-ttu-id="c32d0-109">這個 [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="c32d0-109">Pointer to this [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) object.</span></span>

</dd> <dt>

<span data-ttu-id="c32d0-110">*pIPalette* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c32d0-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c32d0-111">類型： **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span><span class="sxs-lookup"><span data-stu-id="c32d0-111">Type: **[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***</span></span>

<span data-ttu-id="c32d0-112">用於轉換的調色板。</span><span class="sxs-lookup"><span data-stu-id="c32d0-112">The palette to use for conversion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c32d0-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="c32d0-113">Return value</span></span>

<span data-ttu-id="c32d0-114">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c32d0-114">Type: **HRESULT**</span></span>

<span data-ttu-id="c32d0-115">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="c32d0-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c32d0-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c32d0-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c32d0-117">備註</span><span class="sxs-lookup"><span data-stu-id="c32d0-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="c32d0-118">需求</span><span class="sxs-lookup"><span data-stu-id="c32d0-118">Requirements</span></span>



| <span data-ttu-id="c32d0-119">需求</span><span class="sxs-lookup"><span data-stu-id="c32d0-119">Requirement</span></span> | <span data-ttu-id="c32d0-120">值</span><span class="sxs-lookup"><span data-stu-id="c32d0-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c32d0-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c32d0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c32d0-122">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c32d0-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="c32d0-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c32d0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c32d0-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c32d0-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="c32d0-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c32d0-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c32d0-126"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c32d0-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




