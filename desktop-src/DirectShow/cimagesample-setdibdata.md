---
description: SetDIBData 方法會指定此物件正在管理之 GDI 裝置獨立點陣圖 (DIB) 的相關資訊。 呼叫這個方法來初始化 CImageSample 物件。
ms.assetid: 850fa16b-d4b9-4fe6-b202-7b54c49a4589
title: 'CImageSample. SetDIBData 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample.SetDIBData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 418263da0416b325b1b080713dd6289f3bcc688e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977421"
---
# <a name="cimagesamplesetdibdata-method"></a><span data-ttu-id="09479-104">CImageSample. SetDIBData 方法</span><span class="sxs-lookup"><span data-stu-id="09479-104">CImageSample.SetDIBData method</span></span>

<span data-ttu-id="09479-105">`SetDIBData`方法會指定此物件正在管理之 GDI 裝置獨立點陣圖 (DIB) 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="09479-105">The `SetDIBData` method specifies information about the GDI device-independent bitmap (DIB) that this object is managing.</span></span> <span data-ttu-id="09479-106">呼叫這個方法來初始化 **CImageSample** 物件。</span><span class="sxs-lookup"><span data-stu-id="09479-106">Call this method to initialize the **CImageSample** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="09479-107">語法</span><span class="sxs-lookup"><span data-stu-id="09479-107">Syntax</span></span>


```C++
void SetDIBData(
   DIBDATA *pDibData
);
```



## <a name="parameters"></a><span data-ttu-id="09479-108">參數</span><span class="sxs-lookup"><span data-stu-id="09479-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09479-109">*pDibData*</span><span class="sxs-lookup"><span data-stu-id="09479-109">*pDibData*</span></span> 
</dt> <dd>

<span data-ttu-id="09479-110">[**DIBDATA**](dibdata.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="09479-110">Pointer to a [**DIBDATA**](dibdata.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09479-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="09479-111">Return value</span></span>

<span data-ttu-id="09479-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="09479-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="09479-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="09479-113">Requirements</span></span>



| <span data-ttu-id="09479-114">需求</span><span class="sxs-lookup"><span data-stu-id="09479-114">Requirement</span></span> | <span data-ttu-id="09479-115">值</span><span class="sxs-lookup"><span data-stu-id="09479-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09479-116">標頭</span><span class="sxs-lookup"><span data-stu-id="09479-116">Header</span></span><br/>  | <dl> <span data-ttu-id="09479-117"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="09479-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="09479-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="09479-118">Library</span></span><br/> | <dl> <span data-ttu-id="09479-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="09479-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09479-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="09479-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09479-121">**CImageSample 類別**</span><span class="sxs-lookup"><span data-stu-id="09479-121">**CImageSample Class**</span></span>](cimagesample.md)
</dt> </dl>

 

 




