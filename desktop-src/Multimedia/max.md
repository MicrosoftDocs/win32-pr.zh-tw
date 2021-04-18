---
title: 'max 宏 (Minwindef .h) '
description: Max 宏會比較兩個值並傳回較大的值。 資料類型可以是任何數值資料類型（帶正負號或不帶正負號）。 引數的資料類型和傳回值相同。
ms.assetid: 224d2ef7-6764-49c0-9782-51bfadbfb77f
keywords:
- 最大宏 Windows 多媒體
topic_type:
- apiref
api_name:
- max
api_location:
- minwindef.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b484f2505958aca04745c63ca63a0dd131a51ed9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508479"
---
# <a name="max-macro"></a><span data-ttu-id="5e8b2-106">max 巨集</span><span class="sxs-lookup"><span data-stu-id="5e8b2-106">max macro</span></span>

<span data-ttu-id="5e8b2-107">**Max** 宏會比較兩個值並傳回較大的值。</span><span class="sxs-lookup"><span data-stu-id="5e8b2-107">The **max** macro compares two values and returns the larger one.</span></span> <span data-ttu-id="5e8b2-108">資料類型可以是任何數值資料類型（帶正負號或不帶正負號）。</span><span class="sxs-lookup"><span data-stu-id="5e8b2-108">The data type can be any numeric data type, signed or unsigned.</span></span> <span data-ttu-id="5e8b2-109">引數的資料類型和傳回值相同。</span><span class="sxs-lookup"><span data-stu-id="5e8b2-109">The data type of the arguments and the return value is the same.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e8b2-110">語法</span><span class="sxs-lookup"><span data-stu-id="5e8b2-110">Syntax</span></span>


```C++
 max(
    value1,
    value2
);
```



## <a name="parameters"></a><span data-ttu-id="5e8b2-111">參數</span><span class="sxs-lookup"><span data-stu-id="5e8b2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e8b2-112">*value1*</span><span class="sxs-lookup"><span data-stu-id="5e8b2-112">*value1*</span></span> 
</dt> <dd>

<span data-ttu-id="5e8b2-113">指定兩個值的第一個。</span><span class="sxs-lookup"><span data-stu-id="5e8b2-113">Specifies the first of two values.</span></span>

</dd> <dt>

<span data-ttu-id="5e8b2-114">*value2*</span><span class="sxs-lookup"><span data-stu-id="5e8b2-114">*value2*</span></span> 
</dt> <dd>

<span data-ttu-id="5e8b2-115">指定兩個值的第二個。</span><span class="sxs-lookup"><span data-stu-id="5e8b2-115">Specifies the second of two values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e8b2-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="5e8b2-116">Return value</span></span>

<span data-ttu-id="5e8b2-117">傳回值是兩個指定值的最大值。</span><span class="sxs-lookup"><span data-stu-id="5e8b2-117">The return value is the greater of the two specified values.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e8b2-118">備註</span><span class="sxs-lookup"><span data-stu-id="5e8b2-118">Remarks</span></span>

<span data-ttu-id="5e8b2-119">**Max** 宏的定義如下：</span><span class="sxs-lookup"><span data-stu-id="5e8b2-119">The **max** macro is defined as follows:</span></span>


```C++
#define max(a, b)  (((a) > (b)) ? (a) : (b)) 
```



## <a name="requirements"></a><span data-ttu-id="5e8b2-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="5e8b2-120">Requirements</span></span>



| <span data-ttu-id="5e8b2-121">需求</span><span class="sxs-lookup"><span data-stu-id="5e8b2-121">Requirement</span></span> | <span data-ttu-id="5e8b2-122">值</span><span class="sxs-lookup"><span data-stu-id="5e8b2-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e8b2-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5e8b2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5e8b2-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5e8b2-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5e8b2-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5e8b2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5e8b2-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5e8b2-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5e8b2-127">標頭</span><span class="sxs-lookup"><span data-stu-id="5e8b2-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e8b2-128"><dt>Minwindef。h</dt></span><span class="sxs-lookup"><span data-stu-id="5e8b2-128"><dt>Minwindef.h</dt></span></span> </dl> |



 

 





