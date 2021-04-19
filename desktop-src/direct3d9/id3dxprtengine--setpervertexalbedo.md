---
description: 設定每個網格頂點的 >albedo 值，並覆寫先前的 >albedo 值。
ms.assetid: 5220dfe3-8d41-480c-a850-b9aad3d2bb2f
title: 'ID3DXPRTEngine：： SetPerVertexAlbedo 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetPerVertexAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: da7a33a79cc50963e87d0eff15baf22ee8d79ce3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985723"
---
# <a name="id3dxprtenginesetpervertexalbedo-method"></a><span data-ttu-id="25deb-103">ID3DXPRTEngine：： SetPerVertexAlbedo 方法</span><span class="sxs-lookup"><span data-stu-id="25deb-103">ID3DXPRTEngine::SetPerVertexAlbedo method</span></span>

<span data-ttu-id="25deb-104">設定每個網格頂點的 >albedo 值，並覆寫先前的 >albedo 值。</span><span class="sxs-lookup"><span data-stu-id="25deb-104">Sets an albedo value for each mesh vertex, overwriting previous albedo values.</span></span>

## <a name="syntax"></a><span data-ttu-id="25deb-105">語法</span><span class="sxs-lookup"><span data-stu-id="25deb-105">Syntax</span></span>


```C++
HRESULT SetPerVertexAlbedo(
  [in] const VOID *pDataIn,
  [in]       UINT NumChannels,
  [in]       UINT Stride
);
```



## <a name="parameters"></a><span data-ttu-id="25deb-106">參數</span><span class="sxs-lookup"><span data-stu-id="25deb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25deb-107">*pDataIn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="25deb-107">*pDataIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25deb-108">類型： **CONST VOID \***</span><span class="sxs-lookup"><span data-stu-id="25deb-108">Type: **const VOID\***</span></span>

<span data-ttu-id="25deb-109">第一個範例的 FLOAT >albedo 資料指標。</span><span class="sxs-lookup"><span data-stu-id="25deb-109">Pointer to FLOAT albedo data of the first sample.</span></span>

</dd> <dt>

<span data-ttu-id="25deb-110">*NumChannels* \[在\]</span><span class="sxs-lookup"><span data-stu-id="25deb-110">*NumChannels* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25deb-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="25deb-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="25deb-112">要設定的色彩通道數目。</span><span class="sxs-lookup"><span data-stu-id="25deb-112">Number of color channels to set.</span></span> <span data-ttu-id="25deb-113">設定為1以指定灰色材質 (R = G = B) 或3，以啟用色彩不規則效果。</span><span class="sxs-lookup"><span data-stu-id="25deb-113">Set to 1 to specify gray materials (R = G = B), or 3 to enable color bleeding effects.</span></span>

</dd> <dt>

<span data-ttu-id="25deb-114">*Stride* \[在\]</span><span class="sxs-lookup"><span data-stu-id="25deb-114">*Stride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25deb-115">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="25deb-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="25deb-116">取得下一個樣本 >albedo 值所需的 Stride （以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="25deb-116">Stride in bytes needed to get to next sample's albedo value.</span></span> <span data-ttu-id="25deb-117">請參閱 [寬度與音調 (Direct3D 9) ](width-vs--pitch.md)。</span><span class="sxs-lookup"><span data-stu-id="25deb-117">See [Width vs. Pitch (Direct3D 9)](width-vs--pitch.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25deb-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="25deb-118">Return value</span></span>

<span data-ttu-id="25deb-119">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="25deb-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="25deb-120">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="25deb-120">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="25deb-121">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="25deb-121">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="25deb-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="25deb-122">Requirements</span></span>



| <span data-ttu-id="25deb-123">需求</span><span class="sxs-lookup"><span data-stu-id="25deb-123">Requirement</span></span> | <span data-ttu-id="25deb-124">值</span><span class="sxs-lookup"><span data-stu-id="25deb-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="25deb-125">標頭</span><span class="sxs-lookup"><span data-stu-id="25deb-125">Header</span></span><br/>  | <dl> <span data-ttu-id="25deb-126"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="25deb-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="25deb-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="25deb-127">Library</span></span><br/> | <dl> <span data-ttu-id="25deb-128"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="25deb-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="25deb-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="25deb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25deb-130">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="25deb-130">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
