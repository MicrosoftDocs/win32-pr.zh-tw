---
description: CopyMediaType 函式會將 AM \_ 媒體 \_ 類型結構複製到另一個結構，包括格式區塊
ms.assetid: 5b47e197-abb5-4b2c-ad65-a506c5e239be
title: 'CopyMediaType 函式 (Mtype) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CopyMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2e37f277244ae9b82c395d7901917e1fc1e78b35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976157"
---
# <a name="copymediatype-function"></a><span data-ttu-id="3e478-103">CopyMediaType 函式</span><span class="sxs-lookup"><span data-stu-id="3e478-103">CopyMediaType function</span></span>

<span data-ttu-id="3e478-104">**CopyMediaType** 函式會將 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構複製到另一個結構，包括格式區塊</span><span class="sxs-lookup"><span data-stu-id="3e478-104">The **CopyMediaType** function copies an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure into another structure, including the format block</span></span>

## <a name="syntax"></a><span data-ttu-id="3e478-105">語法</span><span class="sxs-lookup"><span data-stu-id="3e478-105">Syntax</span></span>


```C++
HRESULT WINAPI CopyMediaType(
         AM_MEDIA_TYPE *pmtTarget,
   const AM_MEDIA_TYPE *pmtSource
);
```



## <a name="parameters"></a><span data-ttu-id="3e478-106">參數</span><span class="sxs-lookup"><span data-stu-id="3e478-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e478-107">*pmtTarget*</span><span class="sxs-lookup"><span data-stu-id="3e478-107">*pmtTarget*</span></span> 
</dt> <dd>

<span data-ttu-id="3e478-108">[**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="3e478-108">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="3e478-109">方法會將媒體類型複製到這個結構中。</span><span class="sxs-lookup"><span data-stu-id="3e478-109">The method copies the media type into this structure.</span></span>

</dd> <dt>

<span data-ttu-id="3e478-110">*pmtSource*</span><span class="sxs-lookup"><span data-stu-id="3e478-110">*pmtSource*</span></span> 
</dt> <dd>

<span data-ttu-id="3e478-111">要複製之來源 [**\_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="3e478-111">Pointer to a source [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure to copy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e478-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="3e478-112">Return value</span></span>

<span data-ttu-id="3e478-113">傳回 \_ [確定] 或 [E \_ OUTOFMEMORY]。</span><span class="sxs-lookup"><span data-stu-id="3e478-113">Returns S\_OK or E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e478-114">備註</span><span class="sxs-lookup"><span data-stu-id="3e478-114">Remarks</span></span>

<span data-ttu-id="3e478-115">此函式會配置格式區塊的記憶體。</span><span class="sxs-lookup"><span data-stu-id="3e478-115">This function allocates the memory for the format block.</span></span> <span data-ttu-id="3e478-116">如果 *pmtTarget* 參數已經包含已配置的格式區塊，就會發生記憶體流失。</span><span class="sxs-lookup"><span data-stu-id="3e478-116">If the *pmtTarget* parameter already contains an allocated format block, a memory leak will occur.</span></span> <span data-ttu-id="3e478-117">若要避免記憶體流失，請在呼叫此函式之前呼叫 [**FreeMediaType**](freemediatype.md) 。</span><span class="sxs-lookup"><span data-stu-id="3e478-117">To avoid a memory leak, call [**FreeMediaType**](freemediatype.md) before calling this function.</span></span>

<span data-ttu-id="3e478-118">在方法傳回之後，請在 *pmtTarget* 上呼叫 [**FreeMediaType**](freemediatype.md) ，以釋放格式區塊。</span><span class="sxs-lookup"><span data-stu-id="3e478-118">After the method returns, call [**FreeMediaType**](freemediatype.md) on *pmtTarget* to free the format block.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e478-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="3e478-119">Requirements</span></span>



| <span data-ttu-id="3e478-120">需求</span><span class="sxs-lookup"><span data-stu-id="3e478-120">Requirement</span></span> | <span data-ttu-id="3e478-121">值</span><span class="sxs-lookup"><span data-stu-id="3e478-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e478-122">標頭</span><span class="sxs-lookup"><span data-stu-id="3e478-122">Header</span></span><br/>  | <dl> <span data-ttu-id="3e478-123"><dt>Mtype (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="3e478-123"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="3e478-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="3e478-124">Library</span></span><br/> | <dl> <span data-ttu-id="3e478-125"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="3e478-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e478-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3e478-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e478-127">**媒體類型函式**</span><span class="sxs-lookup"><span data-stu-id="3e478-127">**Media Type Functions**</span></span>](media-type-functions.md)
</dt> </dl>

 

 




