---
description: 取得技術的控制碼。
ms.assetid: da139706-734b-4d5e-896d-52f045942218
title: 'ID3DXBaseEffect：： GetTechnique 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 4f0c82c301a48eb939d182062240c4dba6d3fc63
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116289"
---
# <a name="id3dxbaseeffectgettechnique-method"></a><span data-ttu-id="0d6a0-103">ID3DXBaseEffect：： GetTechnique 方法</span><span class="sxs-lookup"><span data-stu-id="0d6a0-103">ID3DXBaseEffect::GetTechnique method</span></span>

<span data-ttu-id="0d6a0-104">取得技術的控制碼。</span><span class="sxs-lookup"><span data-stu-id="0d6a0-104">Gets the handle of a technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d6a0-105">語法</span><span class="sxs-lookup"><span data-stu-id="0d6a0-105">Syntax</span></span>


```C++
D3DXHANDLE GetTechnique(
  [in] UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="0d6a0-106">參數</span><span class="sxs-lookup"><span data-stu-id="0d6a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d6a0-107">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0d6a0-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d6a0-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0d6a0-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0d6a0-109">技術索引。</span><span class="sxs-lookup"><span data-stu-id="0d6a0-109">Technique index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d6a0-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="0d6a0-110">Return value</span></span>

<span data-ttu-id="0d6a0-111">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="0d6a0-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="0d6a0-112">傳回指定之技術的控制碼，如果索引無效，則 **為 Null** 。</span><span class="sxs-lookup"><span data-stu-id="0d6a0-112">Returns the handle of the specified technique, or **NULL** if the index was invalid.</span></span> <span data-ttu-id="0d6a0-113">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="0d6a0-113">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0d6a0-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d6a0-114">Requirements</span></span>



| <span data-ttu-id="0d6a0-115">需求</span><span class="sxs-lookup"><span data-stu-id="0d6a0-115">Requirement</span></span> | <span data-ttu-id="0d6a0-116">值</span><span class="sxs-lookup"><span data-stu-id="0d6a0-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d6a0-117">標頭</span><span class="sxs-lookup"><span data-stu-id="0d6a0-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0d6a0-118"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="0d6a0-118"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="0d6a0-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="0d6a0-119">Library</span></span><br/> | <dl> <span data-ttu-id="0d6a0-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d6a0-120"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="0d6a0-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d6a0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d6a0-122">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="0d6a0-122">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
