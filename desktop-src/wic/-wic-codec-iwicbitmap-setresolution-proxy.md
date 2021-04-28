---
description: SetResolution 方法的 IWICBitmap_SetResolution_Proxy 函數 Proxy 函式。
ms.assetid: c4e3927c-6f9d-401d-acd7-711674cdbb53
title: IWICBitmap_SetResolution_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmap_SetResolution_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: f11189307ad14dde6ea1e1373583a8ab4b08b9be
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086376"
---
# <a name="iwicbitmap_setresolution_proxy-function"></a><span data-ttu-id="e5eb4-103">IWICBitmap \_ SetResolution \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="e5eb4-103">IWICBitmap\_SetResolution\_Proxy function</span></span>

<span data-ttu-id="e5eb4-104">[**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setresolution)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="e5eb4-104">Proxy function for the [**SetResolution**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setresolution) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5eb4-105">語法</span><span class="sxs-lookup"><span data-stu-id="e5eb4-105">Syntax</span></span>


```C++
HRESULT IWICBitmap_SetResolution_Proxy(
  _In_ IWICBitmap *THIS_PTR,
  _In_ double     dpiX,
  _In_ double     dpiY
);
```



## <a name="parameters"></a><span data-ttu-id="e5eb4-106">參數</span><span class="sxs-lookup"><span data-stu-id="e5eb4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5eb4-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="e5eb4-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5eb4-108">類型： **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\***</span><span class="sxs-lookup"><span data-stu-id="e5eb4-108">Type: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\***</span></span>

<span data-ttu-id="e5eb4-109">這個 [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="e5eb4-109">Pointer to this [**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) object.</span></span>

</dd> <dt>

<span data-ttu-id="e5eb4-110">*DPIX* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e5eb4-110">*dpiX* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5eb4-111">類型： **double**</span><span class="sxs-lookup"><span data-stu-id="e5eb4-111">Type: **double**</span></span>

<span data-ttu-id="e5eb4-112">水準解析度。</span><span class="sxs-lookup"><span data-stu-id="e5eb4-112">The horizontal resolution.</span></span>

</dd> <dt>

<span data-ttu-id="e5eb4-113">*DPIY* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e5eb4-113">*dpiY* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5eb4-114">類型： **double**</span><span class="sxs-lookup"><span data-stu-id="e5eb4-114">Type: **double**</span></span>

<span data-ttu-id="e5eb4-115">垂直解析度。</span><span class="sxs-lookup"><span data-stu-id="e5eb4-115">The vertical resolution.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5eb4-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="e5eb4-116">Return value</span></span>

<span data-ttu-id="e5eb4-117">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e5eb4-117">Type: **HRESULT**</span></span>

<span data-ttu-id="e5eb4-118">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="e5eb4-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e5eb4-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e5eb4-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5eb4-120">備註</span><span class="sxs-lookup"><span data-stu-id="e5eb4-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="e5eb4-121">需求</span><span class="sxs-lookup"><span data-stu-id="e5eb4-121">Requirements</span></span>



| <span data-ttu-id="e5eb4-122">需求</span><span class="sxs-lookup"><span data-stu-id="e5eb4-122">Requirement</span></span> | <span data-ttu-id="e5eb4-123">值</span><span class="sxs-lookup"><span data-stu-id="e5eb4-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5eb4-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e5eb4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e5eb4-125">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e5eb4-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="e5eb4-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e5eb4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e5eb4-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e5eb4-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="e5eb4-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e5eb4-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5eb4-129"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5eb4-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




