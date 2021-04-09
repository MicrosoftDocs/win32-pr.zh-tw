---
description: DoesSupportLossless 方法的 Proxy 函式。
ms.assetid: c88d7971-cc93-458c-a31e-19a8b8350d09
title: IWICBitmapCodecInfo_DoesSupportLossless_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_DoesSupportLossless_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 6f498af72391aa0a7745ed79d06c6e1d55317393
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690300"
---
# <a name="iwicbitmapcodecinfo_doessupportlossless_proxy-function"></a><span data-ttu-id="442ef-103">IWICBitmapCodecInfo \_ DoesSupportLossless \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="442ef-103">IWICBitmapCodecInfo\_DoesSupportLossless\_Proxy function</span></span>

<span data-ttu-id="442ef-104">[**DoesSupportLossless**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportlossless)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="442ef-104">Proxy function for the [**DoesSupportLossless**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportlossless) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="442ef-105">語法</span><span class="sxs-lookup"><span data-stu-id="442ef-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_DoesSupportLossless_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _Out_ BOOL                *pfSupportLossless
);
```



## <a name="parameters"></a><span data-ttu-id="442ef-106">參數</span><span class="sxs-lookup"><span data-stu-id="442ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="442ef-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="442ef-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="442ef-108">類型： \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="442ef-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="442ef-109">這個 [_ *IWICBitmapCodecInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="442ef-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="442ef-110">*pfSupportLossless* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="442ef-110">*pfSupportLossless* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="442ef-111">類型： \**BOOL \** _</span><span class="sxs-lookup"><span data-stu-id="442ef-111">Type: \**BOOL\** _</span></span>

<span data-ttu-id="442ef-112">如果編解碼器支援不失真格式，則為收到 _ *TRUE*\* 的指標;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="442ef-112">A pointer that receives _ *TRUE*\* if the codec supports lossless formats; otherwise, **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="442ef-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="442ef-113">Return value</span></span>

<span data-ttu-id="442ef-114">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="442ef-114">Type: **HRESULT**</span></span>

<span data-ttu-id="442ef-115">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="442ef-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="442ef-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="442ef-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="442ef-117">備註</span><span class="sxs-lookup"><span data-stu-id="442ef-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="442ef-118">需求</span><span class="sxs-lookup"><span data-stu-id="442ef-118">Requirements</span></span>



| <span data-ttu-id="442ef-119">需求</span><span class="sxs-lookup"><span data-stu-id="442ef-119">Requirement</span></span> | <span data-ttu-id="442ef-120">值</span><span class="sxs-lookup"><span data-stu-id="442ef-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="442ef-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="442ef-121">Minimum supported client</span></span><br/> | <span data-ttu-id="442ef-122">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="442ef-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="442ef-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="442ef-123">Minimum supported server</span></span><br/> | <span data-ttu-id="442ef-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="442ef-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="442ef-125">DLL</span><span class="sxs-lookup"><span data-stu-id="442ef-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="442ef-126"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="442ef-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




