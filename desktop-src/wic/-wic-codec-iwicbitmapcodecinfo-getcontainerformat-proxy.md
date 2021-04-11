---
description: GetContainerFormat 方法的 Proxy 函式。
ms.assetid: d8a2387a-fb75-4812-b046-51359071281d
title: IWICBitmapCodecInfo_GetContainerFormat_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetContainerFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 896c2ff88085c0300cffcc56c2877b98cd4ab68a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191292"
---
# <a name="iwicbitmapcodecinfo_getcontainerformat_proxy-function"></a><span data-ttu-id="d8983-103">IWICBitmapCodecInfo \_ GetContainerFormat \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="d8983-103">IWICBitmapCodecInfo\_GetContainerFormat\_Proxy function</span></span>

<span data-ttu-id="d8983-104">[**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getcontainerformat)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="d8983-104">Proxy function for the [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getcontainerformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8983-105">語法</span><span class="sxs-lookup"><span data-stu-id="d8983-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_GetContainerFormat_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _Out_ GUID                *pguidContainerFormat
);
```



## <a name="parameters"></a><span data-ttu-id="d8983-106">參數</span><span class="sxs-lookup"><span data-stu-id="d8983-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8983-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="d8983-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8983-108">類型： \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="d8983-108">Type: \**[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\** _</span></span>

<span data-ttu-id="d8983-109">這個 [_ *IWICBitmapCodecInfo* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="d8983-109">Pointer to this [_ *IWICBitmapCodecInfo*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="d8983-110">*pguidContainerFormat* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d8983-110">*pguidContainerFormat* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8983-111">類型： \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="d8983-111">Type: \**GUID\** _</span></span>

<span data-ttu-id="d8983-112">接收容器 GUID 的指標。</span><span class="sxs-lookup"><span data-stu-id="d8983-112">A pointer that receives the container GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8983-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d8983-113">Return value</span></span>

<span data-ttu-id="d8983-114">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="d8983-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="d8983-115">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="d8983-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d8983-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d8983-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8983-117">備註</span><span class="sxs-lookup"><span data-stu-id="d8983-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="d8983-118">需求</span><span class="sxs-lookup"><span data-stu-id="d8983-118">Requirements</span></span>



| <span data-ttu-id="d8983-119">需求</span><span class="sxs-lookup"><span data-stu-id="d8983-119">Requirement</span></span> | <span data-ttu-id="d8983-120">值</span><span class="sxs-lookup"><span data-stu-id="d8983-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8983-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d8983-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d8983-122">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d8983-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="d8983-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d8983-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d8983-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d8983-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="d8983-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d8983-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8983-126"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8983-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




