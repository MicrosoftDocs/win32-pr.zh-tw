---
description: SetPalette 方法的 Proxy 函式。
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
ms.openlocfilehash: d683dda81d52818bfc7d878d044af9b4e09869b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511288"
---
# <a name="iwicbitmap_setpalette_proxy-function"></a><span data-ttu-id="09737-103">IWICBitmap \_ SetPalette \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="09737-103">IWICBitmap\_SetPalette\_Proxy function</span></span>

<span data-ttu-id="09737-104">[**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setpalette)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="09737-104">Proxy function for the [**SetPalette**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setpalette) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="09737-105">語法</span><span class="sxs-lookup"><span data-stu-id="09737-105">Syntax</span></span>


```C++
HRESULT IWICBitmap_SetPalette_Proxy(
  _In_ IWICBitmap  *THIS_PTR,
  _In_ IWICPalette *pIPalette
);
```



## <a name="parameters"></a><span data-ttu-id="09737-106">參數</span><span class="sxs-lookup"><span data-stu-id="09737-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09737-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="09737-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09737-108">類型： \**[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) \** _</span><span class="sxs-lookup"><span data-stu-id="09737-108">Type: \**[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\** _</span></span>

<span data-ttu-id="09737-109">這個 [_ *IWICBitmap* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="09737-109">Pointer to this [_ *IWICBitmap*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) object.</span></span>

</dd> <dt>

<span data-ttu-id="09737-110">*pIPalette* \[在\]</span><span class="sxs-lookup"><span data-stu-id="09737-110">*pIPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09737-111">類型： \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _</span><span class="sxs-lookup"><span data-stu-id="09737-111">Type: \**[**IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\** _</span></span>

<span data-ttu-id="09737-112">用於轉換的調色板。</span><span class="sxs-lookup"><span data-stu-id="09737-112">The palette to use for conversion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09737-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="09737-113">Return value</span></span>

<span data-ttu-id="09737-114">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="09737-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="09737-115">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="09737-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="09737-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="09737-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="09737-117">備註</span><span class="sxs-lookup"><span data-stu-id="09737-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="09737-118">需求</span><span class="sxs-lookup"><span data-stu-id="09737-118">Requirements</span></span>



| <span data-ttu-id="09737-119">需求</span><span class="sxs-lookup"><span data-stu-id="09737-119">Requirement</span></span> | <span data-ttu-id="09737-120">值</span><span class="sxs-lookup"><span data-stu-id="09737-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09737-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="09737-121">Minimum supported client</span></span><br/> | <span data-ttu-id="09737-122">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="09737-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="09737-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="09737-123">Minimum supported server</span></span><br/> | <span data-ttu-id="09737-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="09737-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="09737-125">DLL</span><span class="sxs-lookup"><span data-stu-id="09737-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09737-126"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="09737-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




