---
description: 取得常數資料表的指標。
ms.assetid: 5d836d99-783f-41e1-b7bf-d874d09a4892
title: 'ID3DXTextureShader：： GetConstantBuffer 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader.GetConstantBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8c83a723dde56fc80f643d7209c56fc05ad6cce5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322776"
---
# <a name="id3dxtextureshadergetconstantbuffer-method"></a><span data-ttu-id="48508-103">ID3DXTextureShader：： GetConstantBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="48508-103">ID3DXTextureShader::GetConstantBuffer method</span></span>

<span data-ttu-id="48508-104">取得常數資料表的指標。</span><span class="sxs-lookup"><span data-stu-id="48508-104">Get a pointer to the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="48508-105">語法</span><span class="sxs-lookup"><span data-stu-id="48508-105">Syntax</span></span>


```C++
HRESULT GetConstantBuffer(
  [out] LPD3DXBUFFER *ppConstantBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="48508-106">參數</span><span class="sxs-lookup"><span data-stu-id="48508-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48508-107">*ppConstantBuffer* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="48508-107">*ppConstantBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48508-108">類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="48508-108">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="48508-109">[**ID3DXBuffer**](id3dxbuffer.md)介面的指標，其中包含常數。</span><span class="sxs-lookup"><span data-stu-id="48508-109">Pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface, which contains the constants.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48508-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="48508-110">Return value</span></span>

<span data-ttu-id="48508-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="48508-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="48508-112">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="48508-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="48508-113">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="48508-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="48508-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="48508-114">Requirements</span></span>



| <span data-ttu-id="48508-115">需求</span><span class="sxs-lookup"><span data-stu-id="48508-115">Requirement</span></span> | <span data-ttu-id="48508-116">值</span><span class="sxs-lookup"><span data-stu-id="48508-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="48508-117">標頭</span><span class="sxs-lookup"><span data-stu-id="48508-117">Header</span></span><br/>  | <dl> <span data-ttu-id="48508-118"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="48508-118"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="48508-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="48508-119">Library</span></span><br/> | <dl> <span data-ttu-id="48508-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="48508-120"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="48508-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="48508-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48508-122">ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="48508-122">ID3DXTextureShader</span></span>](id3dxtextureshader.md)
</dt> </dl>

 

 




