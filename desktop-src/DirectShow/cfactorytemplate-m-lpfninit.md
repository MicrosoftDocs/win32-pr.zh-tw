---
description: 從 DLL 進入點呼叫之函式的指標。 可以是 NULL。
ms.assetid: 0769f55b-6f0d-4a89-9d3f-64f211426342
title: 'CFactoryTemplate：： m_lpfnInit 成員 (Combase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lpfnInit
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b44181f926f77ecc7cc22673622d4a0d3dcb7d26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994768"
---
# <a name="cfactorytemplatem_lpfninit-member"></a><span data-ttu-id="8d386-104">CFactoryTemplate：： m \_ lpfnInit 成員</span><span class="sxs-lookup"><span data-stu-id="8d386-104">CFactoryTemplate::m\_lpfnInit member</span></span>

<span data-ttu-id="8d386-105">從 DLL 進入點呼叫之函式的指標。</span><span class="sxs-lookup"><span data-stu-id="8d386-105">Pointer to a function that gets called from the DLL entry point.</span></span> <span data-ttu-id="8d386-106">可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8d386-106">Can be **NULL**.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d386-107">語法</span><span class="sxs-lookup"><span data-stu-id="8d386-107">Syntax</span></span>


```C++
LPFNInitRoutine m_lpfnInit;
```



## <a name="remarks"></a><span data-ttu-id="8d386-108">備註</span><span class="sxs-lookup"><span data-stu-id="8d386-108">Remarks</span></span>

<span data-ttu-id="8d386-109">函數指標型別為 [**LPFNInitRoutine**](lpfninitroutine.md)。</span><span class="sxs-lookup"><span data-stu-id="8d386-109">The function pointer type is [**LPFNInitRoutine**](lpfninitroutine.md).</span></span> <span data-ttu-id="8d386-110">如果您在 DLL 中提供此函式，DLL 進入點函數會使用下列參數來呼叫它：</span><span class="sxs-lookup"><span data-stu-id="8d386-110">If you provide this function in your DLL, the DLL entry-point function calls it with following parameters:</span></span>

-   <span data-ttu-id="8d386-111">*bLoading*：載入 dll 時 **為 TRUE** ，卸載 dll 時為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="8d386-111">*bLoading*: **TRUE** when the DLL is loaded, **FALSE** when the DLL is unloaded.</span></span>
-   <span data-ttu-id="8d386-112">*rclsid*：物件之 CLISD 的指標，在 [**CFactoryTemplate：： m \_ ClsID**](cfactorytemplate-m-clsid.md) 成員變數中指定。</span><span class="sxs-lookup"><span data-stu-id="8d386-112">*rclsid*: Pointer to the object's CLISD, specified in the [**CFactoryTemplate::m\_ClsID**](cfactorytemplate-m-clsid.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d386-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="8d386-113">Requirements</span></span>



| <span data-ttu-id="8d386-114">需求</span><span class="sxs-lookup"><span data-stu-id="8d386-114">Requirement</span></span> | <span data-ttu-id="8d386-115">值</span><span class="sxs-lookup"><span data-stu-id="8d386-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d386-116">標頭</span><span class="sxs-lookup"><span data-stu-id="8d386-116">Header</span></span><br/>  | <dl> <span data-ttu-id="8d386-117"><dt>Combase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="8d386-117"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8d386-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="8d386-118">Library</span></span><br/> | <dl> <span data-ttu-id="8d386-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="8d386-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d386-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8d386-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d386-121">**CFactoryTemplate 類別**</span><span class="sxs-lookup"><span data-stu-id="8d386-121">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




