---
description: SetFormat 方法會初始化格式區塊。
ms.assetid: 71f1c3d4-9c45-4124-8560-378c8f66e710
title: 'CMediaType. SetFormat 方法 (Mtype .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 08dd05faf514581a3325f4922076ba2053cd0c95
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985573"
---
# <a name="cmediatypesetformat-method"></a><span data-ttu-id="3f3dd-103">CMediaType. SetFormat 方法</span><span class="sxs-lookup"><span data-stu-id="3f3dd-103">CMediaType.SetFormat method</span></span>

<span data-ttu-id="3f3dd-104">`SetFormat`方法會初始化格式區塊。</span><span class="sxs-lookup"><span data-stu-id="3f3dd-104">The `SetFormat` method initializes the format block.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f3dd-105">語法</span><span class="sxs-lookup"><span data-stu-id="3f3dd-105">Syntax</span></span>


```C++
BOOL SetFormat(
   BYTE  *pFormat,
   ULONG length
);
```



## <a name="parameters"></a><span data-ttu-id="3f3dd-106">參數</span><span class="sxs-lookup"><span data-stu-id="3f3dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f3dd-107">*Pformatetc 架構*</span><span class="sxs-lookup"><span data-stu-id="3f3dd-107">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="3f3dd-108">包含格式區塊之記憶體區塊的指標。</span><span class="sxs-lookup"><span data-stu-id="3f3dd-108">Pointer to a block of memory that contains the format block.</span></span>

</dd> <dt>

<span data-ttu-id="3f3dd-109">*length* (長度)</span><span class="sxs-lookup"><span data-stu-id="3f3dd-109">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="3f3dd-110">格式區塊的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="3f3dd-110">Length of the format block, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f3dd-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="3f3dd-111">Return value</span></span>

<span data-ttu-id="3f3dd-112">如果成功，則傳回 **TRUE** ; 如果發生錯誤，則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="3f3dd-112">Returns **TRUE** if successful, or **FALSE** if an error occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f3dd-113">備註</span><span class="sxs-lookup"><span data-stu-id="3f3dd-113">Remarks</span></span>

<span data-ttu-id="3f3dd-114">這個方法會為格式區塊配置記憶體，並將 *pformatetc 架構* 指定的緩衝區複製到新的格式區塊。</span><span class="sxs-lookup"><span data-stu-id="3f3dd-114">This method allocates memory for the format block and copies the buffer specified by *pFormat* into the new format block.</span></span> <span data-ttu-id="3f3dd-115">如果媒體類型已包含格式區塊，則會釋放舊的格式區塊。</span><span class="sxs-lookup"><span data-stu-id="3f3dd-115">If the media type already contains a format block, the old one is released.</span></span> <span data-ttu-id="3f3dd-116">方法也會設定 **AM \_ 媒體 \_ 類型** 結構的 **cbFormat** 成員。</span><span class="sxs-lookup"><span data-stu-id="3f3dd-116">The method also sets the **cbFormat** member of the **AM\_MEDIA\_TYPE** structure.</span></span>

<span data-ttu-id="3f3dd-117">若要設定格式類型，請呼叫 [**CMediaType：： SetFormatType**](cmediatype-setformattype.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="3f3dd-117">To set the format type, call the [**CMediaType::SetFormatType**](cmediatype-setformattype.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f3dd-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="3f3dd-118">Requirements</span></span>



| <span data-ttu-id="3f3dd-119">需求</span><span class="sxs-lookup"><span data-stu-id="3f3dd-119">Requirement</span></span> | <span data-ttu-id="3f3dd-120">值</span><span class="sxs-lookup"><span data-stu-id="3f3dd-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f3dd-121">標頭</span><span class="sxs-lookup"><span data-stu-id="3f3dd-121">Header</span></span><br/>  | <dl> <span data-ttu-id="3f3dd-122"><dt>Mtype (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="3f3dd-122"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="3f3dd-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="3f3dd-123">Library</span></span><br/> | <dl> <span data-ttu-id="3f3dd-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="3f3dd-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f3dd-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3f3dd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f3dd-126">**CMediaType 類別**</span><span class="sxs-lookup"><span data-stu-id="3f3dd-126">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




