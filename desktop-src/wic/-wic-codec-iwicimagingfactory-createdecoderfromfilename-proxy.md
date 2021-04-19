---
description: CreateDecoderFromFilename 方法的 Proxy 函式。
ms.assetid: 12c60899-0fe0-47d0-9026-48c74df328ef
title: IWICImagingFactory_CreateDecoderFromFilename_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateDecoderFromFilename_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 3497d71475198d035a496909e65c47df6c5f8b8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975521"
---
# <a name="iwicimagingfactory_createdecoderfromfilename_proxy-function"></a><span data-ttu-id="80dc5-103">IWICImagingFactory \_ CreateDecoderFromFilename \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="80dc5-103">IWICImagingFactory\_CreateDecoderFromFilename\_Proxy function</span></span>

<span data-ttu-id="80dc5-104">[**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="80dc5-104">Proxy function for the [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="80dc5-105">語法</span><span class="sxs-lookup"><span data-stu-id="80dc5-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateDecoderFromFilename_Proxy(
  _In_        IWICImagingFactory  *pFactory,
  _In_        LPCWSTR             wzFilename,
  _In_  const GUID                *pguidVendor,
  _In_        DWORD               dwDesiredAccess,
  _In_        WICDecodeOptions    metadataOptions,
  _Out_       IWICBitmapDecoder   **ppIDecoder
);
```



## <a name="parameters"></a><span data-ttu-id="80dc5-106">參數</span><span class="sxs-lookup"><span data-stu-id="80dc5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80dc5-107">*pFactory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="80dc5-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80dc5-108">類型： \**IWICImagingFactory \** _</span><span class="sxs-lookup"><span data-stu-id="80dc5-108">Type: \**IWICImagingFactory \** _</span></span>

</dd> <dt>

<span data-ttu-id="80dc5-109">_wzFilename \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80dc5-109">_wzFilename\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80dc5-110">類型： **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="80dc5-110">Type: **LPCWSTR**</span></span>

<span data-ttu-id="80dc5-111">以 null 結束的字串指標，指定要建立或開啟之物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="80dc5-111">A pointer to a null-terminated string that specifies the name of an object to create or open.</span></span>

</dd> <dt>

<span data-ttu-id="80dc5-112">*pguidVendor* \[在\]</span><span class="sxs-lookup"><span data-stu-id="80dc5-112">*pguidVendor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80dc5-113">類型： \**CONST GUID \** _</span><span class="sxs-lookup"><span data-stu-id="80dc5-113">Type: \**const GUID\** _</span></span>

<span data-ttu-id="80dc5-114">適用于此解碼器的廠商 GUID。</span><span class="sxs-lookup"><span data-stu-id="80dc5-114">The vendor GUID for the decoder.</span></span>

</dd> <dt>

<span data-ttu-id="80dc5-115">_dwDesiredAccess \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80dc5-115">_dwDesiredAccess\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80dc5-116">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="80dc5-116">Type: **DWORD**</span></span>

<span data-ttu-id="80dc5-117">物件的存取權，可以是讀取、寫入或兩者。</span><span class="sxs-lookup"><span data-stu-id="80dc5-117">The access to the object, which can be read, write, or both.</span></span>

<span data-ttu-id="80dc5-118">如需詳細資訊，請參閱檔案[安全性和存取權限 \[ 檔 \] ](../fileio/file-security-and-access-rights.md)。</span><span class="sxs-lookup"><span data-stu-id="80dc5-118">For more information, see [File Security and Access Rights \[Files\]](../fileio/file-security-and-access-rights.md).</span></span>

</dd> <dt>

<span data-ttu-id="80dc5-119">*metadataOptions* \[在\]</span><span class="sxs-lookup"><span data-stu-id="80dc5-119">*metadataOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80dc5-120">類型： **[ **WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**</span><span class="sxs-lookup"><span data-stu-id="80dc5-120">Type: **[**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**</span></span>

<span data-ttu-id="80dc5-121">建立解碼器時要使用的 [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) 。</span><span class="sxs-lookup"><span data-stu-id="80dc5-121">The [**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) to use when creating the decoder.</span></span>

</dd> <dt>

<span data-ttu-id="80dc5-122">*ppIDecoder* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="80dc5-122">*ppIDecoder* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80dc5-123">類型： **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***</span><span class="sxs-lookup"><span data-stu-id="80dc5-123">Type: **[**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***</span></span>

<span data-ttu-id="80dc5-124">接收新 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)指標的指標。</span><span class="sxs-lookup"><span data-stu-id="80dc5-124">A pointer that receives a pointer to the new [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80dc5-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="80dc5-125">Return value</span></span>

<span data-ttu-id="80dc5-126">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="80dc5-126">Type: **HRESULT**</span></span>

<span data-ttu-id="80dc5-127">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="80dc5-127">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="80dc5-128">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="80dc5-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="80dc5-129">備註</span><span class="sxs-lookup"><span data-stu-id="80dc5-129">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="80dc5-130">需求</span><span class="sxs-lookup"><span data-stu-id="80dc5-130">Requirements</span></span>



| <span data-ttu-id="80dc5-131">需求</span><span class="sxs-lookup"><span data-stu-id="80dc5-131">Requirement</span></span> | <span data-ttu-id="80dc5-132">值</span><span class="sxs-lookup"><span data-stu-id="80dc5-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80dc5-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="80dc5-133">Minimum supported client</span></span><br/> | <span data-ttu-id="80dc5-134">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="80dc5-134">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="80dc5-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="80dc5-135">Minimum supported server</span></span><br/> | <span data-ttu-id="80dc5-136">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="80dc5-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="80dc5-137">DLL</span><span class="sxs-lookup"><span data-stu-id="80dc5-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80dc5-138"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="80dc5-138"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

