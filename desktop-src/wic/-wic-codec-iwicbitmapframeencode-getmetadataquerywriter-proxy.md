---
description: GetMetadataQueryWriter 方法的 Proxy 函式。
ms.assetid: b2c61dee-b72b-408c-8cb9-de2587587f1f
title: IWICBitmapFrameEncode_GetMetadataQueryWriter_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapFrameEncode_GetMetadataQueryWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: b6668ffc4261310bfa76424afcae92e14c4ed921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690288"
---
# <a name="iwicbitmapframeencode_getmetadataquerywriter_proxy-function"></a><span data-ttu-id="667c8-103">IWICBitmapFrameEncode \_ GetMetadataQueryWriter \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="667c8-103">IWICBitmapFrameEncode\_GetMetadataQueryWriter\_Proxy function</span></span>

<span data-ttu-id="667c8-104">[**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="667c8-104">Proxy function for the [**GetMetadataQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="667c8-105">語法</span><span class="sxs-lookup"><span data-stu-id="667c8-105">Syntax</span></span>


```C++
HRESULT IWICBitmapFrameEncode_GetMetadataQueryWriter_Proxy(
  _In_  IWICBitmapFrameEncode   *THIS_PTR,
  _Out_ IWICMetadataQueryWriter **ppIMetadataQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="667c8-106">參數</span><span class="sxs-lookup"><span data-stu-id="667c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="667c8-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="667c8-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="667c8-108">類型： \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) \** _</span><span class="sxs-lookup"><span data-stu-id="667c8-108">Type: \**[**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\** _</span></span>

<span data-ttu-id="667c8-109">這個 [_ *IWICBitmapFrameEncode* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="667c8-109">Pointer to this [_ *IWICBitmapFrameEncode*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) object.</span></span>

</dd> <dt>

<span data-ttu-id="667c8-110">*ppIMetadataQueryWriter* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="667c8-110">*ppIMetadataQueryWriter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="667c8-111">類型： **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="667c8-111">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="667c8-112">接收框架之中繼資料查詢寫入器的指標。</span><span class="sxs-lookup"><span data-stu-id="667c8-112">A pointer that receives a metadata query writer for the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="667c8-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="667c8-113">Return value</span></span>

<span data-ttu-id="667c8-114">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="667c8-114">Type: **HRESULT**</span></span>

<span data-ttu-id="667c8-115">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="667c8-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="667c8-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="667c8-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="667c8-117">備註</span><span class="sxs-lookup"><span data-stu-id="667c8-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="667c8-118">需求</span><span class="sxs-lookup"><span data-stu-id="667c8-118">Requirements</span></span>



| <span data-ttu-id="667c8-119">需求</span><span class="sxs-lookup"><span data-stu-id="667c8-119">Requirement</span></span> | <span data-ttu-id="667c8-120">值</span><span class="sxs-lookup"><span data-stu-id="667c8-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="667c8-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="667c8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="667c8-122">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="667c8-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="667c8-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="667c8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="667c8-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="667c8-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="667c8-125">DLL</span><span class="sxs-lookup"><span data-stu-id="667c8-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="667c8-126"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="667c8-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




