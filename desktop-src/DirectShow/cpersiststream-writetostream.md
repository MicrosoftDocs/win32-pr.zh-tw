---
description: 將篩選的資料寫入至指定的資料流程。
ms.assetid: 1b405050-6cfd-4b69-b449-f00a6ecfac6a
title: 'CPersistStream. WriteToStream 方法 (Pstream .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.WriteToStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 893d58986db92e50cbafefe74676481162808abf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998849"
---
# <a name="cpersiststreamwritetostream-method"></a><span data-ttu-id="1037a-103">CPersistStream. WriteToStream 方法</span><span class="sxs-lookup"><span data-stu-id="1037a-103">CPersistStream.WriteToStream method</span></span>

<span data-ttu-id="1037a-104">將篩選的資料寫入至指定的資料流程。</span><span class="sxs-lookup"><span data-stu-id="1037a-104">Writes the filter's data to the given stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="1037a-105">語法</span><span class="sxs-lookup"><span data-stu-id="1037a-105">Syntax</span></span>


```C++
virtual HRESULT WriteToStream(
   IStream *pStream
);
```



## <a name="parameters"></a><span data-ttu-id="1037a-106">參數</span><span class="sxs-lookup"><span data-stu-id="1037a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1037a-107">*pStream*</span><span class="sxs-lookup"><span data-stu-id="1037a-107">*pStream*</span></span> 
</dt> <dd>

<span data-ttu-id="1037a-108">指定篩選資料之目的地資料流程的 **IStream** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="1037a-108">Pointer to an **IStream** interface that specifies the filter data's destination stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1037a-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="1037a-109">Return value</span></span>

<span data-ttu-id="1037a-110">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="1037a-110">Returns S\_OK.</span></span> <span data-ttu-id="1037a-111">衍生類別應該會傳回有效的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="1037a-111">The derived class should return a valid **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1037a-112">備註</span><span class="sxs-lookup"><span data-stu-id="1037a-112">Remarks</span></span>

<span data-ttu-id="1037a-113">預設版本不會寫入任何內容;您可以覆寫它來寫入您類別的特定資料。</span><span class="sxs-lookup"><span data-stu-id="1037a-113">The default version writes nothing; it can be overridden to write data specific to your class.</span></span>

## <a name="requirements"></a><span data-ttu-id="1037a-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="1037a-114">Requirements</span></span>



| <span data-ttu-id="1037a-115">需求</span><span class="sxs-lookup"><span data-stu-id="1037a-115">Requirement</span></span> | <span data-ttu-id="1037a-116">值</span><span class="sxs-lookup"><span data-stu-id="1037a-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1037a-117">標頭</span><span class="sxs-lookup"><span data-stu-id="1037a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="1037a-118"><dt>Pstream (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="1037a-118"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1037a-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="1037a-119">Library</span></span><br/> | <dl> <span data-ttu-id="1037a-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="1037a-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1037a-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1037a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1037a-122">**CPersistStream 類別**</span><span class="sxs-lookup"><span data-stu-id="1037a-122">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




