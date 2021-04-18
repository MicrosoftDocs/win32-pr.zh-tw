---
title: '向量類型 (HLSL) '
description: 向量包含一到四個純量元件;向量的每個元件都必須是相同的類型。
ms.assetid: 16e66f3c-c513-4d03-8adf-463dc8d83e12
keywords:
- 向量類型 HLSL
topic_type:
- apiref
api_name:
- Vector Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76d07da5d22dfb44215f70a7620d6519b5c8a802
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "104991854"
---
# <a name="vector-type"></a><span data-ttu-id="23550-104">向量類型</span><span class="sxs-lookup"><span data-stu-id="23550-104">Vector Type</span></span>

<span data-ttu-id="23550-105">向量包含一到四個純量元件;向量的每個元件都必須是相同的類型。</span><span class="sxs-lookup"><span data-stu-id="23550-105">A vector contains between one and four scalar components; every component of a vector must be of the same type.</span></span>



|                     |
|---------------------|
| <span data-ttu-id="23550-106">**TypeNumber 名稱**</span><span class="sxs-lookup"><span data-stu-id="23550-106">**TypeNumber Name**</span></span> |



 


```
TypeComponents Name
```



## <a name="components"></a><span data-ttu-id="23550-107">單元</span><span class="sxs-lookup"><span data-stu-id="23550-107">Components</span></span>



| <span data-ttu-id="23550-108">項目</span><span class="sxs-lookup"><span data-stu-id="23550-108">Item</span></span>                                                                                                                             | <span data-ttu-id="23550-109">描述</span><span class="sxs-lookup"><span data-stu-id="23550-109">Description</span></span>                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23550-110"><span id="TypeComponents"></span><span id="typecomponents"></span><span id="TYPECOMPONENTS"></span>**TypeComponents**</span><span class="sxs-lookup"><span data-stu-id="23550-110"><span id="TypeComponents"></span><span id="typecomponents"></span><span id="TYPECOMPONENTS"></span>**TypeComponents**</span></span><br/> | <span data-ttu-id="23550-111">包含兩個部分的單一名稱。</span><span class="sxs-lookup"><span data-stu-id="23550-111">A single name that contains two parts.</span></span> <span data-ttu-id="23550-112">第一個部分是純 [量類型的](dx-graphics-hlsl-data-types.md) 其中一個。</span><span class="sxs-lookup"><span data-stu-id="23550-112">The first part is one of the [scalar](dx-graphics-hlsl-data-types.md) types.</span></span> <span data-ttu-id="23550-113">第二個部分是元件的數目，必須介於1到4（含）之間。</span><span class="sxs-lookup"><span data-stu-id="23550-113">The second part is the number of components, which must be between 1 and 4 inclusive.</span></span><br/> |
| <span data-ttu-id="23550-114"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**名字**</span><span class="sxs-lookup"><span data-stu-id="23550-114"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>                                         | <span data-ttu-id="23550-115">可唯一識別變數名稱的 ASCII 字串。</span><span class="sxs-lookup"><span data-stu-id="23550-115">An ASCII string that uniquely identifies the variable name.</span></span><br/>                                                                                                                                                |



 

## <a name="examples"></a><span data-ttu-id="23550-116">範例</span><span class="sxs-lookup"><span data-stu-id="23550-116">Examples</span></span>

<span data-ttu-id="23550-117">以下是一些範例：</span><span class="sxs-lookup"><span data-stu-id="23550-117">Here are some examples:</span></span>


```
bool    bVector;   // scalar containing 1 Boolean
int1    iVector = 1;
float3  fVector = { 0.2f, 0.3f, 0.4f };
```



<span data-ttu-id="23550-118">您也可以使用此語法來宣告向量：</span><span class="sxs-lookup"><span data-stu-id="23550-118">A vector can be declared using this syntax also:</span></span>


```
vector <Type, Number> VariableName
```



<span data-ttu-id="23550-119">以下是一些範例：</span><span class="sxs-lookup"><span data-stu-id="23550-119">Here are some examples:</span></span>


```
vector <int,    1> iVector = 1;
vector <double, 4> dVector = { 0.2, 0.3, 0.4, 0.5 };
```

## <a name="see-also"></a><span data-ttu-id="23550-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="23550-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23550-121"> (DirectX HLSL) 的資料類型 </span><span class="sxs-lookup"><span data-stu-id="23550-121">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





