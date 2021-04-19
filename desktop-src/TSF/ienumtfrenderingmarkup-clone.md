---
title: IEnumTfRenderingMarkup Clone 方法
description: IEnumTfRenderingMarkup Clone 方法會建立枚舉器物件的複本。
ms.assetid: f1b0ccf9-36d1-4eff-af7c-d7fb4f0e9104
keywords:
- Clone 方法文字服務架構
- Clone 方法文字服務架構，IEnumTfRenderingMarkup 介面
- IEnumTfRenderingMarkup 介面文字服務架構，Clone 方法
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup.Clone
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f15d1bda18d2371f6518da4fa2884fac4df91b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106979669"
---
# <a name="ienumtfrenderingmarkupclone-method"></a><span data-ttu-id="07813-106">IEnumTfRenderingMarkup：： Clone 方法</span><span class="sxs-lookup"><span data-stu-id="07813-106">IEnumTfRenderingMarkup::Clone method</span></span>

<span data-ttu-id="07813-107">**IEnumTfRenderingMarkup：： Clone** 方法會建立枚舉器物件的複本。</span><span class="sxs-lookup"><span data-stu-id="07813-107">The **IEnumTfRenderingMarkup::Clone** method creates a copy of the enumerator object.</span></span>

## <a name="syntax"></a><span data-ttu-id="07813-108">語法</span><span class="sxs-lookup"><span data-stu-id="07813-108">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumTfRenderingMarkup **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="07813-109">參數</span><span class="sxs-lookup"><span data-stu-id="07813-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07813-110">*ppEnum* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="07813-110">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07813-111">\[\] [IEnumTfRenderingMarkup](/windows/desktop/TSF/ienumtfrenderingmarkup)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="07813-111">\[out\] A pointer to a [IEnumTfRenderingMarkup](/windows/desktop/TSF/ienumtfrenderingmarkup) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07813-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="07813-112">Return value</span></span>

<span data-ttu-id="07813-113">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="07813-113">This method can return one of these values.</span></span>



| <span data-ttu-id="07813-114">值</span><span class="sxs-lookup"><span data-stu-id="07813-114">Value</span></span>                                                                                        | <span data-ttu-id="07813-115">描述</span><span class="sxs-lookup"><span data-stu-id="07813-115">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="07813-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="07813-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="07813-117">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="07813-117">The method was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="07813-118"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="07813-118"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="07813-119">發生未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="07813-119">An unspecified error occurred.</span></span><br/>      |
| <dl> <span data-ttu-id="07813-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="07813-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="07813-121">一或多個參數無效。</span><span class="sxs-lookup"><span data-stu-id="07813-121">One or more parameters are invalid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="07813-122">備註</span><span class="sxs-lookup"><span data-stu-id="07813-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="07813-123">這個方法目前不在公用標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="07813-123">This method is not currently in the public header files.</span></span> <span data-ttu-id="07813-124">若要使用此 API，您必須 MIDL 編譯 [原型](prototypes.md)。</span><span class="sxs-lookup"><span data-stu-id="07813-124">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 

