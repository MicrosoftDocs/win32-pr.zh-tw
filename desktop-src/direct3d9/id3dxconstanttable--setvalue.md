---
description: 將緩衝區的內容設定為常數資料表。
ms.assetid: 6058795c-fa32-42aa-9a36-af0b7f6eed1d
title: 'ID3DXConstantTable：： SetValue 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetValue
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e5e02c43e0d0ad84615650bc0b1c0d5fd5654e38
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982016"
---
# <a name="id3dxconstanttablesetvalue-method"></a><span data-ttu-id="a90a8-103">ID3DXConstantTable：： SetValue 方法</span><span class="sxs-lookup"><span data-stu-id="a90a8-103">ID3DXConstantTable::SetValue method</span></span>

<span data-ttu-id="a90a8-104">將緩衝區的內容設定為常數資料表。</span><span class="sxs-lookup"><span data-stu-id="a90a8-104">Sets the contents of the buffer to the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="a90a8-105">語法</span><span class="sxs-lookup"><span data-stu-id="a90a8-105">Syntax</span></span>


```C++
HRESULT SetValue(
  [in] LPDIRECT3DDEVICE9 pDevice,
  [in] D3DXHANDLE        hConstant,
  [in] LPCVOID           pData,
  [in] UINT              Bytes
);
```



## <a name="parameters"></a><span data-ttu-id="a90a8-106">參數</span><span class="sxs-lookup"><span data-stu-id="a90a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a90a8-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a90a8-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a90a8-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="a90a8-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="a90a8-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，表示與常數資料表相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="a90a8-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="a90a8-110">*hConstant* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a90a8-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a90a8-111">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="a90a8-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="a90a8-112">常數的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="a90a8-112">Unique identifier to a constant.</span></span> <span data-ttu-id="a90a8-113">請參閱 [D3DXHANDLE](dx9-graphics-reference-effects-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="a90a8-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="a90a8-114">*.pdata* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a90a8-114">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a90a8-115">類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a90a8-115">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a90a8-116">包含資料的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="a90a8-116">Buffer containing data.</span></span>

</dd> <dt>

<span data-ttu-id="a90a8-117">*位元組* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a90a8-117">*Bytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a90a8-118">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a90a8-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a90a8-119">緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a90a8-119">Size of the buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a90a8-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="a90a8-120">Return value</span></span>

<span data-ttu-id="a90a8-121">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a90a8-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a90a8-122">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="a90a8-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a90a8-123">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="a90a8-123">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="a90a8-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="a90a8-124">Requirements</span></span>



| <span data-ttu-id="a90a8-125">需求</span><span class="sxs-lookup"><span data-stu-id="a90a8-125">Requirement</span></span> | <span data-ttu-id="a90a8-126">值</span><span class="sxs-lookup"><span data-stu-id="a90a8-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a90a8-127">標頭</span><span class="sxs-lookup"><span data-stu-id="a90a8-127">Header</span></span><br/>  | <dl> <span data-ttu-id="a90a8-128"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="a90a8-128"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="a90a8-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="a90a8-129">Library</span></span><br/> | <dl> <span data-ttu-id="a90a8-130"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a90a8-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="a90a8-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a90a8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a90a8-132">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="a90a8-132">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
