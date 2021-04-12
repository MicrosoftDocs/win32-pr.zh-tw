---
description: 藉由查詢名稱來取得函數的控制碼。
ms.assetid: 1e2e2dae-5084-47f3-9812-3dbf609bd70b
title: 'ID3DXBaseEffect：： GetFunctionByName 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFunctionByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e1cd9ec56ff5df3bff293ade0669b4cd7c8dad5d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323340"
---
# <a name="id3dxbaseeffectgetfunctionbyname-method"></a><span data-ttu-id="e277f-103">ID3DXBaseEffect：： GetFunctionByName 方法</span><span class="sxs-lookup"><span data-stu-id="e277f-103">ID3DXBaseEffect::GetFunctionByName method</span></span>

<span data-ttu-id="e277f-104">藉由查詢名稱來取得函數的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e277f-104">Gets the handle of a function by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="e277f-105">語法</span><span class="sxs-lookup"><span data-stu-id="e277f-105">Syntax</span></span>


```C++
D3DXHANDLE GetFunctionByName(
  [in] LPCSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="e277f-106">參數</span><span class="sxs-lookup"><span data-stu-id="e277f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e277f-107">*pName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e277f-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e277f-108">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e277f-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e277f-109">包含函式名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="e277f-109">String containing the function name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e277f-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="e277f-110">Return value</span></span>

<span data-ttu-id="e277f-111">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="e277f-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="e277f-112">傳回指定之函數的控制碼，如果找不到名稱，則 **為 Null** 。</span><span class="sxs-lookup"><span data-stu-id="e277f-112">Returns the handle of the specified function, or **NULL** if the name was not found.</span></span> <span data-ttu-id="e277f-113">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="e277f-113">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e277f-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="e277f-114">Requirements</span></span>



| <span data-ttu-id="e277f-115">需求</span><span class="sxs-lookup"><span data-stu-id="e277f-115">Requirement</span></span> | <span data-ttu-id="e277f-116">值</span><span class="sxs-lookup"><span data-stu-id="e277f-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e277f-117">標頭</span><span class="sxs-lookup"><span data-stu-id="e277f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e277f-118"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="e277f-118"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="e277f-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="e277f-119">Library</span></span><br/> | <dl> <span data-ttu-id="e277f-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e277f-120"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e277f-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e277f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e277f-122">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="e277f-122">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
