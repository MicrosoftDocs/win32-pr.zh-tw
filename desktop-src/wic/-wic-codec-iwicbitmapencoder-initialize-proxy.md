---
description: Initialize 方法的 Proxy 函式。
ms.assetid: 0db79eb4-dcb2-491a-9bea-a0dec418f80f
title: IWICBitmapEncoder_Initialize_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c1a2e684059b75e41c1d89e2d3dd5379cc208b56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975425"
---
# <a name="iwicbitmapencoder_initialize_proxy-function"></a><span data-ttu-id="c8d87-103">IWICBitmapEncoder \_ Initialize \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="c8d87-103">IWICBitmapEncoder\_Initialize\_Proxy function</span></span>

<span data-ttu-id="c8d87-104">[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="c8d87-104">Proxy function for the [**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8d87-105">語法</span><span class="sxs-lookup"><span data-stu-id="c8d87-105">Syntax</span></span>


```C++
HRESULT IWICBitmapEncoder_Initialize_Proxy(
  _In_ IWICBitmapEncoder           *THIS_PTR,
  _In_ IStream                     *pIStream,
  _In_ WICBitmapEncoderCacheOption cacheOption
);
```



## <a name="parameters"></a><span data-ttu-id="c8d87-106">參數</span><span class="sxs-lookup"><span data-stu-id="c8d87-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8d87-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="c8d87-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8d87-108">類型： \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) \** _</span><span class="sxs-lookup"><span data-stu-id="c8d87-108">Type: \**[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\** _</span></span>

<span data-ttu-id="c8d87-109">這個 [_ *IWICBitmapEncoder* \*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="c8d87-109">Pointer to this [_ *IWICBitmapEncoder*\*](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="c8d87-110">*pIStream* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c8d87-110">*pIStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8d87-111">類型： \**[IStream](/windows/desktop/api/objidl/nn-objidl-istream) \** _</span><span class="sxs-lookup"><span data-stu-id="c8d87-111">Type: \**[IStream](/windows/desktop/api/objidl/nn-objidl-istream)\** _</span></span>

<span data-ttu-id="c8d87-112">輸出資料流。</span><span class="sxs-lookup"><span data-stu-id="c8d87-112">The output stream.</span></span>

</dd> <dt>

<span data-ttu-id="c8d87-113">_cacheOption \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8d87-113">_cacheOption\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8d87-114">類型： **[ **WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption)**</span><span class="sxs-lookup"><span data-stu-id="c8d87-114">Type: **[**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption)**</span></span>

<span data-ttu-id="c8d87-115">初始化時使用的 [**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) 。</span><span class="sxs-lookup"><span data-stu-id="c8d87-115">The [**WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) used on initialization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8d87-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="c8d87-116">Return value</span></span>

<span data-ttu-id="c8d87-117">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c8d87-117">Type: **HRESULT**</span></span>

<span data-ttu-id="c8d87-118">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="c8d87-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c8d87-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c8d87-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8d87-120">備註</span><span class="sxs-lookup"><span data-stu-id="c8d87-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="c8d87-121">需求</span><span class="sxs-lookup"><span data-stu-id="c8d87-121">Requirements</span></span>



| <span data-ttu-id="c8d87-122">需求</span><span class="sxs-lookup"><span data-stu-id="c8d87-122">Requirement</span></span> | <span data-ttu-id="c8d87-123">值</span><span class="sxs-lookup"><span data-stu-id="c8d87-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8d87-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c8d87-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c8d87-125">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8d87-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="c8d87-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c8d87-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c8d87-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8d87-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="c8d87-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c8d87-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8d87-129"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8d87-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

