---
description: ID3DXConstantTable：： SetInt 方法：設定整數值。
ms.assetid: b57d30b5-c2b5-469e-a267-24e6e712d645
title: 'ID3DXConstantTable：： SetInt 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetInt
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f218a0cd1a0e1858f24ec8cbccb4848c37121086
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115126"
---
# <a name="id3dxconstanttablesetint-method"></a><span data-ttu-id="6b1d8-103">ID3DXConstantTable：： SetInt 方法</span><span class="sxs-lookup"><span data-stu-id="6b1d8-103">ID3DXConstantTable::SetInt method</span></span>

<span data-ttu-id="6b1d8-104">設定整數值。</span><span class="sxs-lookup"><span data-stu-id="6b1d8-104">Sets an integer value.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b1d8-105">語法</span><span class="sxs-lookup"><span data-stu-id="6b1d8-105">Syntax</span></span>


```C++
HRESULT SetInt(
  [in] LPDIRECT3DDEVICE9 pDevice,
  [in] D3DXHANDLE        hConstant,
  [in] INT               n
);
```



## <a name="parameters"></a><span data-ttu-id="6b1d8-106">參數</span><span class="sxs-lookup"><span data-stu-id="6b1d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b1d8-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6b1d8-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b1d8-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="6b1d8-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="6b1d8-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，表示與常數資料表相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="6b1d8-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="6b1d8-110">*hConstant* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6b1d8-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b1d8-111">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="6b1d8-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="6b1d8-112">常數的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="6b1d8-112">Unique identifier to the constant.</span></span> <span data-ttu-id="6b1d8-113">請參閱 [D3DXHANDLE](dx9-graphics-reference-effects-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="6b1d8-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="6b1d8-114">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b1d8-114">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b1d8-115">類型： **[ **INT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6b1d8-115">Type: **[**INT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6b1d8-116">整數。</span><span class="sxs-lookup"><span data-stu-id="6b1d8-116">Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b1d8-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="6b1d8-117">Return value</span></span>

<span data-ttu-id="6b1d8-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6b1d8-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6b1d8-119">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="6b1d8-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6b1d8-120">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="6b1d8-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b1d8-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="6b1d8-121">Requirements</span></span>



| <span data-ttu-id="6b1d8-122">需求</span><span class="sxs-lookup"><span data-stu-id="6b1d8-122">Requirement</span></span> | <span data-ttu-id="6b1d8-123">值</span><span class="sxs-lookup"><span data-stu-id="6b1d8-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b1d8-124">標頭</span><span class="sxs-lookup"><span data-stu-id="6b1d8-124">Header</span></span><br/>  | <dl> <span data-ttu-id="6b1d8-125"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="6b1d8-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="6b1d8-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="6b1d8-126">Library</span></span><br/> | <dl> <span data-ttu-id="6b1d8-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6b1d8-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="6b1d8-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6b1d8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b1d8-129">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="6b1d8-129">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
