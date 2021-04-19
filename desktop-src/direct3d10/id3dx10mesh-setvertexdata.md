---
description: 將頂點資料設定為其中一個網格的頂點緩衝區。
ms.assetid: 930cbc49-4202-431f-ac72-386c31acd87e
title: 'ID3DX10Mesh：： SetVertexData 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetVertexData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 68d54c6868e44517d42e0b53159f7a23ef45a05a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981844"
---
# <a name="id3dx10meshsetvertexdata-method"></a><span data-ttu-id="3dec6-103">ID3DX10Mesh：： SetVertexData 方法</span><span class="sxs-lookup"><span data-stu-id="3dec6-103">ID3DX10Mesh::SetVertexData method</span></span>

<span data-ttu-id="3dec6-104">將頂點資料設定為其中一個網格的頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="3dec6-104">Set vertex data into one of the mesh's vertex buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dec6-105">語法</span><span class="sxs-lookup"><span data-stu-id="3dec6-105">Syntax</span></span>


```C++
HRESULT SetVertexData(
  [in]       UINT iBuffer,
  [in] const void *pData
);
```



## <a name="parameters"></a><span data-ttu-id="3dec6-106">參數</span><span class="sxs-lookup"><span data-stu-id="3dec6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3dec6-107">*windows.storage.streams.ibuffer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3dec6-107">*iBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dec6-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3dec6-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3dec6-109">要以 .Pdata 填滿的頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="3dec6-109">The vertex buffer to be filled with pData.</span></span>

</dd> <dt>

<span data-ttu-id="3dec6-110">*.pdata* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3dec6-110">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dec6-111">類型： **const void \***</span><span class="sxs-lookup"><span data-stu-id="3dec6-111">Type: **const void\***</span></span>

<span data-ttu-id="3dec6-112">要設定的頂點資料。</span><span class="sxs-lookup"><span data-stu-id="3dec6-112">The vertex data to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3dec6-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="3dec6-113">Return value</span></span>

<span data-ttu-id="3dec6-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3dec6-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3dec6-115">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="3dec6-115">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3dec6-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="3dec6-116">Requirements</span></span>



| <span data-ttu-id="3dec6-117">需求</span><span class="sxs-lookup"><span data-stu-id="3dec6-117">Requirement</span></span> | <span data-ttu-id="3dec6-118">值</span><span class="sxs-lookup"><span data-stu-id="3dec6-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3dec6-119">標頭</span><span class="sxs-lookup"><span data-stu-id="3dec6-119">Header</span></span><br/>  | <dl> <span data-ttu-id="3dec6-120"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="3dec6-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="3dec6-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="3dec6-121">Library</span></span><br/> | <dl> <span data-ttu-id="3dec6-122"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3dec6-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3dec6-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3dec6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dec6-124">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="3dec6-124">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="3dec6-125">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="3dec6-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
