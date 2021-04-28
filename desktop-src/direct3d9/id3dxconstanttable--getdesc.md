---
description: ID3DXConstantTable：： GetDesc 方法-取得常數資料表的描述。
ms.assetid: 3a7396c6-3a3e-44c2-96b7-60339015b376
title: 'ID3DXConstantTable：： GetDesc 方法 (D3DX9Shader .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 81b64f1a01af8909aa820e772214a1f11c6099b8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115236"
---
# <a name="id3dxconstanttablegetdesc-method"></a><span data-ttu-id="accc9-103">ID3DXConstantTable：： GetDesc 方法</span><span class="sxs-lookup"><span data-stu-id="accc9-103">ID3DXConstantTable::GetDesc method</span></span>

<span data-ttu-id="accc9-104">取得常數資料表的描述。</span><span class="sxs-lookup"><span data-stu-id="accc9-104">Gets a description of the constant table.</span></span>

## <a name="syntax"></a><span data-ttu-id="accc9-105">語法</span><span class="sxs-lookup"><span data-stu-id="accc9-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [in] D3DXCONSTANTTABLE_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="accc9-106">參數</span><span class="sxs-lookup"><span data-stu-id="accc9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="accc9-107">*pDesc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="accc9-107">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="accc9-108">類型： **[ **D3DXCONSTANTTABLE \_ DESC**](d3dxconstanttable-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="accc9-108">Type: **[**D3DXCONSTANTTABLE\_DESC**](d3dxconstanttable-desc.md)\***</span></span>

<span data-ttu-id="accc9-109">常數資料表的描述。</span><span class="sxs-lookup"><span data-stu-id="accc9-109">Description of the constant table.</span></span> <span data-ttu-id="accc9-110">請參閱 [**D3DXCONSTANTTABLE \_ DESC**](d3dxconstanttable-desc.md)。</span><span class="sxs-lookup"><span data-stu-id="accc9-110">See [**D3DXCONSTANTTABLE\_DESC**](d3dxconstanttable-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="accc9-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="accc9-111">Return value</span></span>

<span data-ttu-id="accc9-112">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="accc9-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="accc9-113">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="accc9-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="accc9-114">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="accc9-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="accc9-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="accc9-115">Requirements</span></span>



| <span data-ttu-id="accc9-116">需求</span><span class="sxs-lookup"><span data-stu-id="accc9-116">Requirement</span></span> | <span data-ttu-id="accc9-117">值</span><span class="sxs-lookup"><span data-stu-id="accc9-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="accc9-118">標頭</span><span class="sxs-lookup"><span data-stu-id="accc9-118">Header</span></span><br/>  | <dl> <span data-ttu-id="accc9-119"><dt>D3DX9Shader。h</dt></span><span class="sxs-lookup"><span data-stu-id="accc9-119"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="accc9-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="accc9-120">Library</span></span><br/> | <dl> <span data-ttu-id="accc9-121"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="accc9-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="accc9-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="accc9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="accc9-123">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="accc9-123">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> <dt>

[<span data-ttu-id="accc9-124">**ID3DXConstantTable::GetConstantDesc**</span><span class="sxs-lookup"><span data-stu-id="accc9-124">**ID3DXConstantTable::GetConstantDesc**</span></span>](id3dxconstanttable--getconstantdesc.md)
</dt> </dl>

 

 




