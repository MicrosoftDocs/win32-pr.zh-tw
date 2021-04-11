---
description: CreateMetadataWriterFromReader 方法的 Proxy 函式。
ms.assetid: da9e80d3-3265-428d-987e-8b344472527a
title: IWICComponentFactory_CreateMetadataWriterFromReader_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentFactory_CreateMetadataWriterFromReader_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 31aea68f0f2d3c475368ad94b600280719261eb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849687"
---
# <a name="iwiccomponentfactory_createmetadatawriterfromreader_proxy-function"></a><span data-ttu-id="f330b-103">IWICComponentFactory \_ CreateMetadataWriterFromReader \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="f330b-103">IWICComponentFactory\_CreateMetadataWriterFromReader\_Proxy function</span></span>

<span data-ttu-id="f330b-104">[**CreateMetadataWriterFromReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatawriterfromreader)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="f330b-104">Proxy function for the [**CreateMetadataWriterFromReader**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatawriterfromreader) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f330b-105">語法</span><span class="sxs-lookup"><span data-stu-id="f330b-105">Syntax</span></span>


```C++
HRESULT IWICComponentFactory_CreateMetadataWriterFromReader_Proxy(
  _In_        IWICComponentFactory *THIS_PTR,
  _In_        IWICMetadataReader   *pIReader,
  _In_  const GUID                 *pguidVendor,
  _Out_       IWICMetadataWriter   **ppIWriter
);
```



## <a name="parameters"></a><span data-ttu-id="f330b-106">參數</span><span class="sxs-lookup"><span data-stu-id="f330b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f330b-107">*這 \_* \[ 中的 PTR\]</span><span class="sxs-lookup"><span data-stu-id="f330b-107">*THIS\_PTR* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f330b-108">類型： \**[**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="f330b-108">Type: \**[**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)\** _</span></span>

<span data-ttu-id="f330b-109">這個 [_ *IWICComponentFactory* \*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)物件的指標。</span><span class="sxs-lookup"><span data-stu-id="f330b-109">Pointer to this [_ *IWICComponentFactory*\*](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) object.</span></span>

</dd> <dt>

<span data-ttu-id="f330b-110">*pIReader* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f330b-110">*pIReader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f330b-111">類型： \**[**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader) \** _</span><span class="sxs-lookup"><span data-stu-id="f330b-111">Type: \**[**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)\** _</span></span>

</dd> <dt>

<span data-ttu-id="f330b-112">_pguidVendor \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f330b-112">_pguidVendor\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f330b-113">類型： \**CONST GUID \** _</span><span class="sxs-lookup"><span data-stu-id="f330b-113">Type: \**const GUID\** _</span></span>

</dd> <dt>

<span data-ttu-id="f330b-114">_ppIWriter \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f330b-114">_ppIWriter\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f330b-115">類型： **[ **IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)\*\***</span><span class="sxs-lookup"><span data-stu-id="f330b-115">Type: **[**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)\*\***</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f330b-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="f330b-116">Return value</span></span>

<span data-ttu-id="f330b-117">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f330b-117">Type: **HRESULT**</span></span>

<span data-ttu-id="f330b-118">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="f330b-118">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f330b-119">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f330b-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f330b-120">備註</span><span class="sxs-lookup"><span data-stu-id="f330b-120">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="f330b-121">需求</span><span class="sxs-lookup"><span data-stu-id="f330b-121">Requirements</span></span>



| <span data-ttu-id="f330b-122">需求</span><span class="sxs-lookup"><span data-stu-id="f330b-122">Requirement</span></span> | <span data-ttu-id="f330b-123">值</span><span class="sxs-lookup"><span data-stu-id="f330b-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f330b-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f330b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f330b-125">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f330b-125">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="f330b-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f330b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f330b-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f330b-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="f330b-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f330b-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f330b-129"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f330b-129"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




