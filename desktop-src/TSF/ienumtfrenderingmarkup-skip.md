---
title: IEnumTfRenderingMarkup Skip 方法
description: IEnumTfRenderingMarkup Skip 方法會從目前位置取得列舉順序中指定的元素數目。
ms.assetid: d328dfe3-36ab-4daf-8809-ad6686ca5dae
keywords:
- Skip 方法文字服務架構
- Skip 方法文字服務架構，IEnumTfRenderingMarkup 介面
- IEnumTfRenderingMarkup 介面文字服務架構，Skip 方法
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup.Skip
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3542893c739e6cfa2933d95bfed31f16957a0841
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678315"
---
# <a name="ienumtfrenderingmarkupskip-method"></a><span data-ttu-id="42f21-106">IEnumTfRenderingMarkup：： Skip 方法</span><span class="sxs-lookup"><span data-stu-id="42f21-106">IEnumTfRenderingMarkup::Skip method</span></span>

<span data-ttu-id="42f21-107">**IEnumTfRenderingMarkup：： Skip** 方法會從目前位置取得列舉順序中指定的元素數目。</span><span class="sxs-lookup"><span data-stu-id="42f21-107">The **IEnumTfRenderingMarkup::Skip** method obtains, from the current position, the specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="42f21-108">語法</span><span class="sxs-lookup"><span data-stu-id="42f21-108">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG ulCount
);
```



## <a name="parameters"></a><span data-ttu-id="42f21-109">參數</span><span class="sxs-lookup"><span data-stu-id="42f21-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42f21-110">*ulCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="42f21-110">*ulCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42f21-111">\[中的 \] 指定要略過的元素數目。</span><span class="sxs-lookup"><span data-stu-id="42f21-111">\[in\] Specifies the number of elements to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42f21-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="42f21-112">Return value</span></span>

<span data-ttu-id="42f21-113">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="42f21-113">This method can return one of these values.</span></span>



| <span data-ttu-id="42f21-114">值</span><span class="sxs-lookup"><span data-stu-id="42f21-114">Value</span></span>                                                                                   | <span data-ttu-id="42f21-115">描述</span><span class="sxs-lookup"><span data-stu-id="42f21-115">Description</span></span>                                                                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="42f21-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="42f21-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="42f21-117">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="42f21-117">The method was successful.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="42f21-118"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="42f21-118"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="42f21-119">方法在可以略過指定的元素數目之前，已到達列舉的結尾。</span><span class="sxs-lookup"><span data-stu-id="42f21-119">The method reached the end of the enumeration before the specified number of elements could be skipped.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="42f21-120">備註</span><span class="sxs-lookup"><span data-stu-id="42f21-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="42f21-121">這個方法目前不在公用標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="42f21-121">This method is not currently in the public header files.</span></span> <span data-ttu-id="42f21-122">若要使用此 API，您必須 MIDL 編譯 [原型](prototypes.md)。</span><span class="sxs-lookup"><span data-stu-id="42f21-122">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 

 





