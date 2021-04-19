---
description: GetDeviceModels 方法的 Proxy 函式。
ms.assetid: de8f91f7-fef7-48bc-94fc-34c43175248b
title: IWICBitmapCodecInfo_GetDeviceModels_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetDeviceModels_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: b8fa6d6df6984569aa3fe49fc734f7699aa504d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972622"
---
# <a name="iwicbitmapcodecinfo_getdevicemodels_proxy-function"></a><span data-ttu-id="d96ca-103">IWICBitmapCodecInfo \_ GetDeviceModels \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="d96ca-103">IWICBitmapCodecInfo\_GetDeviceModels\_Proxy function</span></span>

<span data-ttu-id="d96ca-104">[**GetDeviceModels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getdevicemodels)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="d96ca-104">Proxy function for the [**GetDeviceModels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getdevicemodels) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d96ca-105">語法</span><span class="sxs-lookup"><span data-stu-id="d96ca-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_GetDeviceModels_Proxy(
  _In_    IWICBitmapCodecInfo *THIS_PTR,
  _In_    UINT                cchDeviceModels,
  _Inout_ WCHAR               *wzDeviceModels,
  _Inout_ UINT                *pcchActual
);
```



## <a name="parameters"></a><span data-ttu-id="d96ca-106">參數</span><span class="sxs-lookup"><span data-stu-id="d96ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d96ca-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="d96ca-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d96ca-108">類型： \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="d96ca-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="d96ca-109">這個 [_ *IWICBitmapCodecInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="d96ca-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="d96ca-110">*cchDeviceModels* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d96ca-110">*cchDeviceModels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d96ca-111">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="d96ca-111">Type: **UINT**</span></span>

<span data-ttu-id="d96ca-112">裝置型號緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="d96ca-112">The size of the device models buffer.</span></span>

</dd> <dt>

<span data-ttu-id="d96ca-113">*wzDeviceModels* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="d96ca-113">*wzDeviceModels* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d96ca-114">類型： \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="d96ca-114">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="d96ca-115">指標，接收與編解碼器相關聯的裝置型號名稱清單（以逗號分隔）。</span><span class="sxs-lookup"><span data-stu-id="d96ca-115">A pointer that receives a comma delimited list of device model names associated with the codec.</span></span>

</dd> <dt>

<span data-ttu-id="d96ca-116">_pcchActual \* \[ in、out\]</span><span class="sxs-lookup"><span data-stu-id="d96ca-116">_pcchActual\* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d96ca-117">類型： \**UINT \** _</span><span class="sxs-lookup"><span data-stu-id="d96ca-117">Type: \**UINT\** _</span></span>

<span data-ttu-id="d96ca-118">取得所有裝置模型名稱所需的實際緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="d96ca-118">The actual buffer size needed to retrieve all of the device model names.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d96ca-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="d96ca-119">Return value</span></span>

<span data-ttu-id="d96ca-120">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="d96ca-120">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="d96ca-121">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="d96ca-121">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d96ca-122">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d96ca-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d96ca-123">備註</span><span class="sxs-lookup"><span data-stu-id="d96ca-123">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="d96ca-124">需求</span><span class="sxs-lookup"><span data-stu-id="d96ca-124">Requirements</span></span>



| <span data-ttu-id="d96ca-125">需求</span><span class="sxs-lookup"><span data-stu-id="d96ca-125">Requirement</span></span> | <span data-ttu-id="d96ca-126">值</span><span class="sxs-lookup"><span data-stu-id="d96ca-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d96ca-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d96ca-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d96ca-128">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d96ca-128">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="d96ca-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d96ca-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d96ca-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d96ca-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="d96ca-131">DLL</span><span class="sxs-lookup"><span data-stu-id="d96ca-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d96ca-132"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d96ca-132"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




