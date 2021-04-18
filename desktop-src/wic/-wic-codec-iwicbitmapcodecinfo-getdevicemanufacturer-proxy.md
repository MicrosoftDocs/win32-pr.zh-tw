---
description: GetDeviceManufacturer 方法的 Proxy 函式。
ms.assetid: f4dbf67a-eb67-4138-a77a-7386567b95e6
title: IWICBitmapCodecInfo_GetDeviceManufacturer_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetDeviceManufacturer_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 3dc10df32325fd0ffc5bb24d1a4c7927b1adc7e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971201"
---
# <a name="iwicbitmapcodecinfo_getdevicemanufacturer_proxy-function"></a><span data-ttu-id="28c62-103">IWICBitmapCodecInfo \_ GetDeviceManufacturer \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="28c62-103">IWICBitmapCodecInfo\_GetDeviceManufacturer\_Proxy function</span></span>

<span data-ttu-id="28c62-104">[**GetDeviceManufacturer**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getdevicemanufacturer)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="28c62-104">Proxy function for the [**GetDeviceManufacturer**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getdevicemanufacturer) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="28c62-105">語法</span><span class="sxs-lookup"><span data-stu-id="28c62-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_GetDeviceManufacturer_Proxy(
  _In_    IWICBitmapCodecInfo *THIS_PTR,
  _In_    UINT                cchDeviceManufacturer,
  _Inout_ WCHAR               *wzDeviceManufacturer,
  _Inout_ UINT                *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="28c62-106">參數</span><span class="sxs-lookup"><span data-stu-id="28c62-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28c62-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="28c62-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28c62-108">類型： \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="28c62-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="28c62-109">這個 [_ *IWICBitmapCodecInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="28c62-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="28c62-110">*cchDeviceManufacturer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="28c62-110">*cchDeviceManufacturer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28c62-111">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="28c62-111">Type: **UINT**</span></span>

<span data-ttu-id="28c62-112">裝置製造名稱的大小。</span><span class="sxs-lookup"><span data-stu-id="28c62-112">The size of the device manufacture's name.</span></span>

</dd> <dt>

<span data-ttu-id="28c62-113">*wzDeviceManufacturer* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="28c62-113">*wzDeviceManufacturer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="28c62-114">類型： \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="28c62-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="28c62-115">接收裝置製造名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="28c62-115">A pointer that receives the device manufacture's name.</span></span>

</dd> <dt>

<span data-ttu-id="28c62-116">_pcchActual \* \[ in、out\]</span><span class="sxs-lookup"><span data-stu-id="28c62-116">_pcchActual\* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="28c62-117">類型： \**UINT \** _</span><span class="sxs-lookup"><span data-stu-id="28c62-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="28c62-118">擷取裝置製造名稱所需的實際緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="28c62-118">The actual buffer size needed to retrieve the device manufacture's name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28c62-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="28c62-119">Return value</span></span>

<span data-ttu-id="28c62-120">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="28c62-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="28c62-121">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="28c62-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="28c62-122">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="28c62-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="28c62-123">備註</span><span class="sxs-lookup"><span data-stu-id="28c62-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="28c62-124">需求</span><span class="sxs-lookup"><span data-stu-id="28c62-124">Requirements</span></span>



| <span data-ttu-id="28c62-125">需求</span><span class="sxs-lookup"><span data-stu-id="28c62-125">Requirement</span></span> | <span data-ttu-id="28c62-126">值</span><span class="sxs-lookup"><span data-stu-id="28c62-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28c62-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="28c62-127">Minimum supported client</span></span><br/> | <span data-ttu-id="28c62-128">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="28c62-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="28c62-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="28c62-129">Minimum supported server</span></span><br/> | <span data-ttu-id="28c62-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="28c62-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="28c62-131">DLL</span><span class="sxs-lookup"><span data-stu-id="28c62-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28c62-132"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="28c62-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




