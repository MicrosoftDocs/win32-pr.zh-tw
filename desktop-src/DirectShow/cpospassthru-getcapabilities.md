---
description: CPosPassThru. GetCapabilities 方法-GetCapabilities 方法會抓取資料流程的所有搜尋功能。 這個方法會實 IMediaSeeking：： GetCapabilities 方法。
ms.assetid: c60c4f47-48de-47d0-9b87-589b84df842c
title: 'CPosPassThru. GetCapabilities 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c21838d3df72d52255d0a2e35dd0b7d34ef55411
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085566"
---
# <a name="cpospassthrugetcapabilities-method"></a><span data-ttu-id="79e83-104">CPosPassThru. GetCapabilities 方法</span><span class="sxs-lookup"><span data-stu-id="79e83-104">CPosPassThru.GetCapabilities method</span></span>

<span data-ttu-id="79e83-105">**GetCapabilities** 方法會抓取資料流程的所有搜尋功能。</span><span class="sxs-lookup"><span data-stu-id="79e83-105">The **GetCapabilities** method retrieves all the seeking capabilities of the stream.</span></span> <span data-ttu-id="79e83-106">這個方法會實 [**IMediaSeeking：： GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) 方法。</span><span class="sxs-lookup"><span data-stu-id="79e83-106">This method implements the [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="79e83-107">語法</span><span class="sxs-lookup"><span data-stu-id="79e83-107">Syntax</span></span>


```C++
HRESULT GetCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="79e83-108">參數</span><span class="sxs-lookup"><span data-stu-id="79e83-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79e83-109">*pCapabilities*</span><span class="sxs-lookup"><span data-stu-id="79e83-109">*pCapabilities*</span></span> 
</dt> <dd>

<span data-ttu-id="79e83-110">變數的指標，此變數會接收搜尋 [**\_ \_ \_ 功能**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) 旗標之 AM 的位元組合。</span><span class="sxs-lookup"><span data-stu-id="79e83-110">Pointer to a variable that receives a bitwise combination of [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) flags.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79e83-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="79e83-111">Return value</span></span>

<span data-ttu-id="79e83-112">從連接的 pin 傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="79e83-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="79e83-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="79e83-113">Requirements</span></span>



| <span data-ttu-id="79e83-114">需求</span><span class="sxs-lookup"><span data-stu-id="79e83-114">Requirement</span></span> | <span data-ttu-id="79e83-115">值</span><span class="sxs-lookup"><span data-stu-id="79e83-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79e83-116">標頭</span><span class="sxs-lookup"><span data-stu-id="79e83-116">Header</span></span><br/>  | <dl> <span data-ttu-id="79e83-117"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="79e83-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="79e83-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="79e83-118">Library</span></span><br/> | <dl> <span data-ttu-id="79e83-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="79e83-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79e83-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="79e83-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79e83-121">**CPosPassThru 類別**</span><span class="sxs-lookup"><span data-stu-id="79e83-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




