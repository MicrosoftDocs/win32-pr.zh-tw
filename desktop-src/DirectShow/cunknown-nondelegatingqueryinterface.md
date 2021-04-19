---
description: 捕獲介面指標並遞增參考計數。 這個方法會實 INonDelegatingUnknown：： NonDelegatingQueryInterface 方法。
ms.assetid: 451ca350-f40b-4cbf-ac39-e86dadb48a24
title: 'CUnknown. NonDelegatingQueryInterface 方法 (Combase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.NonDelegatingQueryInterface
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b41810eb52db38644bda472907228cd812f76f6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001847"
---
# <a name="cunknownnondelegatingqueryinterface-method"></a><span data-ttu-id="3897d-104">CUnknown. NonDelegatingQueryInterface 方法</span><span class="sxs-lookup"><span data-stu-id="3897d-104">CUnknown.NonDelegatingQueryInterface method</span></span>

<span data-ttu-id="3897d-105">捕獲介面指標並遞增參考計數。</span><span class="sxs-lookup"><span data-stu-id="3897d-105">Retrieves an interface pointer and increments the reference count.</span></span> <span data-ttu-id="3897d-106">這個方法會實 **INonDelegatingUnknown：： NonDelegatingQueryInterface** 方法。</span><span class="sxs-lookup"><span data-stu-id="3897d-106">This method implements the **INonDelegatingUnknown::NonDelegatingQueryInterface** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3897d-107">語法</span><span class="sxs-lookup"><span data-stu-id="3897d-107">Syntax</span></span>


```C++
HRESULT NonDelegatingQueryInterface(
   REFIID riid,
   void   **ppv
);
```



## <a name="parameters"></a><span data-ttu-id="3897d-108">參數</span><span class="sxs-lookup"><span data-stu-id="3897d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3897d-109">*riid*</span><span class="sxs-lookup"><span data-stu-id="3897d-109">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="3897d-110">介面的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3897d-110">Identifier of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="3897d-111">*Ppv*</span><span class="sxs-lookup"><span data-stu-id="3897d-111">*ppv*</span></span> 
</dt> <dd>

<span data-ttu-id="3897d-112">接收介面之指標的位址。</span><span class="sxs-lookup"><span data-stu-id="3897d-112">Address of a pointer to receive the interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3897d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="3897d-113">Return value</span></span>

<span data-ttu-id="3897d-114">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="3897d-114">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="3897d-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="3897d-115">Return code</span></span>                                                                                   | <span data-ttu-id="3897d-116">Description</span><span class="sxs-lookup"><span data-stu-id="3897d-116">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="3897d-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="3897d-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3897d-118">成功。</span><span class="sxs-lookup"><span data-stu-id="3897d-118">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="3897d-119"><dt>**E \_ NOINTERFACE**</dt></span><span class="sxs-lookup"><span data-stu-id="3897d-119"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="3897d-120">物件不支援此介面。</span><span class="sxs-lookup"><span data-stu-id="3897d-120">Object does not support this interface.</span></span><br/> |
| <dl> <span data-ttu-id="3897d-121"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="3897d-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="3897d-122">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="3897d-122">**NULL** pointer argument.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="3897d-123">備註</span><span class="sxs-lookup"><span data-stu-id="3897d-123">Remarks</span></span>

<span data-ttu-id="3897d-124">**CUnknown** 類別只會公開 **IUknown** 介面。</span><span class="sxs-lookup"><span data-stu-id="3897d-124">The **CUnknown** class exposes only the **IUknown** interface.</span></span> <span data-ttu-id="3897d-125">覆寫此方法以公開其他介面。</span><span class="sxs-lookup"><span data-stu-id="3897d-125">Override this method to expose additional interfaces.</span></span> <span data-ttu-id="3897d-126">如需有關如何覆寫這個方法的詳細資訊，請參閱 [如何執行 IUnknown](how-to-implement-iunknown.md)。</span><span class="sxs-lookup"><span data-stu-id="3897d-126">For information on how to override this method, see [How to Implement IUnknown](how-to-implement-iunknown.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3897d-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="3897d-127">Requirements</span></span>



| <span data-ttu-id="3897d-128">需求</span><span class="sxs-lookup"><span data-stu-id="3897d-128">Requirement</span></span> | <span data-ttu-id="3897d-129">值</span><span class="sxs-lookup"><span data-stu-id="3897d-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3897d-130">標頭</span><span class="sxs-lookup"><span data-stu-id="3897d-130">Header</span></span><br/>  | <dl> <span data-ttu-id="3897d-131"><dt>Combase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="3897d-131"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3897d-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="3897d-132">Library</span></span><br/> | <dl> <span data-ttu-id="3897d-133"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="3897d-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




