---
description: 檢查指標是否為 Null。 如果指標為 Null，則宏出現的函式或方法會傳回指定的值。
ms.assetid: eca73fbf-5fd8-4b76-af06-ca0c22510b55
title: 'CheckPointer 宏 (Wxdebug) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CheckPointer
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 04f442303e520ef758a3576d21c2df810ef26fb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994360"
---
# <a name="checkpointer-macro"></a><span data-ttu-id="d218a-104">CheckPointer 宏</span><span class="sxs-lookup"><span data-stu-id="d218a-104">CheckPointer macro</span></span>

<span data-ttu-id="d218a-105">檢查指標是否為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d218a-105">Checks whether a pointer is **NULL**.</span></span> <span data-ttu-id="d218a-106">如果指標為 **Null**，則宏出現的函式或方法會傳回指定的值。</span><span class="sxs-lookup"><span data-stu-id="d218a-106">If the pointer is **NULL**, the function or method in which the macro appears returns the specified value.</span></span>

## <a name="syntax"></a><span data-ttu-id="d218a-107">語法</span><span class="sxs-lookup"><span data-stu-id="d218a-107">Syntax</span></span>


```C++
HRESULT CheckPointer(
    p,
    ret
);
```



## <a name="parameters"></a><span data-ttu-id="d218a-108">參數</span><span class="sxs-lookup"><span data-stu-id="d218a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d218a-109">*P*</span><span class="sxs-lookup"><span data-stu-id="d218a-109">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="d218a-110">要檢查的指標。</span><span class="sxs-lookup"><span data-stu-id="d218a-110">Pointer to check.</span></span>

</dd> <dt>

<span data-ttu-id="d218a-111">*Ret*</span><span class="sxs-lookup"><span data-stu-id="d218a-111">*ret*</span></span> 
</dt> <dd>

<span data-ttu-id="d218a-112">如果 *p* 為 **Null**，則函式或方法所傳回的值。</span><span class="sxs-lookup"><span data-stu-id="d218a-112">Value that the function or method returns if *p* is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d218a-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d218a-113">Return value</span></span>

<span data-ttu-id="d218a-114">如果 *p* 為 **Null**，則周圍函數會傳回 *ret* 。</span><span class="sxs-lookup"><span data-stu-id="d218a-114">The surrounding function returns *ret* if *p* is **NULL**.</span></span> <span data-ttu-id="d218a-115">否則，宏不會造成周圍函數傳回。</span><span class="sxs-lookup"><span data-stu-id="d218a-115">Otherwise, the macro does not cause the surrounding function to return.</span></span>

## <a name="examples"></a><span data-ttu-id="d218a-116">範例</span><span class="sxs-lookup"><span data-stu-id="d218a-116">Examples</span></span>


```
HRESULT MyFunction(VOID *pSomeParameter)
{
    // Return E_INVALIDARG if pSomeParameter is NULL.
    CheckPointer(pSomeParameter, E_INVALIDARG)

    // Rest of the function (not shown).
}
```



## <a name="requirements"></a><span data-ttu-id="d218a-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="d218a-117">Requirements</span></span>



| <span data-ttu-id="d218a-118">需求</span><span class="sxs-lookup"><span data-stu-id="d218a-118">Requirement</span></span> | <span data-ttu-id="d218a-119">值</span><span class="sxs-lookup"><span data-stu-id="d218a-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d218a-120">標頭</span><span class="sxs-lookup"><span data-stu-id="d218a-120">Header</span></span><br/> | <dl> <span data-ttu-id="d218a-121"><dt>Wxdebug (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d218a-121"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d218a-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d218a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d218a-123">指標驗證宏</span><span class="sxs-lookup"><span data-stu-id="d218a-123">Pointer Validation Macros</span></span>](pointer-validation-macros.md)
</dt> </dl>

 

 




