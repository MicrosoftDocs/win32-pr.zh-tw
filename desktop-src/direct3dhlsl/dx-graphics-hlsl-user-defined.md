---
title: 使用者自訂類型
description: 使用下列語法來宣告使用者定義型別。
ms.assetid: 8ef18864-f456-4b52-af83-f9b1050a0bba
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2107e3eb2b2dc2362776a1a9ecd50830519c6627
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371986"
---
# <a name="user-defined-type"></a><span data-ttu-id="67205-103">使用者自訂類型</span><span class="sxs-lookup"><span data-stu-id="67205-103">User-Defined Type</span></span>

<span data-ttu-id="67205-104">使用下列語法來宣告使用者定義型別。</span><span class="sxs-lookup"><span data-stu-id="67205-104">Use the following syntax to declare a user-defined type.</span></span>



|                                           |
|-------------------------------------------|
| <span data-ttu-id="67205-105">typedef **\[ const \] 型別 \[ 名稱 \] 索引**;</span><span class="sxs-lookup"><span data-stu-id="67205-105">typedef **\[const\] Type Name\[Index\]**;</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="67205-106">參數</span><span class="sxs-lookup"><span data-stu-id="67205-106">Parameters</span></span>



| <span data-ttu-id="67205-107">項目</span><span class="sxs-lookup"><span data-stu-id="67205-107">Item</span></span>                                                                                         | <span data-ttu-id="67205-108">描述</span><span class="sxs-lookup"><span data-stu-id="67205-108">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="67205-109"><span id="_const_"></span><span id="_CONST_"></span>**\[常量\]**</span><span class="sxs-lookup"><span data-stu-id="67205-109"><span id="_const_"></span><span id="_CONST_"></span>**\[const\]**</span></span><br/>                 | <span data-ttu-id="67205-110">選擇性。</span><span class="sxs-lookup"><span data-stu-id="67205-110">Optional.</span></span> <span data-ttu-id="67205-111">此關鍵字會將類型明確標示為常數。</span><span class="sxs-lookup"><span data-stu-id="67205-111">This keyword explicitly marks the type as a constant.</span></span><br/>             |
| <span data-ttu-id="67205-112"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**類型**</span><span class="sxs-lookup"><span data-stu-id="67205-112"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Type**</span></span><br/>     | <span data-ttu-id="67205-113">識別資料類型;必須是其中一個 HLSL 內建資料類型。</span><span class="sxs-lookup"><span data-stu-id="67205-113">Identifies the data type; must be one of the HLSL intrinsic data types.</span></span><br/>     |
| <span data-ttu-id="67205-114"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**名字**</span><span class="sxs-lookup"><span data-stu-id="67205-114"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="67205-115">可唯一識別變數名稱的 ASCII 字串。</span><span class="sxs-lookup"><span data-stu-id="67205-115">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="67205-116"><span id="Index"></span><span id="index"></span><span id="INDEX"></span>**指數**</span><span class="sxs-lookup"><span data-stu-id="67205-116"><span id="Index"></span><span id="index"></span><span id="INDEX"></span>**Index**</span></span><br/> | <span data-ttu-id="67205-117">選擇性陣列大小。</span><span class="sxs-lookup"><span data-stu-id="67205-117">Optional array size.</span></span> <span data-ttu-id="67205-118">必須是介於1到4（含）之間的不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="67205-118">Must be an unsigned integer between 1 and 4 inclusive.</span></span><br/> |



 

<span data-ttu-id="67205-119">除了內建的內建資料類型，HLSL 還支援遵循下列語法的使用者定義或自訂類型：</span><span class="sxs-lookup"><span data-stu-id="67205-119">In addition to the built-in intrinsic data types, HLSL supports user-defined or custom types which follow this syntax:</span></span>

## <a name="remarks"></a><span data-ttu-id="67205-120">備註</span><span class="sxs-lookup"><span data-stu-id="67205-120">Remarks</span></span>

<span data-ttu-id="67205-121">使用者定義類型不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="67205-121">User-defined types are not case-sensitive.</span></span> <span data-ttu-id="67205-122">為了方便起見，下列類型會自動定義在超級全域範圍中。</span><span class="sxs-lookup"><span data-stu-id="67205-122">For convenience, the following types are automatically defined at super-global scope.</span></span>


```
typedef vector <bool, #> bool#;
typedef vector <int, #> int#;
typedef vector <uint, #> uint#;
typedef vector <half, #> half#;
typedef vector <float, #> float#;
typedef vector <double, #> double#;

typedef matrix <bool, #, #> bool#x#;
typedef matrix <int, #, #> int#x#;
typedef matrix <uint, #, #> uint#x#;
typedef matrix <half, #, #> half#x#;
typedef matrix <float, #, #> float#x#;
typedef matrix <double, #, #> double#x#;
```



<span data-ttu-id="67205-123">井字型大小 (\#) 代表介於1到4之間的整數數位。</span><span class="sxs-lookup"><span data-stu-id="67205-123">The pound sign (\#) represents an integer digit between 1 and 4.</span></span>

<span data-ttu-id="67205-124">為了與 DirectX 8 效果相容，下列類型會自動定義在超級全域範圍內：</span><span class="sxs-lookup"><span data-stu-id="67205-124">For compatibility with DirectX 8 effects, the following types are automatically defined at super-global scope:</span></span>


```
typedef int DWORD;
typedef float FLOAT; 
typedef vector <float, 4> VECTOR;
typedef matrix <float, 4, 4> MATRIX;
typedef string STRING;
typedef texture TEXTURE;
typedef pixelshader PIXELSHADER;
typedef vertexshader VERTEXSHADER;
```



## <a name="related-topics"></a><span data-ttu-id="67205-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="67205-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67205-126"> (DirectX HLSL) 的資料類型 </span><span class="sxs-lookup"><span data-stu-id="67205-126">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





