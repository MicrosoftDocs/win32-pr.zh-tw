---
description: 針對材質物件中的每個材質設定一般向量。 如果) 計算以圖元為基礎的預先計算 radiance 傳輸 (PRT) ，則會使用這個方法來儲存網格 (中的頂點一般向量或插入頂點法線。
ms.assetid: 165a3ef6-c142-4988-b4fb-5aafd8ff11fe
title: 'ID3DXPRTEngine：： SetPerTexelNormal 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetPerTexelNormal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5220ad500312792cd158967e9502381f49b0e3e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386477"
---
# <a name="id3dxprtenginesetpertexelnormal-method"></a><span data-ttu-id="400d8-104">ID3DXPRTEngine：： SetPerTexelNormal 方法</span><span class="sxs-lookup"><span data-stu-id="400d8-104">ID3DXPRTEngine::SetPerTexelNormal method</span></span>

<span data-ttu-id="400d8-105">針對材質物件中的每個材質設定一般向量。</span><span class="sxs-lookup"><span data-stu-id="400d8-105">Sets a normal vector for each texel in a texture object.</span></span> <span data-ttu-id="400d8-106">如果) 計算以圖元為基礎的預先計算 radiance 傳輸 (PRT) ，則會使用這個方法來儲存網格 (中的頂點一般向量或插入頂點法線。</span><span class="sxs-lookup"><span data-stu-id="400d8-106">This method is used to store vertex normal vectors from a mesh (or interpolated vertex normals if pixel-based precomputed radiance transfer (PRT) is being computed).</span></span>

## <a name="syntax"></a><span data-ttu-id="400d8-107">語法</span><span class="sxs-lookup"><span data-stu-id="400d8-107">Syntax</span></span>


```C++
HRESULT SetPerTexelNormal(
  [in] LPDIRECT3DTEXTURE9 pNormalTexture
);
```



## <a name="parameters"></a><span data-ttu-id="400d8-108">參數</span><span class="sxs-lookup"><span data-stu-id="400d8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="400d8-109">*pNormalTexture* \[在\]</span><span class="sxs-lookup"><span data-stu-id="400d8-109">*pNormalTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="400d8-110">類型： **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="400d8-110">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="400d8-111">指向 [**IDirect3DTexture9**](/windows/desktop/api) 材質物件的指標，此物件可作為物件空間一般地圖以用來儲存一般向量。</span><span class="sxs-lookup"><span data-stu-id="400d8-111">Pointer to an [**IDirect3DTexture9**](/windows/desktop/api) texture object that serves as an object space normal map in which to store normal vectors.</span></span> <span data-ttu-id="400d8-112">材質必須具有與 [**ID3DXPRTBuffer**](id3dxprtbuffer.md) 相同的維度，而且必須能夠儲存已簽署的材質格式。</span><span class="sxs-lookup"><span data-stu-id="400d8-112">The texture must have the same dimensions as [**ID3DXPRTBuffer**](id3dxprtbuffer.md) and must be able to store signed texture formats.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="400d8-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="400d8-113">Return value</span></span>

<span data-ttu-id="400d8-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="400d8-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="400d8-115">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="400d8-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="400d8-116">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="400d8-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="400d8-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="400d8-117">Requirements</span></span>



| <span data-ttu-id="400d8-118">需求</span><span class="sxs-lookup"><span data-stu-id="400d8-118">Requirement</span></span> | <span data-ttu-id="400d8-119">值</span><span class="sxs-lookup"><span data-stu-id="400d8-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="400d8-120">標頭</span><span class="sxs-lookup"><span data-stu-id="400d8-120">Header</span></span><br/>  | <dl> <span data-ttu-id="400d8-121"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="400d8-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="400d8-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="400d8-122">Library</span></span><br/> | <dl> <span data-ttu-id="400d8-123"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="400d8-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="400d8-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="400d8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="400d8-125">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="400d8-125">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
