---
description: 描述效果物件所使用的預處理器定義。
ms.assetid: 43413b79-e331-4466-b288-bd4439c135a2
title: 'D3DXMACRO 結構 (D3dx9shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMACRO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 7fd6c52b94c3fb6f36c9b3a8e2b4b513fb8903f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986120"
---
# <a name="d3dxmacro-structure"></a><span data-ttu-id="798c4-103">D3DXMACRO 結構</span><span class="sxs-lookup"><span data-stu-id="798c4-103">D3DXMACRO structure</span></span>

<span data-ttu-id="798c4-104">描述效果物件所使用的預處理器定義。</span><span class="sxs-lookup"><span data-stu-id="798c4-104">Describes preprocessor definitions used by an effect object.</span></span>

## <a name="syntax"></a><span data-ttu-id="798c4-105">語法</span><span class="sxs-lookup"><span data-stu-id="798c4-105">Syntax</span></span>


```C++
typedef struct D3DXMACRO {
  LPCSTR Name;
  LPCSTR Definition;
} D3DXMACRO, *LPD3DXMACRO;
```



## <a name="members"></a><span data-ttu-id="798c4-106">成員</span><span class="sxs-lookup"><span data-stu-id="798c4-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="798c4-107">**名稱**</span><span class="sxs-lookup"><span data-stu-id="798c4-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="798c4-108">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="798c4-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="798c4-109">預處理器名稱。</span><span class="sxs-lookup"><span data-stu-id="798c4-109">Preprocessor name.</span></span>

</dd> <dt>

<span data-ttu-id="798c4-110">**定義**</span><span class="sxs-lookup"><span data-stu-id="798c4-110">**Definition**</span></span>
</dt> <dd>

<span data-ttu-id="798c4-111">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="798c4-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="798c4-112">定義名稱。</span><span class="sxs-lookup"><span data-stu-id="798c4-112">Definition name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="798c4-113">備註</span><span class="sxs-lookup"><span data-stu-id="798c4-113">Remarks</span></span>

<span data-ttu-id="798c4-114">若要在多行中使用 **D3DXMACRO**，請在每一個換行字元前面加上反斜線 (例如 \# C 語言) 中的定義。</span><span class="sxs-lookup"><span data-stu-id="798c4-114">To use **D3DXMACRO** s in more than one line, prefix each new line character with a backslash (like a \#define in the C language).</span></span> <span data-ttu-id="798c4-115">例如：</span><span class="sxs-lookup"><span data-stu-id="798c4-115">For example:</span></span>


```
sample=
macro.Name = "DO_CODE_BLOCK";
macro.Definition =
    "/* here is a block of code */\\\n"
    "{ do something ... }\\\n";
```



<span data-ttu-id="798c4-116">請注意行結尾的3個反斜線字元。</span><span class="sxs-lookup"><span data-stu-id="798c4-116">Notice the 3 backslash characters at the end of the line.</span></span> <span data-ttu-id="798c4-117">前兩個需要輸出單一 ' \\ '，後面接著分行符號 " \\ n"。</span><span class="sxs-lookup"><span data-stu-id="798c4-117">The first two are required to output a single '\\', followed by the newline character "\\n".</span></span> <span data-ttu-id="798c4-118">（選擇性）您也可能想要使用 " \\ \\ \\ r \\ n" 來終止您的行。</span><span class="sxs-lookup"><span data-stu-id="798c4-118">Optionally, you may also want to terminate your lines using "\\\\\\r\\n".</span></span>

## <a name="requirements"></a><span data-ttu-id="798c4-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="798c4-119">Requirements</span></span>



| <span data-ttu-id="798c4-120">需求</span><span class="sxs-lookup"><span data-stu-id="798c4-120">Requirement</span></span> | <span data-ttu-id="798c4-121">值</span><span class="sxs-lookup"><span data-stu-id="798c4-121">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="798c4-122">標頭</span><span class="sxs-lookup"><span data-stu-id="798c4-122">Header</span></span><br/> | <dl> <span data-ttu-id="798c4-123"><dt>D3dx9shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="798c4-123"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="798c4-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="798c4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="798c4-125">效果結構</span><span class="sxs-lookup"><span data-stu-id="798c4-125">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> <dt>

[<span data-ttu-id="798c4-126">**D3DXCreateEffectFromFile**</span><span class="sxs-lookup"><span data-stu-id="798c4-126">**D3DXCreateEffectFromFile**</span></span>](d3dxcreateeffectfromfile.md)
</dt> </dl>

 

 
