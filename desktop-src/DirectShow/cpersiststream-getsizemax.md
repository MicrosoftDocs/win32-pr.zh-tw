---
description: 抓取目前資料流程所需的最大位元組大小，包括版本號碼。
ms.assetid: 55ea4568-5ca4-4139-8def-bef20071835d
title: 'CPersistStream. GetSizeMax 方法 (Pstream .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.GetSizeMax
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4ef9fcd176463aa8b0bc69fabbd74d78d4ca17cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990061"
---
# <a name="cpersiststreamgetsizemax-method"></a><span data-ttu-id="0a316-103">CPersistStream. GetSizeMax 方法</span><span class="sxs-lookup"><span data-stu-id="0a316-103">CPersistStream.GetSizeMax method</span></span>

<span data-ttu-id="0a316-104">抓取目前資料流程所需的最大位元組大小，包括版本號碼。</span><span class="sxs-lookup"><span data-stu-id="0a316-104">Retrieves the maximum byte size needed for the current stream, including the version number.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a316-105">語法</span><span class="sxs-lookup"><span data-stu-id="0a316-105">Syntax</span></span>


```C++
HRESULT GetSizeMax(
   ULARGE_INTEGER *pcbSize
);
```



## <a name="parameters"></a><span data-ttu-id="0a316-106">參數</span><span class="sxs-lookup"><span data-stu-id="0a316-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a316-107">*pcbSize*</span><span class="sxs-lookup"><span data-stu-id="0a316-107">*pcbSize*</span></span> 
</dt> <dd>

<span data-ttu-id="0a316-108">儲存此資料流程所需的大小（以位元組為單位），包括版本號碼。</span><span class="sxs-lookup"><span data-stu-id="0a316-108">Pointer to the size in bytes needed to save this stream, including the version number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a316-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="0a316-109">Return value</span></span>

<span data-ttu-id="0a316-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="0a316-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a316-111">備註</span><span class="sxs-lookup"><span data-stu-id="0a316-111">Remarks</span></span>

<span data-ttu-id="0a316-112">此成員函式會實作為 **IPersistStream：： GetSizeMax** 方法。</span><span class="sxs-lookup"><span data-stu-id="0a316-112">This member function implements the **IPersistStream::GetSizeMax** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a316-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="0a316-113">Requirements</span></span>



| <span data-ttu-id="0a316-114">需求</span><span class="sxs-lookup"><span data-stu-id="0a316-114">Requirement</span></span> | <span data-ttu-id="0a316-115">值</span><span class="sxs-lookup"><span data-stu-id="0a316-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a316-116">標頭</span><span class="sxs-lookup"><span data-stu-id="0a316-116">Header</span></span><br/>  | <dl> <span data-ttu-id="0a316-117"><dt>Pstream (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="0a316-117"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0a316-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="0a316-118">Library</span></span><br/> | <dl> <span data-ttu-id="0a316-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="0a316-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a316-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0a316-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a316-121">**CPersistStream 類別**</span><span class="sxs-lookup"><span data-stu-id="0a316-121">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




