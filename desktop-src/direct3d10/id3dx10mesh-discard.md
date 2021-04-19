---
description: 使用 ID3DX10Mesh：： CommitToDevice) ，從已認可至裝置 (的裝置移除網格資料。
ms.assetid: 60eee1f8-f04b-4f33-8f86-0564d0334f97
title: 'ID3DX10Mesh：:D iscard 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.Discard
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f861de8eefff603954e896a1b6684afc8806764f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106991466"
---
# <a name="id3dx10meshdiscard-method"></a><span data-ttu-id="5bc7a-103">ID3DX10Mesh：:D iscard 方法</span><span class="sxs-lookup"><span data-stu-id="5bc7a-103">ID3DX10Mesh::Discard method</span></span>

<span data-ttu-id="5bc7a-104">使用 [**ID3DX10Mesh：： CommitToDevice**](id3dx10mesh-committodevice.md)) ，從已認可至裝置 (的裝置移除網格資料。</span><span class="sxs-lookup"><span data-stu-id="5bc7a-104">Removes mesh data from the device that has been committed to the device (with [**ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="5bc7a-105">語法</span><span class="sxs-lookup"><span data-stu-id="5bc7a-105">Syntax</span></span>


```C++
HRESULT Discard(
  [in] D3DX10_MESH_DISCARD_FLAGS dwDiscard
);
```



## <a name="parameters"></a><span data-ttu-id="5bc7a-106">參數</span><span class="sxs-lookup"><span data-stu-id="5bc7a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bc7a-107">*dwDiscard* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5bc7a-107">*dwDiscard* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bc7a-108">類型： **[ **D3DX10 \_ 網格 \_ 捨棄 \_ 旗標**](d3dx10-mesh-discard-flags.md)**</span><span class="sxs-lookup"><span data-stu-id="5bc7a-108">Type: **[**D3DX10\_MESH\_DISCARD\_FLAGS**](d3dx10-mesh-discard-flags.md)**</span></span>

<span data-ttu-id="5bc7a-109">指定要從裝置捨棄哪些網格資料片段。</span><span class="sxs-lookup"><span data-stu-id="5bc7a-109">Specifies which pieces of mesh data to discard from the device.</span></span> <span data-ttu-id="5bc7a-110">請參閱 [**D3DX10 \_ 網格 \_ 捨棄 \_ 旗標**](d3dx10-mesh-discard-flags.md)。</span><span class="sxs-lookup"><span data-stu-id="5bc7a-110">See [**D3DX10\_MESH\_DISCARD\_FLAGS**](d3dx10-mesh-discard-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bc7a-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="5bc7a-111">Return value</span></span>

<span data-ttu-id="5bc7a-112">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5bc7a-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5bc7a-113">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="5bc7a-113">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5bc7a-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="5bc7a-114">Requirements</span></span>



| <span data-ttu-id="5bc7a-115">需求</span><span class="sxs-lookup"><span data-stu-id="5bc7a-115">Requirement</span></span> | <span data-ttu-id="5bc7a-116">值</span><span class="sxs-lookup"><span data-stu-id="5bc7a-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5bc7a-117">標頭</span><span class="sxs-lookup"><span data-stu-id="5bc7a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="5bc7a-118"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="5bc7a-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="5bc7a-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="5bc7a-119">Library</span></span><br/> | <dl> <span data-ttu-id="5bc7a-120"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5bc7a-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bc7a-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5bc7a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bc7a-122">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="5bc7a-122">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="5bc7a-123">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="5bc7a-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




