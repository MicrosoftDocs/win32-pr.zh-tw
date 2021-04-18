---
description: GetClassID 方法會抓取物件 (CLSID) 的類別識別碼。 這個方法會實 IPersist：： GetClassID 方法。
ms.assetid: 3d2cc6a3-67d1-4dd9-916b-7c350ce6a542
title: 'CSystemClock. GetClassID 方法 (Sysclock .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2f83d3e3c2efcbcb5d4604bc5c50a37dc020f0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976281"
---
# <a name="csystemclockgetclassid-method"></a><span data-ttu-id="747b2-104">CSystemClock. GetClassID 方法</span><span class="sxs-lookup"><span data-stu-id="747b2-104">CSystemClock.GetClassID method</span></span>

<span data-ttu-id="747b2-105">方法會抓取 `GetClassID` 物件 (CLSID) 的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="747b2-105">The `GetClassID` method retrieves the class identifier (CLSID) of the object.</span></span> <span data-ttu-id="747b2-106">這個方法會實 **IPersist：： GetClassID** 方法。</span><span class="sxs-lookup"><span data-stu-id="747b2-106">This method implements the **IPersist::GetClassID** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="747b2-107">語法</span><span class="sxs-lookup"><span data-stu-id="747b2-107">Syntax</span></span>


```C++
HRESULT GetClassID(
   CLSID *pClsID
);
```



## <a name="parameters"></a><span data-ttu-id="747b2-108">參數</span><span class="sxs-lookup"><span data-stu-id="747b2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="747b2-109">*pClsID*</span><span class="sxs-lookup"><span data-stu-id="747b2-109">*pClsID*</span></span> 
</dt> <dd>

<span data-ttu-id="747b2-110">接收值 CLSID SystemClock 之變數的指標 \_ 。</span><span class="sxs-lookup"><span data-stu-id="747b2-110">Pointer to a variable that receives the value CLSID\_SystemClock.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="747b2-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="747b2-111">Return value</span></span>

<span data-ttu-id="747b2-112">傳回 S \_ OK 或 E \_ 指標。</span><span class="sxs-lookup"><span data-stu-id="747b2-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="747b2-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="747b2-113">Requirements</span></span>



| <span data-ttu-id="747b2-114">需求</span><span class="sxs-lookup"><span data-stu-id="747b2-114">Requirement</span></span> | <span data-ttu-id="747b2-115">值</span><span class="sxs-lookup"><span data-stu-id="747b2-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="747b2-116">版本</span><span class="sxs-lookup"><span data-stu-id="747b2-116">Version</span></span><br/> | <span data-ttu-id="747b2-117">CSystemClock 類別</span><span class="sxs-lookup"><span data-stu-id="747b2-117">CSystemClock Class</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="747b2-118">標頭</span><span class="sxs-lookup"><span data-stu-id="747b2-118">Header</span></span><br/>  | <dl> <span data-ttu-id="747b2-119"><dt>Sysclock (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="747b2-119"><dt>Sysclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="747b2-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="747b2-120">Library</span></span><br/> | <dl> <span data-ttu-id="747b2-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="747b2-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




