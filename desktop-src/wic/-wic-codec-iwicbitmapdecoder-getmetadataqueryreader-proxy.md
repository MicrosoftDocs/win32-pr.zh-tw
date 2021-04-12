---
description: GetMetadataQueryReader 方法的 Proxy 函式。
ms.assetid: cc32bdf1-d807-46ac-87b7-77bf2d498e72
title: IWICBitmapDecoder_GetMetadataQueryReader_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetMetadataQueryReader_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 72b47652c76934fdf3ea518925990d6d4d1d3eb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318264"
---
# <a name="iwicbitmapdecoder_getmetadataqueryreader_proxy-function"></a><span data-ttu-id="28b3e-103">IWICBitmapDecoder \_ GetMetadataQueryReader \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="28b3e-103">IWICBitmapDecoder\_GetMetadataQueryReader\_Proxy function</span></span>

<span data-ttu-id="28b3e-104">[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getmetadataqueryreader)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="28b3e-104">Proxy function for the [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getmetadataqueryreader) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="28b3e-105">語法</span><span class="sxs-lookup"><span data-stu-id="28b3e-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetMetadataQueryReader_Proxy(
  _In_  IWICBitmapDecoder       *THIS_PTR,
  _Out_ IWICMetadataQueryReader **ppIMetadataQueryReader
);
```



## <a name="parameters"></a><span data-ttu-id="28b3e-106">參數</span><span class="sxs-lookup"><span data-stu-id="28b3e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28b3e-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="28b3e-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28b3e-108">類型： \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) \** _</span><span class="sxs-lookup"><span data-stu-id="28b3e-108">Type: \**[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\** _</span></span>

<span data-ttu-id="28b3e-109">這個 [_ *IWICBitmapDecoder* \*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="28b3e-109">Pointer to this [_ *IWICBitmapDecoder*\*](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="28b3e-110">*ppIMetadataQueryReader* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="28b3e-110">*ppIMetadataQueryReader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28b3e-111">類型： **[ **IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***</span><span class="sxs-lookup"><span data-stu-id="28b3e-111">Type: **[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***</span></span>

<span data-ttu-id="28b3e-112">接收中繼資料指標的指標。</span><span class="sxs-lookup"><span data-stu-id="28b3e-112">A pointer that receives a pointer to the metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28b3e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="28b3e-113">Return value</span></span>

<span data-ttu-id="28b3e-114">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="28b3e-114">Type: **HRESULT**</span></span>

<span data-ttu-id="28b3e-115">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="28b3e-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="28b3e-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="28b3e-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="28b3e-117">備註</span><span class="sxs-lookup"><span data-stu-id="28b3e-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="28b3e-118">需求</span><span class="sxs-lookup"><span data-stu-id="28b3e-118">Requirements</span></span>



| <span data-ttu-id="28b3e-119">需求</span><span class="sxs-lookup"><span data-stu-id="28b3e-119">Requirement</span></span> | <span data-ttu-id="28b3e-120">值</span><span class="sxs-lookup"><span data-stu-id="28b3e-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28b3e-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="28b3e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="28b3e-122">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="28b3e-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="28b3e-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="28b3e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="28b3e-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="28b3e-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="28b3e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="28b3e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28b3e-126"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="28b3e-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




