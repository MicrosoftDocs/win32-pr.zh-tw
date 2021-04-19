---
description: IsClassID 方法會判斷 CLSID 是否符合此類別範本。
ms.assetid: de560f7a-2ccb-44e2-ac32-3b0fea0d80b8
title: 'CFactoryTemplate. IsClassID 方法 (Combase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFactoryTemplate.IsClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94564d7e9db52f8be22717a10f73fffb7fb6fa14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994362"
---
# <a name="cfactorytemplateisclassid-method"></a><span data-ttu-id="8b709-103">CFactoryTemplate. IsClassID 方法</span><span class="sxs-lookup"><span data-stu-id="8b709-103">CFactoryTemplate.IsClassID method</span></span>

<span data-ttu-id="8b709-104">`IsClassID`方法會判斷 CLSID 是否符合此類別範本。</span><span class="sxs-lookup"><span data-stu-id="8b709-104">The `IsClassID` method determines whether a CLSID matches this class template.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b709-105">語法</span><span class="sxs-lookup"><span data-stu-id="8b709-105">Syntax</span></span>


```C++
BOOL IsClassID(
   REFCLSID rclsid
);
```



## <a name="parameters"></a><span data-ttu-id="8b709-106">參數</span><span class="sxs-lookup"><span data-stu-id="8b709-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b709-107">*rclsid*</span><span class="sxs-lookup"><span data-stu-id="8b709-107">*rclsid*</span></span> 
</dt> <dd>

<span data-ttu-id="8b709-108">CLSID 的參考。</span><span class="sxs-lookup"><span data-stu-id="8b709-108">Reference to a CLSID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b709-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="8b709-109">Return value</span></span>

<span data-ttu-id="8b709-110">如果 *rclsid* 參數與 [**CFactoryTemplate：： m \_ CLSID**](cfactorytemplate-m-clsid.md)成員變數的 Clsid 相同，則傳回 **TRUE** ，否則傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="8b709-110">Returns **TRUE** if the *rclsid* parameter is the same CLSID as the [**CFactoryTemplate::m\_ClsID**](cfactorytemplate-m-clsid.md) member variable, or else returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b709-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="8b709-111">Requirements</span></span>



| <span data-ttu-id="8b709-112">需求</span><span class="sxs-lookup"><span data-stu-id="8b709-112">Requirement</span></span> | <span data-ttu-id="8b709-113">值</span><span class="sxs-lookup"><span data-stu-id="8b709-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b709-114">標頭</span><span class="sxs-lookup"><span data-stu-id="8b709-114">Header</span></span><br/>  | <dl> <span data-ttu-id="8b709-115"><dt>Combase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="8b709-115"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8b709-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="8b709-116">Library</span></span><br/> | <dl> <span data-ttu-id="8b709-117"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="8b709-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b709-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8b709-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b709-119">**CFactoryTemplate 類別**</span><span class="sxs-lookup"><span data-stu-id="8b709-119">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




