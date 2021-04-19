---
description: 設定浮點數。
ms.assetid: 920cbcf2-ccb9-4533-abbc-6bab8b159ebe
title: 'ID3DXConstantTable：： SetFloat 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetFloat
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5048f08acc470e5244de80f4e5618c7416bc1bbf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982211"
---
# <a name="id3dxconstanttablesetfloat-method"></a><span data-ttu-id="5821e-103">ID3DXConstantTable：： SetFloat 方法</span><span class="sxs-lookup"><span data-stu-id="5821e-103">ID3DXConstantTable::SetFloat method</span></span>

<span data-ttu-id="5821e-104">設定浮點數。</span><span class="sxs-lookup"><span data-stu-id="5821e-104">Sets a floating-point number.</span></span>

## <a name="syntax"></a><span data-ttu-id="5821e-105">語法</span><span class="sxs-lookup"><span data-stu-id="5821e-105">Syntax</span></span>


```C++
HRESULT SetFloat(
  [in] LPDIRECT3DDEVICE9 pDevice,
  [in] D3DXHANDLE        hConstant,
  [in] FLOAT             f
);
```



## <a name="parameters"></a><span data-ttu-id="5821e-106">參數</span><span class="sxs-lookup"><span data-stu-id="5821e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5821e-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5821e-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5821e-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="5821e-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="5821e-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，表示與常數資料表相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="5821e-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> <dt>

<span data-ttu-id="5821e-110">*hConstant* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5821e-110">*hConstant* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5821e-111">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="5821e-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="5821e-112">常數的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="5821e-112">Unique identifier to the constant.</span></span> <span data-ttu-id="5821e-113">請參閱 [D3DXHANDLE](dx9-graphics-reference-effects-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="5821e-113">See [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="5821e-114">*f* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5821e-114">*f* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5821e-115">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5821e-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5821e-116">浮點數。</span><span class="sxs-lookup"><span data-stu-id="5821e-116">Floating-point number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5821e-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="5821e-117">Return value</span></span>

<span data-ttu-id="5821e-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5821e-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5821e-119">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="5821e-119">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5821e-120">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="5821e-120">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="5821e-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="5821e-121">Requirements</span></span>



| <span data-ttu-id="5821e-122">需求</span><span class="sxs-lookup"><span data-stu-id="5821e-122">Requirement</span></span> | <span data-ttu-id="5821e-123">值</span><span class="sxs-lookup"><span data-stu-id="5821e-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5821e-124">標頭</span><span class="sxs-lookup"><span data-stu-id="5821e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="5821e-125"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="5821e-125"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="5821e-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="5821e-126">Library</span></span><br/> | <dl> <span data-ttu-id="5821e-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5821e-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5821e-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5821e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5821e-129">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="5821e-129">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
