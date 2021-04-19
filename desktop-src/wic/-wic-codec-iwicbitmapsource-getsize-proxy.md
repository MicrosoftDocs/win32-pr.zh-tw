---
description: GetSize 方法的 Proxy 函式。
ms.assetid: a9b7d01c-78d9-47b8-a373-a7c49f7bccfd
title: IWICBitmapSource_GetSize_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_GetSize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 978748125b7c7f643027077182b9136b577cb00c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981615"
---
# <a name="iwicbitmapsource_getsize_proxy-function"></a><span data-ttu-id="f7da5-103">IWICBitmapSource \_ GetSize \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="f7da5-103">IWICBitmapSource\_GetSize\_Proxy function</span></span>

<span data-ttu-id="f7da5-104">[**GetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="f7da5-104">Proxy function for the [**GetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7da5-105">語法</span><span class="sxs-lookup"><span data-stu-id="f7da5-105">Syntax</span></span>


```C++
HRESULT IWICBitmapSource_GetSize_Proxy(
  _In_  IWICBitmapSource *THIS_PTR,
  _Out_ UINT             *puiWidth,
  _Out_ UINT             *puiHeight
);
```



## <a name="parameters"></a><span data-ttu-id="f7da5-106">參數</span><span class="sxs-lookup"><span data-stu-id="f7da5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7da5-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="f7da5-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7da5-108">類型： \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _</span><span class="sxs-lookup"><span data-stu-id="f7da5-108">Type: \**[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\** _</span></span>

<span data-ttu-id="f7da5-109">這個 [_ *IWICBitmapSource* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="f7da5-109">Pointer to this [_ *IWICBitmapSource*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) object.</span></span>

</dd> <dt>

<span data-ttu-id="f7da5-110">*puiWidth* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f7da5-110">*puiWidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f7da5-111">類型： \**UINT \** _</span><span class="sxs-lookup"><span data-stu-id="f7da5-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="f7da5-112">接收點陣圖圖元寬度的指標。</span><span class="sxs-lookup"><span data-stu-id="f7da5-112">A pointer that receives the pixel width of the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="f7da5-113">_puiHeight \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f7da5-113">_puiHeight\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f7da5-114">類型： \**UINT \** _</span><span class="sxs-lookup"><span data-stu-id="f7da5-114">Type: \**UINT\** _</span></span>

<span data-ttu-id="f7da5-115">接收點陣圖圖元高度的指標</span><span class="sxs-lookup"><span data-stu-id="f7da5-115">A pointer that receives the pixel height of the bitmap</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7da5-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="f7da5-116">Return value</span></span>

<span data-ttu-id="f7da5-117">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="f7da5-117">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="f7da5-118">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="f7da5-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f7da5-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f7da5-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7da5-120">備註</span><span class="sxs-lookup"><span data-stu-id="f7da5-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="f7da5-121">需求</span><span class="sxs-lookup"><span data-stu-id="f7da5-121">Requirements</span></span>



| <span data-ttu-id="f7da5-122">需求</span><span class="sxs-lookup"><span data-stu-id="f7da5-122">Requirement</span></span> | <span data-ttu-id="f7da5-123">值</span><span class="sxs-lookup"><span data-stu-id="f7da5-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7da5-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f7da5-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f7da5-125">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f7da5-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="f7da5-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f7da5-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f7da5-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f7da5-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="f7da5-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f7da5-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7da5-129"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f7da5-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




