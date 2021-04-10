---
description: CreateFormatConverter 方法的 Proxy 函式。
ms.assetid: 1013720a-d00e-4381-af5d-747806546692
title: IWICImagingFactory_CreateFormatConverter_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateFormatConverter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 91e0d87a57326e413e725e056bd5f44aff152934
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194408"
---
# <a name="iwicimagingfactory_createformatconverter_proxy-function"></a><span data-ttu-id="696c8-103">IWICImagingFactory \_ CreateFormatConverter \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="696c8-103">IWICImagingFactory\_CreateFormatConverter\_Proxy function</span></span>

<span data-ttu-id="696c8-104">[**CreateFormatConverter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createformatconverter)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="696c8-104">Proxy function for the [**CreateFormatConverter**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="696c8-105">語法</span><span class="sxs-lookup"><span data-stu-id="696c8-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateFormatConverter_Proxy(
  _In_  IWICImagingFactory  *pFactory,
  _Out_ IWICFormatConverter **ppIFormatConverter
);
```



## <a name="parameters"></a><span data-ttu-id="696c8-106">參數</span><span class="sxs-lookup"><span data-stu-id="696c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="696c8-107">*pFactory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="696c8-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="696c8-108">類型： \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="696c8-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="696c8-109">_ppIFormatConverter \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="696c8-109">_ppIFormatConverter\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="696c8-110">類型： **[ **IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)\*\***</span><span class="sxs-lookup"><span data-stu-id="696c8-110">Type: **[**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)\*\***</span></span>

<span data-ttu-id="696c8-111">接收新 [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)指標的指標。</span><span class="sxs-lookup"><span data-stu-id="696c8-111">A pointer that receives a pointer to a new [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="696c8-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="696c8-112">Return value</span></span>

<span data-ttu-id="696c8-113">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="696c8-113">Type: **HRESULT**</span></span>

<span data-ttu-id="696c8-114">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="696c8-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="696c8-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="696c8-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="696c8-116">備註</span><span class="sxs-lookup"><span data-stu-id="696c8-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="696c8-117">需求</span><span class="sxs-lookup"><span data-stu-id="696c8-117">Requirements</span></span>



| <span data-ttu-id="696c8-118">需求</span><span class="sxs-lookup"><span data-stu-id="696c8-118">Requirement</span></span> | <span data-ttu-id="696c8-119">值</span><span class="sxs-lookup"><span data-stu-id="696c8-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="696c8-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="696c8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="696c8-121">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="696c8-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="696c8-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="696c8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="696c8-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="696c8-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="696c8-124">DLL</span><span class="sxs-lookup"><span data-stu-id="696c8-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="696c8-125"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="696c8-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




