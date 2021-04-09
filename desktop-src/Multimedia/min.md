---
title: 'min 宏 (Minwindef .h) '
description: Min 宏會比較兩個值並傳回較小的值。 資料類型可以是任何數值資料類型（帶正負號或不帶正負號）。 引數的資料類型和傳回值相同。
ms.assetid: c7d5094c-6f26-4799-95c8-804a8b48d39e
keywords:
- 最小宏 Windows 多媒體
topic_type:
- apiref
api_name:
- min
api_location:
- minwindef.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b50680d5902ae2dc895f53f023c4b229b03c7e86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686640"
---
# <a name="min-macro"></a><span data-ttu-id="d8d9b-106">min 巨集</span><span class="sxs-lookup"><span data-stu-id="d8d9b-106">min macro</span></span>

<span data-ttu-id="d8d9b-107">**Min** 宏會比較兩個值並傳回較小的值。</span><span class="sxs-lookup"><span data-stu-id="d8d9b-107">The **min** macro compares two values and returns the smaller one.</span></span> <span data-ttu-id="d8d9b-108">資料類型可以是任何數值資料類型（帶正負號或不帶正負號）。</span><span class="sxs-lookup"><span data-stu-id="d8d9b-108">The data type can be any numeric data type, signed or unsigned.</span></span> <span data-ttu-id="d8d9b-109">引數的資料類型和傳回值相同。</span><span class="sxs-lookup"><span data-stu-id="d8d9b-109">The data type of the arguments and the return value is the same.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8d9b-110">語法</span><span class="sxs-lookup"><span data-stu-id="d8d9b-110">Syntax</span></span>


```C++
 min(
    value1,
    value2
);
```



## <a name="parameters"></a><span data-ttu-id="d8d9b-111">參數</span><span class="sxs-lookup"><span data-stu-id="d8d9b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8d9b-112">*value1*</span><span class="sxs-lookup"><span data-stu-id="d8d9b-112">*value1*</span></span> 
</dt> <dd>

<span data-ttu-id="d8d9b-113">指定兩個值的第一個。</span><span class="sxs-lookup"><span data-stu-id="d8d9b-113">Specifies the first of two values.</span></span>

</dd> <dt>

<span data-ttu-id="d8d9b-114">*value2*</span><span class="sxs-lookup"><span data-stu-id="d8d9b-114">*value2*</span></span> 
</dt> <dd>

<span data-ttu-id="d8d9b-115">指定兩個值的第二個。</span><span class="sxs-lookup"><span data-stu-id="d8d9b-115">Specifies the second of two values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8d9b-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="d8d9b-116">Return value</span></span>

<span data-ttu-id="d8d9b-117">傳回值是兩個指定值的較小者。</span><span class="sxs-lookup"><span data-stu-id="d8d9b-117">The return value is the smaller of the two specified values.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8d9b-118">備註</span><span class="sxs-lookup"><span data-stu-id="d8d9b-118">Remarks</span></span>

<span data-ttu-id="d8d9b-119">**Min** 巨集定義如下：</span><span class="sxs-lookup"><span data-stu-id="d8d9b-119">The **min** macro is defined as follows:</span></span>


```C++
#define min(a, b)  (((a) < (b)) ? (a) : (b)) 
```



## <a name="requirements"></a><span data-ttu-id="d8d9b-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="d8d9b-120">Requirements</span></span>



| <span data-ttu-id="d8d9b-121">需求</span><span class="sxs-lookup"><span data-stu-id="d8d9b-121">Requirement</span></span> | <span data-ttu-id="d8d9b-122">值</span><span class="sxs-lookup"><span data-stu-id="d8d9b-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8d9b-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d8d9b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d8d9b-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d8d9b-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d8d9b-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d8d9b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d8d9b-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d8d9b-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d8d9b-127">標頭</span><span class="sxs-lookup"><span data-stu-id="d8d9b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8d9b-128"><dt>Minwindef。h</dt></span><span class="sxs-lookup"><span data-stu-id="d8d9b-128"><dt>Minwindef.h</dt></span></span> </dl> |



 

 





