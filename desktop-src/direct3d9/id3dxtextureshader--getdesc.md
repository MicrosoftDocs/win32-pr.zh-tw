---
description: ID3DXTextureShader：： GetDesc 方法-取得常數資料表的描述。
ms.assetid: 91b537bb-5f7a-448b-a21f-c0ddf66d7238
title: 'ID3DXTextureShader：： GetDesc 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6ea94f0e22d838f09dae9b423f85aa1d55d2365b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117636"
---
# <a name="id3dxtextureshadergetdesc-method"></a><span data-ttu-id="e07e3-103">ID3DXTextureShader：： GetDesc 方法</span><span class="sxs-lookup"><span data-stu-id="e07e3-103">ID3DXTextureShader::GetDesc method</span></span>

<span data-ttu-id="e07e3-104">取得常數資料表的描述。</span><span class="sxs-lookup"><span data-stu-id="e07e3-104">Gets a description of the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="e07e3-105">語法</span><span class="sxs-lookup"><span data-stu-id="e07e3-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [in] D3DXCONSTANTTABLE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="e07e3-106">參數</span><span class="sxs-lookup"><span data-stu-id="e07e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e07e3-107">*pDesc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e07e3-107">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e07e3-108">類型： **[ **D3DXCONSTANTTABLE \_ DESC**](d3dxconstanttable-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="e07e3-108">Type: **[**D3DXCONSTANTTABLE\_DESC**](d3dxconstanttable-desc.md)\***</span></span>

<span data-ttu-id="e07e3-109">常數資料表的屬性。</span><span class="sxs-lookup"><span data-stu-id="e07e3-109">The attributes of the constant table.</span></span> <span data-ttu-id="e07e3-110">請參閱 [**D3DXCONSTANTTABLE \_ DESC**](d3dxconstanttable-desc.md)。</span><span class="sxs-lookup"><span data-stu-id="e07e3-110">See [**D3DXCONSTANTTABLE\_DESC**](d3dxconstanttable-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e07e3-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e07e3-111">Return value</span></span>

<span data-ttu-id="e07e3-112">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e07e3-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e07e3-113">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="e07e3-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e07e3-114">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="e07e3-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="e07e3-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="e07e3-115">Requirements</span></span>



| <span data-ttu-id="e07e3-116">需求</span><span class="sxs-lookup"><span data-stu-id="e07e3-116">Requirement</span></span> | <span data-ttu-id="e07e3-117">值</span><span class="sxs-lookup"><span data-stu-id="e07e3-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e07e3-118">標頭</span><span class="sxs-lookup"><span data-stu-id="e07e3-118">Header</span></span><br/>  | <dl> <span data-ttu-id="e07e3-119"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="e07e3-119"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="e07e3-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="e07e3-120">Library</span></span><br/> | <dl> <span data-ttu-id="e07e3-121"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e07e3-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e07e3-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e07e3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e07e3-123">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="e07e3-123">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




