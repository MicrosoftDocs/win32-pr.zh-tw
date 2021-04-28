---
description: GetContainerFormat 方法的 IWICBitmapCodecInfo_GetContainerFormat_Proxy 函數 Proxy 函式。
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
ms.openlocfilehash: 729b4e2fe0f21fd1e96082e53194fd49bbc39ae1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086366"
---
# <a name="iwicbitmapcodecinfo_getcontainerformat_proxy-function"></a><span data-ttu-id="da799-103">IWICBitmapCodecInfo \_ GetContainerFormat \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="da799-103">IWICBitmapCodecInfo\_GetContainerFormat\_Proxy function</span></span>

<span data-ttu-id="da799-104">[**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getcontainerformat)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="da799-104">Proxy function for the [**GetContainerFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getcontainerformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="da799-105">語法</span><span class="sxs-lookup"><span data-stu-id="da799-105">Syntax</span></span>


```C++
HRESULT IWICBitmapCodecInfo_GetContainerFormat_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _Out_ GUID                *pguidContainerFormat
);
```



## <a name="parameters"></a><span data-ttu-id="da799-106">參數</span><span class="sxs-lookup"><span data-stu-id="da799-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da799-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="da799-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da799-108">類型： **[ **IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\***</span><span class="sxs-lookup"><span data-stu-id="da799-108">Type: **[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\***</span></span>

<span data-ttu-id="da799-109">這個 [**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="da799-109">Pointer to this [**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) object.</span></span>

</dd> <dt>

<span data-ttu-id="da799-110">*pguidContainerFormat* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="da799-110">*pguidContainerFormat* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="da799-111">類型： **GUID \***</span><span class="sxs-lookup"><span data-stu-id="da799-111">Type: **GUID\***</span></span>

<span data-ttu-id="da799-112">接收容器 GUID 的指標。</span><span class="sxs-lookup"><span data-stu-id="da799-112">A pointer that receives the container GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da799-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="da799-113">Return value</span></span>

<span data-ttu-id="da799-114">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="da799-114">Type: **HRESULT**</span></span>

<span data-ttu-id="da799-115">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="da799-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="da799-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="da799-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="da799-117">備註</span><span class="sxs-lookup"><span data-stu-id="da799-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="da799-118">需求</span><span class="sxs-lookup"><span data-stu-id="da799-118">Requirements</span></span>



| <span data-ttu-id="da799-119">需求</span><span class="sxs-lookup"><span data-stu-id="da799-119">Requirement</span></span> | <span data-ttu-id="da799-120">值</span><span class="sxs-lookup"><span data-stu-id="da799-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da799-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="da799-121">Minimum supported client</span></span><br/> | <span data-ttu-id="da799-122">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="da799-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="da799-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="da799-123">Minimum supported server</span></span><br/> | <span data-ttu-id="da799-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="da799-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="da799-125">DLL</span><span class="sxs-lookup"><span data-stu-id="da799-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da799-126"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="da799-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




