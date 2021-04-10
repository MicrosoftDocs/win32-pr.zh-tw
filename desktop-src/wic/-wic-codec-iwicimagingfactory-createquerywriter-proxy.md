---
description: CreateQueryWriter 方法的 Proxy 函式。
ms.assetid: 7f925117-6244-4be6-bcef-fa852672ac64
title: IWICImagingFactory_CreateQueryWriter_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateQueryWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 4ae0d41b9ceb652f23084c026b130bf711c44f7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694683"
---
# <a name="iwicimagingfactory_createquerywriter_proxy-function"></a><span data-ttu-id="f170f-103">IWICImagingFactory \_ CreateQueryWriter \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="f170f-103">IWICImagingFactory\_CreateQueryWriter\_Proxy function</span></span>

<span data-ttu-id="f170f-104">[**CreateQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createquerywriter)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="f170f-104">Proxy function for the [**CreateQueryWriter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createquerywriter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f170f-105">語法</span><span class="sxs-lookup"><span data-stu-id="f170f-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateQueryWriter_Proxy(
  _In_        IWICImagingFactory      *pFactory,
  _In_        REFGUID                 guidMetadataFormat,
  _In_  const GUID                    *pguidVendor,
  _Out_       IWICMetadataQueryWriter **ppIQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="f170f-106">參數</span><span class="sxs-lookup"><span data-stu-id="f170f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f170f-107">*pFactory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f170f-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f170f-108">類型： \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="f170f-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="f170f-109">_guidMetadataFormat \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f170f-109">_guidMetadataFormat\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f170f-110">類型： **REFGUID**</span><span class="sxs-lookup"><span data-stu-id="f170f-110">Type: **REFGUID**</span></span>

<span data-ttu-id="f170f-111">所需元資料格式的 GUID。</span><span class="sxs-lookup"><span data-stu-id="f170f-111">The GUID for the desired metadata format.</span></span>

</dd> <dt>

<span data-ttu-id="f170f-112">*pguidVendor* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f170f-112">*pguidVendor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f170f-113">類型： \**CONST GUID \** _</span><span class="sxs-lookup"><span data-stu-id="f170f-113">Type: \**const GUID\** _</span></span>

<span data-ttu-id="f170f-114">中繼資料寫入器的廠商 GUID。</span><span class="sxs-lookup"><span data-stu-id="f170f-114">The vendor GUID of the metadata writer.</span></span>

</dd> <dt>

<span data-ttu-id="f170f-115">_ppIQueryWriter \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f170f-115">_ppIQueryWriter\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f170f-116">類型： **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="f170f-116">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="f170f-117">接收新 [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)指標的指標。</span><span class="sxs-lookup"><span data-stu-id="f170f-117">A pointer that receives a pointer to a new [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f170f-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="f170f-118">Return value</span></span>

<span data-ttu-id="f170f-119">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f170f-119">Type: **HRESULT**</span></span>

<span data-ttu-id="f170f-120">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="f170f-120">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f170f-121">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f170f-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f170f-122">備註</span><span class="sxs-lookup"><span data-stu-id="f170f-122">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="f170f-123">需求</span><span class="sxs-lookup"><span data-stu-id="f170f-123">Requirements</span></span>



| <span data-ttu-id="f170f-124">需求</span><span class="sxs-lookup"><span data-stu-id="f170f-124">Requirement</span></span> | <span data-ttu-id="f170f-125">值</span><span class="sxs-lookup"><span data-stu-id="f170f-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f170f-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f170f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f170f-127">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f170f-127">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="f170f-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f170f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f170f-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f170f-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="f170f-130">DLL</span><span class="sxs-lookup"><span data-stu-id="f170f-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f170f-131"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f170f-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




