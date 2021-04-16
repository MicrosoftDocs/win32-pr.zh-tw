---
description: 常數資料表的描述。
ms.assetid: 848b328a-95a4-4fd0-a7d4-4fb0e5d14f64
title: 'D3DXCONSTANTTABLE_DESC 結構 (D3dx9shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCONSTANTTABLE_DESC
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 7c53023952518182f68cf4a671ec47c6056a92a6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696675"
---
# <a name="d3dxconstanttable_desc-structure"></a><span data-ttu-id="194cd-103">D3DXCONSTANTTABLE \_ DESC 結構</span><span class="sxs-lookup"><span data-stu-id="194cd-103">D3DXCONSTANTTABLE\_DESC structure</span></span>

<span data-ttu-id="194cd-104">常數資料表的描述。</span><span class="sxs-lookup"><span data-stu-id="194cd-104">A description of the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="194cd-105">語法</span><span class="sxs-lookup"><span data-stu-id="194cd-105">Syntax</span></span>


```C++
typedef struct D3DXCONSTANTTABLE_DESC {
  LPCSTR Creator;
  DWORD  Version;
  UINT   Constants;
} D3DXCONSTANTTABLE_DESC, *LPD3DXCONSTANTTABLE_DESC;
```



## <a name="members"></a><span data-ttu-id="194cd-106">成員</span><span class="sxs-lookup"><span data-stu-id="194cd-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="194cd-107">**建立者**</span><span class="sxs-lookup"><span data-stu-id="194cd-107">**Creator**</span></span>
</dt> <dd>

<span data-ttu-id="194cd-108">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="194cd-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="194cd-109">常數資料表建立者的名稱。</span><span class="sxs-lookup"><span data-stu-id="194cd-109">Name of the constant table creator.</span></span>

</dd> <dt>

<span data-ttu-id="194cd-110">**版本**</span><span class="sxs-lookup"><span data-stu-id="194cd-110">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="194cd-111">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="194cd-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="194cd-112">著色器版本。</span><span class="sxs-lookup"><span data-stu-id="194cd-112">Shader version.</span></span>

</dd> <dt>

<span data-ttu-id="194cd-113">**常數**</span><span class="sxs-lookup"><span data-stu-id="194cd-113">**Constants**</span></span>
</dt> <dd>

<span data-ttu-id="194cd-114">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="194cd-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="194cd-115">常數資料表中的常數數目。</span><span class="sxs-lookup"><span data-stu-id="194cd-115">Number of constants in the constant table.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="194cd-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="194cd-116">Requirements</span></span>



| <span data-ttu-id="194cd-117">需求</span><span class="sxs-lookup"><span data-stu-id="194cd-117">Requirement</span></span> | <span data-ttu-id="194cd-118">值</span><span class="sxs-lookup"><span data-stu-id="194cd-118">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="194cd-119">標頭</span><span class="sxs-lookup"><span data-stu-id="194cd-119">Header</span></span><br/> | <dl> <span data-ttu-id="194cd-120"><dt>D3dx9shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="194cd-120"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="194cd-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="194cd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="194cd-122">D3DX 結構</span><span class="sxs-lookup"><span data-stu-id="194cd-122">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="194cd-123">**D3DXCONSTANT \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="194cd-123">**D3DXCONSTANT\_DESC**</span></span>](d3dxconstant-desc.md)
</dt> </dl>

 

 
