---
description: DoesSupportAnimation 方法的 Proxy 函式。
ms.assetid: dd7ed856-14b5-4215-96da-8f5db19a7796
title: IWICBitmapCodecInfo_DoesSupportAnimation_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_DoesSupportAnimation_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 443a8ec7871af6161de2efbb6d4f21d65e5ae9d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970594"
---
# <a name="iwicbitmapcodecinfo_doessupportanimation_proxy-function"></a><span data-ttu-id="0d945-103">IWICBitmapCodecInfo \_ DoesSupportAnimation \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="0d945-103">IWICBitmapCodecInfo\_DoesSupportAnimation\_Proxy function</span></span>

<span data-ttu-id="0d945-104">[**DoesSupportAnimation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportanimation)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="0d945-104">Proxy function for the [**DoesSupportAnimation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportanimation) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d945-105">語法</span><span class="sxs-lookup"><span data-stu-id="0d945-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_DoesSupportAnimation_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _Out_ BOOL                *pfSupportAnimation
);
```



## <a name="parameters"></a><span data-ttu-id="0d945-106">參數</span><span class="sxs-lookup"><span data-stu-id="0d945-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d945-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="0d945-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d945-108">類型： \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="0d945-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="0d945-109">這個 [_ *IWICBitmapCodecInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="0d945-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="0d945-110">*pfSupportAnimation* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0d945-110">*pfSupportAnimation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d945-111">類型： \**BOOL \** _</span><span class="sxs-lookup"><span data-stu-id="0d945-111">Type: \**BOOL\** _</span></span>

<span data-ttu-id="0d945-112">如果編解碼器支援具有時間資訊的影像，則為接收 _ *TRUE*\* 的指標;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="0d945-112">A pointer that receives _ *TRUE*\* if the codec supports images with timing information; otherwise, **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d945-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="0d945-113">Return value</span></span>

<span data-ttu-id="0d945-114">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0d945-114">Type: **HRESULT**</span></span>

<span data-ttu-id="0d945-115">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="0d945-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0d945-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0d945-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d945-117">備註</span><span class="sxs-lookup"><span data-stu-id="0d945-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="0d945-118">需求</span><span class="sxs-lookup"><span data-stu-id="0d945-118">Requirements</span></span>



| <span data-ttu-id="0d945-119">需求</span><span class="sxs-lookup"><span data-stu-id="0d945-119">Requirement</span></span> | <span data-ttu-id="0d945-120">值</span><span class="sxs-lookup"><span data-stu-id="0d945-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d945-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0d945-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0d945-122">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0d945-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="0d945-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0d945-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0d945-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0d945-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="0d945-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0d945-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d945-126"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d945-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




