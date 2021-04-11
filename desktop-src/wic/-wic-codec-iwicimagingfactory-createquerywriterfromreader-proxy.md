---
description: CreateQueryWriterFromReader 方法的 Proxy 函式。
ms.assetid: 7784c5e9-38e0-43de-83db-4de3361fa20e
title: IWICImagingFactory_CreateQueryWriterFromReader_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateQueryWriterFromReader_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 4fb0d9c2346fe854cf23acee288ee1086828a76e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945078"
---
# <a name="iwicimagingfactory_createquerywriterfromreader_proxy-function"></a><span data-ttu-id="30bdc-103">IWICImagingFactory \_ CreateQueryWriterFromReader \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="30bdc-103">IWICImagingFactory\_CreateQueryWriterFromReader\_Proxy function</span></span>

<span data-ttu-id="30bdc-104">[**CreateQueryWriterFromReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createquerywriterfromreader)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="30bdc-104">Proxy function for the [**CreateQueryWriterFromReader**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createquerywriterfromreader) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="30bdc-105">語法</span><span class="sxs-lookup"><span data-stu-id="30bdc-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateQueryWriterFromReader_Proxy(
  _In_        IWICImagingFactory      *pFactory,
  _In_        IWICMetadataQueryReader *pIQueryReader,
  _In_  const GUID                    *pguidVendor,
  _Out_       IWICMetadataQueryWriter **ppIQueryWriter
);
```



## <a name="parameters"></a><span data-ttu-id="30bdc-106">參數</span><span class="sxs-lookup"><span data-stu-id="30bdc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30bdc-107">*pFactory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="30bdc-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30bdc-108">類型： \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="30bdc-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="30bdc-109">_pIQueryReader \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30bdc-109">_pIQueryReader\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30bdc-110">類型： \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) \** _</span><span class="sxs-lookup"><span data-stu-id="30bdc-110">Type: \**[**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\** _</span></span>

<span data-ttu-id="30bdc-111">中繼資料查詢讀取器，用來建立中繼資料寫入器。</span><span class="sxs-lookup"><span data-stu-id="30bdc-111">The metadata query reader to create the metadata writer from.</span></span>

</dd> <dt>

<span data-ttu-id="30bdc-112">_pguidVendor \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30bdc-112">_pguidVendor\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30bdc-113">類型： \**CONST GUID \** _</span><span class="sxs-lookup"><span data-stu-id="30bdc-113">Type: \**const GUID\** _</span></span>

<span data-ttu-id="30bdc-114">中繼資料查詢寫入器的廠商 GUID。</span><span class="sxs-lookup"><span data-stu-id="30bdc-114">The vendor GUID for the metadata query writer.</span></span>

</dd> <dt>

<span data-ttu-id="30bdc-115">_ppIQueryWriter \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="30bdc-115">_ppIQueryWriter\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="30bdc-116">類型： **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="30bdc-116">Type: **[**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***</span></span>

<span data-ttu-id="30bdc-117">接收新 [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)指標的指標。</span><span class="sxs-lookup"><span data-stu-id="30bdc-117">A pointer that receives a pointer to a new [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30bdc-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="30bdc-118">Return value</span></span>

<span data-ttu-id="30bdc-119">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="30bdc-119">Type: **HRESULT**</span></span>

<span data-ttu-id="30bdc-120">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="30bdc-120">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="30bdc-121">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="30bdc-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="30bdc-122">備註</span><span class="sxs-lookup"><span data-stu-id="30bdc-122">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="30bdc-123">需求</span><span class="sxs-lookup"><span data-stu-id="30bdc-123">Requirements</span></span>



| <span data-ttu-id="30bdc-124">需求</span><span class="sxs-lookup"><span data-stu-id="30bdc-124">Requirement</span></span> | <span data-ttu-id="30bdc-125">值</span><span class="sxs-lookup"><span data-stu-id="30bdc-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30bdc-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="30bdc-126">Minimum supported client</span></span><br/> | <span data-ttu-id="30bdc-127">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="30bdc-127">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="30bdc-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="30bdc-128">Minimum supported server</span></span><br/> | <span data-ttu-id="30bdc-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="30bdc-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="30bdc-130">DLL</span><span class="sxs-lookup"><span data-stu-id="30bdc-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30bdc-131"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="30bdc-131"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




