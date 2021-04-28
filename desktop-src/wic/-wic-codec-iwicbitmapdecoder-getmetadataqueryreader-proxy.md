---
description: GetMetadataQueryReader 方法的 IWICBitmapDecoder_GetMetadataQueryReader_Proxy 函數 Proxy 函式。
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
ms.openlocfilehash: ebda8edb5c2007b1dfb39ca9f406855da05c456a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100646"
---
# <a name="iwicbitmapdecoder_getmetadataqueryreader_proxy-function"></a><span data-ttu-id="9e52f-103">IWICBitmapDecoder \_ GetMetadataQueryReader \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="9e52f-103">IWICBitmapDecoder\_GetMetadataQueryReader\_Proxy function</span></span>

<span data-ttu-id="9e52f-104">[**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getmetadataqueryreader)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="9e52f-104">Proxy function for the [**GetMetadataQueryReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getmetadataqueryreader) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e52f-105">語法</span><span class="sxs-lookup"><span data-stu-id="9e52f-105">Syntax</span></span>


```C++
HRESULT IWICBitmapDecoder_GetMetadataQueryReader_Proxy(
  _In_  IWICBitmapDecoder       *THIS_PTR,
  _Out_ IWICMetadataQueryReader **ppIMetadataQueryReader
);
```



## <a name="parameters"></a><span data-ttu-id="9e52f-106">參數</span><span class="sxs-lookup"><span data-stu-id="9e52f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e52f-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="9e52f-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e52f-108">類型： **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***</span><span class="sxs-lookup"><span data-stu-id="9e52f-108">Type: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***</span></span>

<span data-ttu-id="9e52f-109">這個 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="9e52f-109">Pointer to this [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) object.</span></span>

</dd> <dt>

<span data-ttu-id="9e52f-110">*ppIMetadataQueryReader* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9e52f-110">*ppIMetadataQueryReader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9e52f-111">類型： **[ **IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***</span><span class="sxs-lookup"><span data-stu-id="9e52f-111">Type: **[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\*\***</span></span>

<span data-ttu-id="9e52f-112">接收中繼資料指標的指標。</span><span class="sxs-lookup"><span data-stu-id="9e52f-112">A pointer that receives a pointer to the metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e52f-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="9e52f-113">Return value</span></span>

<span data-ttu-id="9e52f-114">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9e52f-114">Type: **HRESULT**</span></span>

<span data-ttu-id="9e52f-115">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="9e52f-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9e52f-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9e52f-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e52f-117">備註</span><span class="sxs-lookup"><span data-stu-id="9e52f-117">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="9e52f-118">需求</span><span class="sxs-lookup"><span data-stu-id="9e52f-118">Requirements</span></span>



| <span data-ttu-id="9e52f-119">需求</span><span class="sxs-lookup"><span data-stu-id="9e52f-119">Requirement</span></span> | <span data-ttu-id="9e52f-120">值</span><span class="sxs-lookup"><span data-stu-id="9e52f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e52f-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9e52f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9e52f-122">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9e52f-122">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="9e52f-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9e52f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9e52f-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9e52f-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="9e52f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9e52f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e52f-126"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e52f-126"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




