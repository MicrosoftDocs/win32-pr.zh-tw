---
description: 取得函數 DWORD 資料流程的指標。
ms.assetid: a051b51a-185c-4a9e-a8b9-4096615e2634
title: 'ID3DXTextureShader：： GetFunction 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetFunction
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 80e504e65e4c8437247b2935794025e1b693433a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982226"
---
# <a name="id3dxtextureshadergetfunction-method"></a><span data-ttu-id="40ffb-103">ID3DXTextureShader：： GetFunction 方法</span><span class="sxs-lookup"><span data-stu-id="40ffb-103">ID3DXTextureShader::GetFunction method</span></span>

<span data-ttu-id="40ffb-104">取得函數 DWORD 資料流程的指標。</span><span class="sxs-lookup"><span data-stu-id="40ffb-104">Gets a pointer to the function DWORD stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="40ffb-105">語法</span><span class="sxs-lookup"><span data-stu-id="40ffb-105">Syntax</span></span>


```C++
HRESULT GetFunction(
  [in] LPD3DXBUFFER *ppFunction
);
```



## <a name="parameters"></a><span data-ttu-id="40ffb-106">參數</span><span class="sxs-lookup"><span data-stu-id="40ffb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40ffb-107">*ppFunction* \[在\]</span><span class="sxs-lookup"><span data-stu-id="40ffb-107">*ppFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40ffb-108">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="40ffb-108">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="40ffb-109">函數 DWORD 資料流程的指標。</span><span class="sxs-lookup"><span data-stu-id="40ffb-109">A pointer to the function DWORD stream.</span></span> <span data-ttu-id="40ffb-110">請參閱 [**ID3DXBuffer**](id3dxbuffer.md)。</span><span class="sxs-lookup"><span data-stu-id="40ffb-110">See [**ID3DXBuffer**](id3dxbuffer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40ffb-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="40ffb-111">Return value</span></span>

<span data-ttu-id="40ffb-112">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="40ffb-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="40ffb-113">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="40ffb-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="40ffb-114">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="40ffb-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="40ffb-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="40ffb-115">Requirements</span></span>



| <span data-ttu-id="40ffb-116">需求</span><span class="sxs-lookup"><span data-stu-id="40ffb-116">Requirement</span></span> | <span data-ttu-id="40ffb-117">值</span><span class="sxs-lookup"><span data-stu-id="40ffb-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="40ffb-118">標頭</span><span class="sxs-lookup"><span data-stu-id="40ffb-118">Header</span></span><br/>  | <dl> <span data-ttu-id="40ffb-119"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="40ffb-119"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="40ffb-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="40ffb-120">Library</span></span><br/> | <dl> <span data-ttu-id="40ffb-121"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="40ffb-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="40ffb-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="40ffb-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40ffb-123">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="40ffb-123">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




