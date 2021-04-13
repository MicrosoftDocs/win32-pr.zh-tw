---
description: CreateComponentInfo 方法的 Proxy 函式。
ms.assetid: 7d3b791a-d65e-4b90-8050-373a949e6d9c
title: IWICImagingFactory_CreateComponentInfo_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateComponentInfo_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 208b8b09b402e01f59a925f3dc6de6694b196db2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320120"
---
# <a name="iwicimagingfactory_createcomponentinfo_proxy-function"></a><span data-ttu-id="02bac-103">IWICImagingFactory \_ CreateComponentInfo \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="02bac-103">IWICImagingFactory\_CreateComponentInfo\_Proxy function</span></span>

<span data-ttu-id="02bac-104">[**CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="02bac-104">Proxy function for the [**CreateComponentInfo**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentinfo) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="02bac-105">語法</span><span class="sxs-lookup"><span data-stu-id="02bac-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateComponentInfo_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _In_  REFCLSID           clsidComponent,
  _Out_ IWICComponentInfo  **ppIInfo
);
```



## <a name="parameters"></a><span data-ttu-id="02bac-106">參數</span><span class="sxs-lookup"><span data-stu-id="02bac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02bac-107">*pFactory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="02bac-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02bac-108">類型： \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="02bac-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="02bac-109">_clsidComponent \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="02bac-109">_clsidComponent\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02bac-110">類型： **REFCLSID**</span><span class="sxs-lookup"><span data-stu-id="02bac-110">Type: **REFCLSID**</span></span>

<span data-ttu-id="02bac-111">所需元件的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="02bac-111">The CLSID for the desired component.</span></span>

</dd> <dt>

<span data-ttu-id="02bac-112">*ppIInfo* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="02bac-112">*ppIInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02bac-113">類型： **[ **IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\*\***</span><span class="sxs-lookup"><span data-stu-id="02bac-113">Type: **[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\*\***</span></span>

<span data-ttu-id="02bac-114">接收新 [**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)指標的指標。</span><span class="sxs-lookup"><span data-stu-id="02bac-114">A pointer that receives a pointer to a new [**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02bac-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="02bac-115">Return value</span></span>

<span data-ttu-id="02bac-116">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="02bac-116">Type: **HRESULT**</span></span>

<span data-ttu-id="02bac-117">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="02bac-117">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="02bac-118">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="02bac-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="02bac-119">備註</span><span class="sxs-lookup"><span data-stu-id="02bac-119">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="02bac-120">需求</span><span class="sxs-lookup"><span data-stu-id="02bac-120">Requirements</span></span>



| <span data-ttu-id="02bac-121">需求</span><span class="sxs-lookup"><span data-stu-id="02bac-121">Requirement</span></span> | <span data-ttu-id="02bac-122">值</span><span class="sxs-lookup"><span data-stu-id="02bac-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02bac-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="02bac-123">Minimum supported client</span></span><br/> | <span data-ttu-id="02bac-124">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02bac-124">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="02bac-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="02bac-125">Minimum supported server</span></span><br/> | <span data-ttu-id="02bac-126">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02bac-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="02bac-127">DLL</span><span class="sxs-lookup"><span data-stu-id="02bac-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02bac-128"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="02bac-128"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




