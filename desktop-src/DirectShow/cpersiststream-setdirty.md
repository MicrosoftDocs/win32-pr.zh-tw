---
description: 變更目前資料流程的變更旗標。
ms.assetid: 65fa7fbe-4fa7-45a3-91a4-4a3547b035b9
title: 'CPersistStream. SetDirty 方法 (Pstream .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.SetDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 382b74f6314beb586b1e51c02a257cad8904c188
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998850"
---
# <a name="cpersiststreamsetdirty-method"></a><span data-ttu-id="ff233-103">CPersistStream. SetDirty 方法</span><span class="sxs-lookup"><span data-stu-id="ff233-103">CPersistStream.SetDirty method</span></span>

<span data-ttu-id="ff233-104">變更目前資料流程的變更旗標。</span><span class="sxs-lookup"><span data-stu-id="ff233-104">Changes the dirty flag for the current stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff233-105">語法</span><span class="sxs-lookup"><span data-stu-id="ff233-105">Syntax</span></span>


```C++
HRESULT SetDirty(
   BOOL fDirty
);
```



## <a name="parameters"></a><span data-ttu-id="ff233-106">參數</span><span class="sxs-lookup"><span data-stu-id="ff233-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff233-107">*fDirty*</span><span class="sxs-lookup"><span data-stu-id="ff233-107">*fDirty*</span></span> 
</dt> <dd>

<span data-ttu-id="ff233-108">此資料流程的新中途旗標。</span><span class="sxs-lookup"><span data-stu-id="ff233-108">New dirty flag for this stream.</span></span> <span data-ttu-id="ff233-109">**TRUE** 表示資料尚未儲存。</span><span class="sxs-lookup"><span data-stu-id="ff233-109">**TRUE** means that the data has not been saved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff233-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="ff233-110">Return value</span></span>

<span data-ttu-id="ff233-111">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="ff233-111">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff233-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff233-112">Requirements</span></span>



| <span data-ttu-id="ff233-113">需求</span><span class="sxs-lookup"><span data-stu-id="ff233-113">Requirement</span></span> | <span data-ttu-id="ff233-114">值</span><span class="sxs-lookup"><span data-stu-id="ff233-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff233-115">標頭</span><span class="sxs-lookup"><span data-stu-id="ff233-115">Header</span></span><br/>  | <dl> <span data-ttu-id="ff233-116"><dt>Pstream (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="ff233-116"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ff233-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="ff233-117">Library</span></span><br/> | <dl> <span data-ttu-id="ff233-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="ff233-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff233-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ff233-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff233-120">**CPersistStream 類別**</span><span class="sxs-lookup"><span data-stu-id="ff233-120">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




