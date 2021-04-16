---
description: GetMimeTypes 方法的 Proxy 函式。
ms.assetid: 9d05624f-da08-4475-933b-faa12bec9012
title: IWICBitmapCodecInfo_GetMimeTypes_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetMimeTypes_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: eb00b2ae3cd935171a9333a55a76038ef9ae2ed8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511284"
---
# <a name="iwicbitmapcodecinfo_getmimetypes_proxy-function"></a><span data-ttu-id="353e8-103">IWICBitmapCodecInfo \_ GetMimeTypes \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="353e8-103">IWICBitmapCodecInfo\_GetMimeTypes\_Proxy function</span></span>

<span data-ttu-id="353e8-104">[**GetMimeTypes**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getmimetypes)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="353e8-104">Proxy function for the [**GetMimeTypes**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getmimetypes) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="353e8-105">語法</span><span class="sxs-lookup"><span data-stu-id="353e8-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_GetMimeTypes_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _In_  UINT                cchMimeTypes,
  _Out_ WCHAR               *wzMimeTypes,
  _Out_ UINT                *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="353e8-106">參數</span><span class="sxs-lookup"><span data-stu-id="353e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="353e8-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="353e8-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="353e8-108">類型： \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="353e8-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="353e8-109">這個 [_ *IWICBitmapCodecInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="353e8-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="353e8-110">*cchMimeTypes* \[在\]</span><span class="sxs-lookup"><span data-stu-id="353e8-110">*cchMimeTypes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="353e8-111">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="353e8-111">Type: **UINT**</span></span>

<span data-ttu-id="353e8-112">Mime 類型緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="353e8-112">The size of the mime types buffer.</span></span>

</dd> <dt>

<span data-ttu-id="353e8-113">*wzMimeTypes* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="353e8-113">*wzMimeTypes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="353e8-114">類型： \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="353e8-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="353e8-115">接收與編解碼器相關聯之 mime 類型的指標。</span><span class="sxs-lookup"><span data-stu-id="353e8-115">A pointer that receives the mime types associated with the codec.</span></span>

</dd> <dt>

<span data-ttu-id="353e8-116">_pcchActual \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="353e8-116">_pcchActual\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="353e8-117">類型： \**UINT \** _</span><span class="sxs-lookup"><span data-stu-id="353e8-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="353e8-118">取得與編解碼器相關聯的所有 mime 類型所需的實際緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="353e8-118">The actual buffer size needed to retrieve all mime types associated with the codec.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="353e8-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="353e8-119">Return value</span></span>

<span data-ttu-id="353e8-120">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="353e8-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="353e8-121">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="353e8-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="353e8-122">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="353e8-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="353e8-123">備註</span><span class="sxs-lookup"><span data-stu-id="353e8-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="353e8-124">需求</span><span class="sxs-lookup"><span data-stu-id="353e8-124">Requirements</span></span>



| <span data-ttu-id="353e8-125">需求</span><span class="sxs-lookup"><span data-stu-id="353e8-125">Requirement</span></span> | <span data-ttu-id="353e8-126">值</span><span class="sxs-lookup"><span data-stu-id="353e8-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="353e8-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="353e8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="353e8-128">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="353e8-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="353e8-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="353e8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="353e8-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="353e8-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="353e8-131">DLL</span><span class="sxs-lookup"><span data-stu-id="353e8-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="353e8-132"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="353e8-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




