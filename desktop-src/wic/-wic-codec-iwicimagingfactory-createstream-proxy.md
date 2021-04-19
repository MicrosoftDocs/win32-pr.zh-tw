---
description: CreateStream 方法的 Proxy 函式。
ms.assetid: c827e1aa-13ae-459e-a1dc-5ff8c31a54bc
title: IWICImagingFactory_CreateStream_Proxy 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateStream_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 61670dbe3c1689a3d5b8030585a2b13d281efd19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998158"
---
# <a name="iwicimagingfactory_createstream_proxy-function"></a><span data-ttu-id="96846-103">IWICImagingFactory \_ CreateStream \_ Proxy 函式</span><span class="sxs-lookup"><span data-stu-id="96846-103">IWICImagingFactory\_CreateStream\_Proxy function</span></span>

<span data-ttu-id="96846-104">[**CreateStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream)方法的 Proxy 函式。</span><span class="sxs-lookup"><span data-stu-id="96846-104">Proxy function for the [**CreateStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="96846-105">語法</span><span class="sxs-lookup"><span data-stu-id="96846-105">Syntax</span></span>


```C++
HRESULT IWICImagingFactory_CreateStream_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _Out_ IWICStream         **ppIWICStream
);
```



## <a name="parameters"></a><span data-ttu-id="96846-106">參數</span><span class="sxs-lookup"><span data-stu-id="96846-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96846-107">*pFactory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="96846-107">*pFactory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96846-108">類型： \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _</span><span class="sxs-lookup"><span data-stu-id="96846-108">Type: \**[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\** _</span></span>

</dd> <dt>

<span data-ttu-id="96846-109">_ppIWICStream \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="96846-109">_ppIWICStream\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96846-110">類型： **[ **IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\*\***</span><span class="sxs-lookup"><span data-stu-id="96846-110">Type: **[**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\*\***</span></span>

<span data-ttu-id="96846-111">接收新 [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)指標的指標。</span><span class="sxs-lookup"><span data-stu-id="96846-111">A pointer that receives a pointer to a new [**IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96846-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="96846-112">Return value</span></span>

<span data-ttu-id="96846-113">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="96846-113">Type: **HRESULT**</span></span>

<span data-ttu-id="96846-114">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="96846-114">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="96846-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="96846-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="96846-116">備註</span><span class="sxs-lookup"><span data-stu-id="96846-116">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="96846-117">需求</span><span class="sxs-lookup"><span data-stu-id="96846-117">Requirements</span></span>



| <span data-ttu-id="96846-118">需求</span><span class="sxs-lookup"><span data-stu-id="96846-118">Requirement</span></span> | <span data-ttu-id="96846-119">值</span><span class="sxs-lookup"><span data-stu-id="96846-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96846-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="96846-120">Minimum supported client</span></span><br/> | <span data-ttu-id="96846-121">Windows XP （含 SP2）、 \[ 僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="96846-121">Windows XP with SP2, Windows Vista \[desktop apps only\]</span></span><br/>                                                                                              |
| <span data-ttu-id="96846-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="96846-122">Minimum supported server</span></span><br/> | <span data-ttu-id="96846-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="96846-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                                                                             |
| <span data-ttu-id="96846-124">DLL</span><span class="sxs-lookup"><span data-stu-id="96846-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96846-125"><dt>Windowscodecs.dll;</dt><dt>Wincodec .lib</dt></span><span class="sxs-lookup"><span data-stu-id="96846-125"><dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt></span></span> </dl> |



 

 




