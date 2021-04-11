---
description: 切換模式以繪製 OpenGL 樣式的線條。
ms.assetid: 298bf391-9f2b-4352-b9f8-3bc2ab661eee
title: 'ID3DXLine：： SetGLLines 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetGLLines
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 131c472ef4a2254880ef560edccb9c0cf1c8774b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103854088"
---
# <a name="id3dxlinesetgllines-method"></a><span data-ttu-id="1ed12-103">ID3DXLine：： SetGLLines 方法</span><span class="sxs-lookup"><span data-stu-id="1ed12-103">ID3DXLine::SetGLLines method</span></span>

<span data-ttu-id="1ed12-104">切換模式以繪製 OpenGL 樣式的線條。</span><span class="sxs-lookup"><span data-stu-id="1ed12-104">Toggles the mode to draw OpenGL-style lines.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ed12-105">語法</span><span class="sxs-lookup"><span data-stu-id="1ed12-105">Syntax</span></span>


```C++
HRESULT SetGLLines(
  [in] BOOL bGLLines
);
```



## <a name="parameters"></a><span data-ttu-id="1ed12-106">參數</span><span class="sxs-lookup"><span data-stu-id="1ed12-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ed12-107">*bGLLines* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1ed12-107">*bGLLines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ed12-108">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ed12-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ed12-109">切換 OpenGL 樣式的線條繪圖。</span><span class="sxs-lookup"><span data-stu-id="1ed12-109">Toggles OpenGL-style line drawing.</span></span> <span data-ttu-id="1ed12-110">**TRUE** 會啟用 OpenGL 樣式的行，而 **FALSE** 則會啟用 Direct3D 樣式的行。</span><span class="sxs-lookup"><span data-stu-id="1ed12-110">**TRUE** enables OpenGL-style lines, and **FALSE** enables Direct3D-style lines.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ed12-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1ed12-111">Return value</span></span>

<span data-ttu-id="1ed12-112">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1ed12-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1ed12-113">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="1ed12-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1ed12-114">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="1ed12-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ed12-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ed12-115">Requirements</span></span>



| <span data-ttu-id="1ed12-116">需求</span><span class="sxs-lookup"><span data-stu-id="1ed12-116">Requirement</span></span> | <span data-ttu-id="1ed12-117">值</span><span class="sxs-lookup"><span data-stu-id="1ed12-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ed12-118">標頭</span><span class="sxs-lookup"><span data-stu-id="1ed12-118">Header</span></span><br/>  | <dl> <span data-ttu-id="1ed12-119"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="1ed12-119"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="1ed12-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="1ed12-120">Library</span></span><br/> | <dl> <span data-ttu-id="1ed12-121"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ed12-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1ed12-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1ed12-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ed12-123">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="1ed12-123">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
