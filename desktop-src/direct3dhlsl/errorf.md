---
title: errorf 函式
description: 將錯誤訊息提交至資訊佇列。
ms.assetid: bf4dc6dc-b36e-4b71-ad61-b7a5ba332879
keywords:
- errorf 函式 HLSL
topic_type:
- apiref
api_name:
- errorf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 76c8fbcd9b6cb15dbbb735296a3aada8f5e568cb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022336"
---
# <a name="errorf-function"></a><span data-ttu-id="1797e-104">errorf 函式</span><span class="sxs-lookup"><span data-stu-id="1797e-104">errorf function</span></span>

<span data-ttu-id="1797e-105">將錯誤訊息提交至資訊佇列。</span><span class="sxs-lookup"><span data-stu-id="1797e-105">Submits an error message to the information queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="1797e-106">語法</span><span class="sxs-lookup"><span data-stu-id="1797e-106">Syntax</span></span>

``` syntax
void errorf(
   string format,
    argument ...
);
```

## <a name="parameters"></a><span data-ttu-id="1797e-107">參數</span><span class="sxs-lookup"><span data-stu-id="1797e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1797e-108">*format*</span><span class="sxs-lookup"><span data-stu-id="1797e-108">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="1797e-109">格式字串。</span><span class="sxs-lookup"><span data-stu-id="1797e-109">The format string.</span></span>

</dd> <dt>

<span data-ttu-id="1797e-110">*參數。。。*</span><span class="sxs-lookup"><span data-stu-id="1797e-110">*argument ...*</span></span> 
</dt> <dd>

<span data-ttu-id="1797e-111">選擇性引數。</span><span class="sxs-lookup"><span data-stu-id="1797e-111">Optional arguments.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1797e-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="1797e-112">Return value</span></span>

<span data-ttu-id="1797e-113">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="1797e-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1797e-114">備註</span><span class="sxs-lookup"><span data-stu-id="1797e-114">Remarks</span></span>

<span data-ttu-id="1797e-115">此作業不會在不支援的裝置上執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="1797e-115">This operation does nothing on devices that do not support it.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="1797e-116">最小著色器模型</span><span class="sxs-lookup"><span data-stu-id="1797e-116">Minimum Shader Model</span></span>

<span data-ttu-id="1797e-117">下列著色器模型支援此函數。</span><span class="sxs-lookup"><span data-stu-id="1797e-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1797e-118">著色器模型</span><span class="sxs-lookup"><span data-stu-id="1797e-118">Shader Model</span></span>                                                        | <span data-ttu-id="1797e-119">支援</span><span class="sxs-lookup"><span data-stu-id="1797e-119">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| [<span data-ttu-id="1797e-120">著色器模型 4 (DirectX HLSL) 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="1797e-120">Shader Model 4 (DirectX HLSL) or later.</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1797e-121">是</span><span class="sxs-lookup"><span data-stu-id="1797e-121">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1797e-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1797e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1797e-123">內建函式</span><span class="sxs-lookup"><span data-stu-id="1797e-123">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 




