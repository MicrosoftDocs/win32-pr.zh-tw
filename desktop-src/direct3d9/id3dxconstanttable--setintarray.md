---
description: 設定整數的陣列。
ms.assetid: 15add9df-966d-45aa-b29c-d4bed2a125f4
title: 'ID3DXConstantTable：： SetIntArray 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetIntArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9f89de7d784ce355570d369606bfa67ddd6f5acf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988190"
---
# <a name="id3dxconstanttablesetintarray-method"></a><span data-ttu-id="11532-103">ID3DXConstantTable：： SetIntArray 方法</span><span class="sxs-lookup"><span data-stu-id="11532-103">ID3DXConstantTable::SetIntArray method</span></span>

<span data-ttu-id="11532-104">設定整數的陣列。</span><span class="sxs-lookup"><span data-stu-id="11532-104">Sets an array of integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="11532-105">語法</span><span class="sxs-lookup"><span data-stu-id="11532-105">Syntax</span></span>


```C++
HRESULT SetIntArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const INT               *pn,
  [in]       UINT              Count
);
```



## <a name="parameters"></a><span data-ttu-id="11532-106">參數</span><span class="sxs-lookup"><span data-stu-id="11532-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11532-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="11532-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11532-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="11532-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="11532-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，表示與常數資料表相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="11532-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="11532-110">*hConstant* \[在\]</span><span class="sxs-lookup"><span data-stu-id="11532-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11532-111">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="11532-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="11532-112">常數陣列的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="11532-112">Unique identifier to the array of constants.</span></span> <span data-ttu-id="11532-113">請參閱 [D3DXHANDLE](dx9-graphics-reference-effects-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="11532-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="11532-114">*pn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="11532-114">*pn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11532-115">類型： **Const [**INT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="11532-115">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="11532-116">整數的陣列。</span><span class="sxs-lookup"><span data-stu-id="11532-116">Array of integers.</span></span>

</dd> <dt>

<span data-ttu-id="11532-117">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="11532-117">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11532-118">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="11532-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="11532-119">陣列中的整數數目。</span><span class="sxs-lookup"><span data-stu-id="11532-119">Number of integers in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11532-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="11532-120">Return value</span></span>

<span data-ttu-id="11532-121">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="11532-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="11532-122">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="11532-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="11532-123">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="11532-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="11532-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="11532-124">Requirements</span></span>



| <span data-ttu-id="11532-125">需求</span><span class="sxs-lookup"><span data-stu-id="11532-125">Requirement</span></span> | <span data-ttu-id="11532-126">值</span><span class="sxs-lookup"><span data-stu-id="11532-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="11532-127">標頭</span><span class="sxs-lookup"><span data-stu-id="11532-127">Header</span></span><br/>  | <dl> <span data-ttu-id="11532-128"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="11532-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="11532-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="11532-129">Library</span></span><br/> | <dl> <span data-ttu-id="11532-130"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="11532-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="11532-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="11532-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11532-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="11532-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
