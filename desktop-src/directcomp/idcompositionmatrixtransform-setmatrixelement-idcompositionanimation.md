---
title: IDCompositionMatrixTransform SetMatrixElement (int，int，IDCompositionAnimation ) 方法
description: 將這個2D 轉換之矩陣的某個元素值繪製成動畫。
ms.assetid: 16A9E136-5F0C-4F34-A127-BF06C4530499
keywords:
- SetMatrixElement 方法 DirectComposition
- SetMatrixElement 方法 DirectComposition、IDCompositionMatrixTransform 介面
- IDCompositionMatrixTransform 介面 DirectComposition，SetMatrixElement 方法
topic_type:
- apiref
api_name:
- IDCompositionMatrixTransform.SetMatrixElement
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5b4bf2a43e762b85b8b8cfd0c15468b3dc438221
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376181"
---
# <a name="idcompositionmatrixtransformsetmatrixelementint-int-idcompositionanimation-method"></a><span data-ttu-id="c5185-106">IDCompositionMatrixTransform：： SetMatrixElement (int，int，IDCompositionAnimation \*) 方法</span><span class="sxs-lookup"><span data-stu-id="c5185-106">IDCompositionMatrixTransform::SetMatrixElement(int, int, IDCompositionAnimation\*) method</span></span>

<span data-ttu-id="c5185-107">將這個2D 轉換之矩陣的某個元素值繪製成動畫。</span><span class="sxs-lookup"><span data-stu-id="c5185-107">Animates the value of one element of the matrix of this 2D transform.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5185-108">語法</span><span class="sxs-lookup"><span data-stu-id="c5185-108">Syntax</span></span>


```C++
HRESULT SetMatrixElement(
  [in] int                    row,
  [in] int                    column,
  [in] IDCompositionAnimation *animation
);
```



## <a name="parameters"></a><span data-ttu-id="c5185-109">參數</span><span class="sxs-lookup"><span data-stu-id="c5185-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5185-110">資料 *列* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c5185-110">*row* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5185-111">要變更之元素的資料列索引。</span><span class="sxs-lookup"><span data-stu-id="c5185-111">The row index of the element to change.</span></span> <span data-ttu-id="c5185-112">此值必須介於0和2（含）之間。</span><span class="sxs-lookup"><span data-stu-id="c5185-112">This value must be between 0 and 2, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="c5185-113">資料 *行* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c5185-113">*column* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5185-114">要變更之元素的資料行索引。</span><span class="sxs-lookup"><span data-stu-id="c5185-114">The column index of the element to change.</span></span> <span data-ttu-id="c5185-115">此值必須介於0和1（含）之間。</span><span class="sxs-lookup"><span data-stu-id="c5185-115">This value must be between 0 and 1, inclusive.</span></span>

</dd> <dt>

<span data-ttu-id="c5185-116">*動畫* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c5185-116">*animation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5185-117">表示指定專案的值如何隨著時間而改變的動畫。</span><span class="sxs-lookup"><span data-stu-id="c5185-117">An animation that represents how the value of the specified element changes over time.</span></span> <span data-ttu-id="c5185-118">此參數不得為 Null。</span><span class="sxs-lookup"><span data-stu-id="c5185-118">This parameter must not be NULL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5185-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="c5185-119">Return value</span></span>

<span data-ttu-id="c5185-120">如果函式成功，則會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="c5185-120">If the function succeeds, it returns S\_OK.</span></span> <span data-ttu-id="c5185-121">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c5185-121">Otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="c5185-122">如需錯誤碼清單，請參閱 [DirectComposition 錯誤碼](directcomposition-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="c5185-122">See [DirectComposition Error Codes](directcomposition-error-codes.md) for a list of error codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5185-123">備註</span><span class="sxs-lookup"><span data-stu-id="c5185-123">Remarks</span></span>

<span data-ttu-id="c5185-124">這個方法會複製指定的動畫。</span><span class="sxs-lookup"><span data-stu-id="c5185-124">This method makes a copy of the specified animation.</span></span> <span data-ttu-id="c5185-125">如果在呼叫這個方法之後變更了 *動畫* 參數所參考的物件，除非再次呼叫這個方法，否則變更不會影響元素。</span><span class="sxs-lookup"><span data-stu-id="c5185-125">If the object referenced by the *animation* parameter is changed after calling this method, the change does not affect the element unless this method is called again.</span></span> <span data-ttu-id="c5185-126">如果專案先前是以動畫顯示，呼叫這個方法會以新動畫取代先前的動畫。</span><span class="sxs-lookup"><span data-stu-id="c5185-126">If the element was previously animated, calling this method replaces the previous animation with the new animation.</span></span>

<span data-ttu-id="c5185-127">如果 *動畫* 是不正確指標，或與受影響的轉換不是由相同的 [**IDCompositionDevice**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) 介面所建立，則這個方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="c5185-127">This method fails if *animation* is an invalid pointer or if it was not created by the same [**IDCompositionDevice**](/windows/win32/api/dcomp/nn-dcomp-idcompositiondevice) interface as the affected transform.</span></span> <span data-ttu-id="c5185-128">介面不能是自訂的實值;只有 Microsoft DirectComposition 建立的介面可以搭配此方法使用。</span><span class="sxs-lookup"><span data-stu-id="c5185-128">The interface cannot be a custom implementation; only interfaces created by Microsoft DirectComposition can be used with this method.</span></span>

## <a name="see-also"></a><span data-ttu-id="c5185-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5185-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5185-130">**IDCompositionMatrixTransform**</span><span class="sxs-lookup"><span data-stu-id="c5185-130">**IDCompositionMatrixTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform)
</dt> </dl>

 

 