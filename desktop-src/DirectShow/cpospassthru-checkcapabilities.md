---
description: CheckCapabilities 方法會查詢資料流程是否已指定搜尋功能。 這個方法會實 IMediaSeeking：： CheckCapabilities 方法。
ms.assetid: 48096af6-bbce-4a1f-be9a-fd150ed4536e
title: 'CPosPassThru. CheckCapabilities 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CheckCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 33f7a685684667d2f5d465b14070a595c70b178c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998627"
---
# <a name="cpospassthrucheckcapabilities-method"></a><span data-ttu-id="f760f-104">CPosPassThru. CheckCapabilities 方法</span><span class="sxs-lookup"><span data-stu-id="f760f-104">CPosPassThru.CheckCapabilities method</span></span>

<span data-ttu-id="f760f-105">`CheckCapabilities`方法會查詢資料流程是否已指定搜尋功能。</span><span class="sxs-lookup"><span data-stu-id="f760f-105">The `CheckCapabilities` method queries whether a stream has specified seeking capabilities.</span></span> <span data-ttu-id="f760f-106">這個方法會實 [**IMediaSeeking：： CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) 方法。</span><span class="sxs-lookup"><span data-stu-id="f760f-106">This method implements the [**IMediaSeeking::CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f760f-107">語法</span><span class="sxs-lookup"><span data-stu-id="f760f-107">Syntax</span></span>


```C++
HRESULT CheckCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="f760f-108">參數</span><span class="sxs-lookup"><span data-stu-id="f760f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f760f-109">*pCapabilities*</span><span class="sxs-lookup"><span data-stu-id="f760f-109">*pCapabilities*</span></span> 
</dt> <dd>

<span data-ttu-id="f760f-110">一或多個搜尋中搜尋 [**\_ \_ \_ 功能**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) 屬性的位元組合指標。</span><span class="sxs-lookup"><span data-stu-id="f760f-110">Pointer to a bitwise combination of one or more [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) attributes.</span></span> <span data-ttu-id="f760f-111">當方法傳回時，值會指出哪些屬性可供使用。</span><span class="sxs-lookup"><span data-stu-id="f760f-111">When the method returns, the value indicates which of those attributes are available.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f760f-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="f760f-112">Return value</span></span>

<span data-ttu-id="f760f-113">從連接的 pin 傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="f760f-113">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="f760f-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="f760f-114">Requirements</span></span>



| <span data-ttu-id="f760f-115">需求</span><span class="sxs-lookup"><span data-stu-id="f760f-115">Requirement</span></span> | <span data-ttu-id="f760f-116">值</span><span class="sxs-lookup"><span data-stu-id="f760f-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f760f-117">標頭</span><span class="sxs-lookup"><span data-stu-id="f760f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f760f-118"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="f760f-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f760f-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="f760f-119">Library</span></span><br/> | <dl> <span data-ttu-id="f760f-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="f760f-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f760f-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f760f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f760f-122">**CPosPassThru 類別**</span><span class="sxs-lookup"><span data-stu-id="f760f-122">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




