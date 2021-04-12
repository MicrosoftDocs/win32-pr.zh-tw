---
description: FilterAddObject 函式會將單一物件加入至顯示篩選。
ms.assetid: 796216f4-a407-4a8c-98b3-8c3761d91913
title: 'FilterAddObject 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FilterAddObject
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7fc6c41a675bfe560c060e271e4f9f48f88cd58c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468752"
---
# <a name="filteraddobject-function"></a><span data-ttu-id="20bd1-103">FilterAddObject 函式</span><span class="sxs-lookup"><span data-stu-id="20bd1-103">FilterAddObject function</span></span>

<span data-ttu-id="20bd1-104">**FilterAddObject** 函式會將單一物件加入至 [*顯示篩選*](d.md)。</span><span class="sxs-lookup"><span data-stu-id="20bd1-104">The **FilterAddObject** function adds a single object to a [*display filter*](d.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="20bd1-105">語法</span><span class="sxs-lookup"><span data-stu-id="20bd1-105">Syntax</span></span>


```C++
DWORD WINAPI FilterAddObject(
  _In_  HFILTER        hFilter,
  _Out_ LPFILTEROBJECT lpFilterObject
);
```



## <a name="parameters"></a><span data-ttu-id="20bd1-106">參數</span><span class="sxs-lookup"><span data-stu-id="20bd1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20bd1-107">*hFilter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="20bd1-107">*hFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20bd1-108">顯示篩選的控制碼。</span><span class="sxs-lookup"><span data-stu-id="20bd1-108">Handle to the display filter.</span></span>

</dd> <dt>

<span data-ttu-id="20bd1-109">*lpFilterObject* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="20bd1-109">*lpFilterObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="20bd1-110">[FILTEROBJECT](filterobject.md)結構的指標，該結構定義要加入至篩選的物件。</span><span class="sxs-lookup"><span data-stu-id="20bd1-110">Pointer to a [FILTEROBJECT](filterobject.md) structure that defines the object to be added to the filter.</span></span> <span data-ttu-id="20bd1-111">每個物件都可以是運算子、值或屬性。</span><span class="sxs-lookup"><span data-stu-id="20bd1-111">Each object can be an operator, value, or property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20bd1-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="20bd1-112">Return value</span></span>

<span data-ttu-id="20bd1-113">如果函式成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="20bd1-113">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="20bd1-114">如果函式不成功，則傳回值為錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="20bd1-114">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="20bd1-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="20bd1-115">Return code</span></span>                                                                                              | <span data-ttu-id="20bd1-116">Description</span><span class="sxs-lookup"><span data-stu-id="20bd1-116">Description</span></span>                                                                  |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="20bd1-117"><dt>**NMERR \_ 不正確 \_ 參數**</dt></span><span class="sxs-lookup"><span data-stu-id="20bd1-117"><dt>**NMERR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="20bd1-118">*HFilter* 參數的值無效。</span><span class="sxs-lookup"><span data-stu-id="20bd1-118">The *hFilter* parameter has an invalid value.</span></span><br/>                     |
| <dl> <span data-ttu-id="20bd1-119"><dt>**NMERR \_ \_ 記憶體不足 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="20bd1-119"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl>    | <span data-ttu-id="20bd1-120">網路監視器沒有足夠的記憶體可建立物件。</span><span class="sxs-lookup"><span data-stu-id="20bd1-120">Network Monitor does not have enough memory to create the object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="20bd1-121">備註</span><span class="sxs-lookup"><span data-stu-id="20bd1-121">Remarks</span></span>

<span data-ttu-id="20bd1-122">[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **FilterAddObject** 函數。</span><span class="sxs-lookup"><span data-stu-id="20bd1-122">[*Experts*](e.md) and [*parsers*](p.md) can call the **FilterAddObject** function.</span></span>

<span data-ttu-id="20bd1-123">每次將篩選物件加入至顯示篩選時，就會呼叫 **FilterAddObject** 函數。</span><span class="sxs-lookup"><span data-stu-id="20bd1-123">The **FilterAddObject** function is called each time a filter object is added to the display filter.</span></span> <span data-ttu-id="20bd1-124">顯示篩選是物件的後置堆疊，可以是運算子、值或屬性。</span><span class="sxs-lookup"><span data-stu-id="20bd1-124">The display filter is a postfix stack of objects that can be an operator, value, or property.</span></span>

## <a name="requirements"></a><span data-ttu-id="20bd1-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="20bd1-125">Requirements</span></span>



| <span data-ttu-id="20bd1-126">需求</span><span class="sxs-lookup"><span data-stu-id="20bd1-126">Requirement</span></span> | <span data-ttu-id="20bd1-127">值</span><span class="sxs-lookup"><span data-stu-id="20bd1-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="20bd1-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="20bd1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="20bd1-129">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="20bd1-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="20bd1-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="20bd1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="20bd1-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="20bd1-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="20bd1-132">標頭</span><span class="sxs-lookup"><span data-stu-id="20bd1-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="20bd1-133"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="20bd1-133"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="20bd1-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="20bd1-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="20bd1-135"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="20bd1-135"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="20bd1-136">DLL</span><span class="sxs-lookup"><span data-stu-id="20bd1-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20bd1-137"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20bd1-137"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20bd1-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="20bd1-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20bd1-139">FILTEROBJECT</span><span class="sxs-lookup"><span data-stu-id="20bd1-139">FILTEROBJECT</span></span>](filterobject.md)
</dt> </dl>

 

 




