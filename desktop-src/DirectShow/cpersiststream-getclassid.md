---
description: 抓取此篩選準則的類別識別碼。
ms.assetid: f0559437-5d0d-4522-a3dc-947e3494b576
title: 'CPersistStream. GetClassID 方法 (Pstream .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7603541eae4f431327a91777488a740afb7f628b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995333"
---
# <a name="cpersiststreamgetclassid-method"></a><span data-ttu-id="15321-103">CPersistStream. GetClassID 方法</span><span class="sxs-lookup"><span data-stu-id="15321-103">CPersistStream.GetClassID method</span></span>

<span data-ttu-id="15321-104">抓取此篩選準則的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="15321-104">Retrieves the class identifier for this filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="15321-105">語法</span><span class="sxs-lookup"><span data-stu-id="15321-105">Syntax</span></span>


```C++
HRESULT GetClassID(
   CLSID *pClsID
);
```



## <a name="parameters"></a><span data-ttu-id="15321-106">參數</span><span class="sxs-lookup"><span data-stu-id="15321-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15321-107">*pClsID*</span><span class="sxs-lookup"><span data-stu-id="15321-107">*pClsID*</span></span> 
</dt> <dd>

<span data-ttu-id="15321-108">CLSID 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="15321-108">Pointer to a CLSID structure.</span></span> <span data-ttu-id="15321-109">將您的類別識別碼複製到這裡。</span><span class="sxs-lookup"><span data-stu-id="15321-109">Copy your class ID to here.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15321-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="15321-110">Return value</span></span>

<span data-ttu-id="15321-111">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="15321-111">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="15321-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="15321-112">Requirements</span></span>



| <span data-ttu-id="15321-113">需求</span><span class="sxs-lookup"><span data-stu-id="15321-113">Requirement</span></span> | <span data-ttu-id="15321-114">值</span><span class="sxs-lookup"><span data-stu-id="15321-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15321-115">標頭</span><span class="sxs-lookup"><span data-stu-id="15321-115">Header</span></span><br/>  | <dl> <span data-ttu-id="15321-116"><dt>Pstream (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="15321-116"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="15321-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="15321-117">Library</span></span><br/> | <dl> <span data-ttu-id="15321-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="15321-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15321-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="15321-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15321-120">**CPersistStream 類別**</span><span class="sxs-lookup"><span data-stu-id="15321-120">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




