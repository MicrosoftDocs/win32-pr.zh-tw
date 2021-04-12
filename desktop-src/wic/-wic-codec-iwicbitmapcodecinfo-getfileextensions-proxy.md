---
description: GetFileExtensions 方法的 Proxy 函式。
ms.assetid: 1c9232c5-54f3-4186-a1c8-4531e8357d06
title: IWICBitmapCodecInfo_GetFileExtensions_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetFileExtensions_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 7dc44622bb7d576bfe4dc8a70e69779a72c1c07b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318268"
---
# <a name="iwicbitmapcodecinfo_getfileextensions_proxy-function"></a><span data-ttu-id="d38df-103">IWICBitmapCodecInfo \_ GetFileExtensions \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="d38df-103">IWICBitmapCodecInfo\_GetFileExtensions\_Proxy function</span></span>

<span data-ttu-id="d38df-104">[**GetFileExtensions**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getfileextensions)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="d38df-104">Proxy function for the [**GetFileExtensions**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getfileextensions) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d38df-105">語法</span><span class="sxs-lookup"><span data-stu-id="d38df-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_GetFileExtensions_Proxy(
  _In_    IWICBitmapCodecInfo *THIS_PTR,
  _In_    UINT                cchFileExtensions,
  _Inout_ WCHAR               *wzFileExtensions,
  _Inout_ UINT                *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="d38df-106">參數</span><span class="sxs-lookup"><span data-stu-id="d38df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d38df-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="d38df-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d38df-108">類型： \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="d38df-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="d38df-109">這個 [_ *IWICBitmapCodecInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="d38df-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="d38df-110">*cchFileExtensions* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d38df-110">*cchFileExtensions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d38df-111">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="d38df-111">Type: **UINT**</span></span>

<span data-ttu-id="d38df-112">副檔名緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="d38df-112">The size of the file name extension buffer.</span></span>

</dd> <dt>

<span data-ttu-id="d38df-113">*wzFileExtensions* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="d38df-113">*wzFileExtensions* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d38df-114">類型： \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="d38df-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="d38df-115">此指標會接收與編解碼器相關聯的副檔名。</span><span class="sxs-lookup"><span data-stu-id="d38df-115">A pointer that receives the file name extensions associated with the codec.</span></span>

</dd> <dt>

<span data-ttu-id="d38df-116">_pcchActual \* \[ in、out\]</span><span class="sxs-lookup"><span data-stu-id="d38df-116">_pcchActual\* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d38df-117">類型： \**UINT \** _</span><span class="sxs-lookup"><span data-stu-id="d38df-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="d38df-118">取得所有與此編解碼器相關聯的副檔名時，所需的實際緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="d38df-118">The actual buffer size needed to retrieve all file name extensions associated with the codec.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d38df-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="d38df-119">Return value</span></span>

<span data-ttu-id="d38df-120">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="d38df-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="d38df-121">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="d38df-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d38df-122">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d38df-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d38df-123">備註</span><span class="sxs-lookup"><span data-stu-id="d38df-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="d38df-124">需求</span><span class="sxs-lookup"><span data-stu-id="d38df-124">Requirements</span></span>



| <span data-ttu-id="d38df-125">需求</span><span class="sxs-lookup"><span data-stu-id="d38df-125">Requirement</span></span> | <span data-ttu-id="d38df-126">值</span><span class="sxs-lookup"><span data-stu-id="d38df-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d38df-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d38df-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d38df-128">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d38df-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="d38df-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d38df-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d38df-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d38df-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="d38df-131">DLL</span><span class="sxs-lookup"><span data-stu-id="d38df-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d38df-132"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d38df-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




