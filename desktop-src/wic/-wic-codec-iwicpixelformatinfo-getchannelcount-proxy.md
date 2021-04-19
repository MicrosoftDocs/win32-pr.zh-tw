---
description: GetChannelCount 方法的 Proxy 函式。
ms.assetid: f74916d9-d4b5-4b1b-adba-489d46c8d81c
title: IWICPixelFormatInfo_GetChannelCount_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPixelFormatInfo_GetChannelCount_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 6bf3f0d8aaf6cf95633fa4cce771bd7c7e8db85d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971660"
---
# <a name="iwicpixelformatinfo_getchannelcount_proxy-function"></a><span data-ttu-id="2e779-103">IWICPixelFormatInfo \_ GetChannelCount \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="2e779-103">IWICPixelFormatInfo\_GetChannelCount\_Proxy function</span></span>

<span data-ttu-id="2e779-104">[**GetChannelCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getchannelcount)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="2e779-104">Proxy function for the [**GetChannelCount**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpixelformatinfo-getchannelcount) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e779-105">語法</span><span class="sxs-lookup"><span data-stu-id="2e779-105">Syntax</span></span>


```C++
HRESULT IWICPixelFormatInfo_GetChannelCount_Proxy(
  _In_  IWICPixelFormatInfo *THIS_PTR,
  _Out_ UINT                *puiChannelCount
);
```



## <a name="parameters"></a><span data-ttu-id="2e779-106">參數</span><span class="sxs-lookup"><span data-stu-id="2e779-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e779-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="2e779-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e779-108">類型： \**[**IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="2e779-108">Type: \**[**IWICPixelFormatInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo)\** _</span></span>

<span data-ttu-id="2e779-109">這個 [_ *IWICPixelFormatInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="2e779-109">Pointer to this [_ *IWICPixelFormatInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicpixelformatinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="2e779-110">*puiChannelCount* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2e779-110">*puiChannelCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e779-111">類型： \**UINT \** _</span><span class="sxs-lookup"><span data-stu-id="2e779-111">Type: \**UINT\** _</span></span>

<span data-ttu-id="2e779-112">接收通道計數的指標。</span><span class="sxs-lookup"><span data-stu-id="2e779-112">Pointer that receives the channel count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e779-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="2e779-113">Return value</span></span>

<span data-ttu-id="2e779-114">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="2e779-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="2e779-115">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="2e779-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2e779-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2e779-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e779-117">備註</span><span class="sxs-lookup"><span data-stu-id="2e779-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="2e779-118">需求</span><span class="sxs-lookup"><span data-stu-id="2e779-118">Requirements</span></span>



| <span data-ttu-id="2e779-119">需求</span><span class="sxs-lookup"><span data-stu-id="2e779-119">Requirement</span></span> | <span data-ttu-id="2e779-120">值</span><span class="sxs-lookup"><span data-stu-id="2e779-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e779-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2e779-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2e779-122">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2e779-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="2e779-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2e779-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2e779-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2e779-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="2e779-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2e779-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e779-126"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e779-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




