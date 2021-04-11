---
title: IEnumTfRenderingMarkup Next 方法
description: IEnumTfRenderingMarkup Next 方法會從目前位置取得列舉順序中指定的專案數。
ms.assetid: a3aec919-2c65-4e65-9430-d73fdaf5d28e
keywords:
- Next 方法文字服務架構
- Next 方法文字服務架構，IEnumTfRenderingMarkup 介面
- IEnumTfRenderingMarkup 介面文字服務架構、Next 方法
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup.Next
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0989d35a2fa7c521d5ea103fbe40a73d012a3997
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023725"
---
# <a name="ienumtfrenderingmarkupnext-method"></a><span data-ttu-id="ba5cd-106">IEnumTfRenderingMarkup：： Next 方法</span><span class="sxs-lookup"><span data-stu-id="ba5cd-106">IEnumTfRenderingMarkup::Next method</span></span>

<span data-ttu-id="ba5cd-107">**IEnumTfRenderingMarkup：： Next** 方法會從目前位置取得列舉順序中指定的元素數目。</span><span class="sxs-lookup"><span data-stu-id="ba5cd-107">The **IEnumTfRenderingMarkup::Next** method obtains, from the current position, the specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba5cd-108">語法</span><span class="sxs-lookup"><span data-stu-id="ba5cd-108">Syntax</span></span>


```C++
HRESULT Next(
  [out] ULONG ulCount,
  [out]       ppElement,
  [out] ULONG *pcFetched
);
```



## <a name="parameters"></a><span data-ttu-id="ba5cd-109">參數</span><span class="sxs-lookup"><span data-stu-id="ba5cd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba5cd-110">*ulCount* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ba5cd-110">*ulCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba5cd-111">\[out \] 指定要取得的元素數目。</span><span class="sxs-lookup"><span data-stu-id="ba5cd-111">\[out\] Specifies the number of elements to obtain.</span></span>

</dd> <dt>

<span data-ttu-id="ba5cd-112">*ppElement* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ba5cd-112">*ppElement* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba5cd-113">\[\] [TF \_ RENDERINGMARKUP](/windows/desktop/TSF/tf-renderingmarkup)結構陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="ba5cd-113">\[out\] Pointer to an array of [TF\_RENDERINGMARKUP](/windows/desktop/TSF/tf-renderingmarkup) structures.</span></span> <span data-ttu-id="ba5cd-114">此陣列的大小必須至少為 *ulCount* 元素。</span><span class="sxs-lookup"><span data-stu-id="ba5cd-114">This array must be at least *ulCount* elements in size.</span></span>

</dd> <dt>

<span data-ttu-id="ba5cd-115">*pcFetched* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ba5cd-115">*pcFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba5cd-116">\[指向 \] ULONG 值的指標，此值會接收實際取得的元素數目。</span><span class="sxs-lookup"><span data-stu-id="ba5cd-116">\[out\] Pointer to a ULONG value that receives the number of elements actually obtained.</span></span> <span data-ttu-id="ba5cd-117">這個值可能小於所要求的專案數。</span><span class="sxs-lookup"><span data-stu-id="ba5cd-117">This value can be less than the number of items requested.</span></span> <span data-ttu-id="ba5cd-118">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="ba5cd-118">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba5cd-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="ba5cd-119">Return value</span></span>

<span data-ttu-id="ba5cd-120">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="ba5cd-120">This method can return one of these values.</span></span>



| <span data-ttu-id="ba5cd-121">值</span><span class="sxs-lookup"><span data-stu-id="ba5cd-121">Value</span></span>                                                                                        | <span data-ttu-id="ba5cd-122">描述</span><span class="sxs-lookup"><span data-stu-id="ba5cd-122">Description</span></span>                                                                                                         |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ba5cd-123"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="ba5cd-123"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="ba5cd-124">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="ba5cd-124">The method was successful.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="ba5cd-125"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="ba5cd-125"><dt>**S\_FALSE**</dt></span></span> </dl>      | <span data-ttu-id="ba5cd-126">方法在取得指定數目的元素之前，已到達列舉的結尾。</span><span class="sxs-lookup"><span data-stu-id="ba5cd-126">The method reached the end of the enumeration before the specified number of elements could be obtained.</span></span><br/> |
| <dl> <span data-ttu-id="ba5cd-127"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ba5cd-127"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="ba5cd-128">一或多個參數無效。</span><span class="sxs-lookup"><span data-stu-id="ba5cd-128">One or more parameters are invalid.</span></span><br/>                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="ba5cd-129">備註</span><span class="sxs-lookup"><span data-stu-id="ba5cd-129">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ba5cd-130">這個方法目前不在公用標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="ba5cd-130">This method is not currently in the public header files.</span></span> <span data-ttu-id="ba5cd-131">若要使用此 API，您必須 MIDL 編譯 [原型](prototypes.md)。</span><span class="sxs-lookup"><span data-stu-id="ba5cd-131">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 

