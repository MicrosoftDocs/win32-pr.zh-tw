---
description: UpdateColourTable 方法會以新的調色板更新色彩表。
ms.assetid: 61ad98c6-a526-4aac-ad68-d44fadc668de
title: 'CDrawImage. UpdateColourTable 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.UpdateColourTable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fcffdf9e7deaaac5a01f6559ee557c978fcda88f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991044"
---
# <a name="cdrawimageupdatecolourtable-method"></a><span data-ttu-id="8cc35-103">CDrawImage. UpdateColourTable 方法</span><span class="sxs-lookup"><span data-stu-id="8cc35-103">CDrawImage.UpdateColourTable method</span></span>

<span data-ttu-id="8cc35-104">`UpdateColourTable`方法會使用新的調色板來更新色彩表。</span><span class="sxs-lookup"><span data-stu-id="8cc35-104">The `UpdateColourTable` method updates the color table with a new palette.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cc35-105">語法</span><span class="sxs-lookup"><span data-stu-id="8cc35-105">Syntax</span></span>


```C++
void UpdateColourTable(
   HDC              hdc,
   BITMAPINFOHEADER *pbmi
);
```



## <a name="parameters"></a><span data-ttu-id="8cc35-106">參數</span><span class="sxs-lookup"><span data-stu-id="8cc35-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cc35-107">*hdc*</span><span class="sxs-lookup"><span data-stu-id="8cc35-107">*hdc*</span></span> 
</dt> <dd>

<span data-ttu-id="8cc35-108">包含映射的裝置內容。</span><span class="sxs-lookup"><span data-stu-id="8cc35-108">Device context containing the image.</span></span>

</dd> <dt>

<span data-ttu-id="8cc35-109">*pbmi*</span><span class="sxs-lookup"><span data-stu-id="8cc35-109">*pbmi*</span></span> 
</dt> <dd>

<span data-ttu-id="8cc35-110">[**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)結構的指標，其中包含新的調色板。</span><span class="sxs-lookup"><span data-stu-id="8cc35-110">Pointer to a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure containing the new palette.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cc35-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="8cc35-111">Return value</span></span>

<span data-ttu-id="8cc35-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="8cc35-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cc35-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="8cc35-113">Requirements</span></span>



| <span data-ttu-id="8cc35-114">需求</span><span class="sxs-lookup"><span data-stu-id="8cc35-114">Requirement</span></span> | <span data-ttu-id="8cc35-115">值</span><span class="sxs-lookup"><span data-stu-id="8cc35-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cc35-116">標頭</span><span class="sxs-lookup"><span data-stu-id="8cc35-116">Header</span></span><br/>  | <dl> <span data-ttu-id="8cc35-117"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="8cc35-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8cc35-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="8cc35-118">Library</span></span><br/> | <dl> <span data-ttu-id="8cc35-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="8cc35-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cc35-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8cc35-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cc35-121">**CDrawImage 類別**</span><span class="sxs-lookup"><span data-stu-id="8cc35-121">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




