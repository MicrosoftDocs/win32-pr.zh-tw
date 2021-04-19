---
description: 將篩選的資料儲存至指定的資料流程。
ms.assetid: f45c8c6e-f0bb-4358-805a-da2669706d34
title: 'CPersistStream： Save 方法 (Pstream .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.Save
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c16e4820f846d2d60382fabd6aafe3ad82880193
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989839"
---
# <a name="cpersiststreamsave-method"></a><span data-ttu-id="50e8b-103">CPersistStream。 Save 方法</span><span class="sxs-lookup"><span data-stu-id="50e8b-103">CPersistStream.Save method</span></span>

<span data-ttu-id="50e8b-104">將篩選的資料儲存至指定的資料流程。</span><span class="sxs-lookup"><span data-stu-id="50e8b-104">Saves the filter's data to the given stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="50e8b-105">語法</span><span class="sxs-lookup"><span data-stu-id="50e8b-105">Syntax</span></span>


```C++
HRESULT Save(
   LPSTREAM pStm,
   BOOL     fClearDirty
);
```



## <a name="parameters"></a><span data-ttu-id="50e8b-106">參數</span><span class="sxs-lookup"><span data-stu-id="50e8b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50e8b-107">*pStm*</span><span class="sxs-lookup"><span data-stu-id="50e8b-107">*pStm*</span></span> 
</dt> <dd>

<span data-ttu-id="50e8b-108">要儲存資料的資料流程指標。</span><span class="sxs-lookup"><span data-stu-id="50e8b-108">Pointer to the stream to which data is to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="50e8b-109">*fClearDirty*</span><span class="sxs-lookup"><span data-stu-id="50e8b-109">*fClearDirty*</span></span> 
</dt> <dd>

<span data-ttu-id="50e8b-110">指出是否要重設目前資料流程之中途旗標的旗標; **TRUE** 表示重設它。</span><span class="sxs-lookup"><span data-stu-id="50e8b-110">Flag that indicates whether to reset the current stream's dirty flag; **TRUE** means to reset it.</span></span> <span data-ttu-id="50e8b-111"> (在儲存作業中呼叫方法時，此值通常為 **TRUE**。當呼叫做為「另存新檔」作業的一部分時，值通常是 **FALSE**。 ) </span><span class="sxs-lookup"><span data-stu-id="50e8b-111">(When the method is called as part of a Save operation, the value is typically **TRUE**; when called as part of a Save As operation, the value is typically **FALSE**.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50e8b-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="50e8b-112">Return value</span></span>

<span data-ttu-id="50e8b-113">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="50e8b-113">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="50e8b-114">備註</span><span class="sxs-lookup"><span data-stu-id="50e8b-114">Remarks</span></span>

<span data-ttu-id="50e8b-115">此成員函式會實行 **IPersistStream：： Save** 方法。</span><span class="sxs-lookup"><span data-stu-id="50e8b-115">This member function implements the **IPersistStream::Save** method.</span></span> <span data-ttu-id="50e8b-116">它會以軟體版本呼叫 **WriteInt** 、使用 *pStm* 中的串流呼叫 [**CPersistStream：： WriteToStream**](cpersiststream-writetostream.md) ，然後重設 **mp \_ fDirty**。</span><span class="sxs-lookup"><span data-stu-id="50e8b-116">It calls **WriteInt** with the software version, calls [**CPersistStream::WriteToStream**](cpersiststream-writetostream.md) with the stream in *pStm*, and resets **mPS\_fDirty**.</span></span>

## <a name="requirements"></a><span data-ttu-id="50e8b-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="50e8b-117">Requirements</span></span>



| <span data-ttu-id="50e8b-118">需求</span><span class="sxs-lookup"><span data-stu-id="50e8b-118">Requirement</span></span> | <span data-ttu-id="50e8b-119">值</span><span class="sxs-lookup"><span data-stu-id="50e8b-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50e8b-120">標頭</span><span class="sxs-lookup"><span data-stu-id="50e8b-120">Header</span></span><br/>  | <dl> <span data-ttu-id="50e8b-121"><dt>Pstream (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="50e8b-121"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="50e8b-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="50e8b-122">Library</span></span><br/> | <dl> <span data-ttu-id="50e8b-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="50e8b-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50e8b-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50e8b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50e8b-125">**CPersistStream 類別**</span><span class="sxs-lookup"><span data-stu-id="50e8b-125">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




