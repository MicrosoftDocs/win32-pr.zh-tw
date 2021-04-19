---
description: 在使用 ID3DX10Mesh：： CommitToDevice 認可至裝置之後，存取網格的頂點緩衝區。 這與 ID3DX10Mesh：： GetVertexBuffer 不同，它會在認可至裝置之前傳回頂點緩衝區。
ms.assetid: 621d9105-e55d-47b8-8557-8adb7db19d66
title: 'ID3DX10Mesh：： GetDeviceVertexBuffer 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetDeviceVertexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9943050d174acb4e8f8e676f56a95cfdcde88f5a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106989212"
---
# <a name="id3dx10meshgetdevicevertexbuffer-method"></a><span data-ttu-id="2b94e-104">ID3DX10Mesh：： GetDeviceVertexBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="2b94e-104">ID3DX10Mesh::GetDeviceVertexBuffer method</span></span>

<span data-ttu-id="2b94e-105">在使用 [**ID3DX10Mesh：： CommitToDevice**](id3dx10mesh-committodevice.md)認可至裝置之後，存取網格的頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="2b94e-105">Access the mesh's vertex buffer after it has been committed to the device with [**ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md).</span></span> <span data-ttu-id="2b94e-106">這與 [**ID3DX10Mesh：： GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md)不同，它會在認可至裝置之前傳回頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="2b94e-106">This is different from [**ID3DX10Mesh::GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md), which returns the vertex buffer before it has been committed to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b94e-107">語法</span><span class="sxs-lookup"><span data-stu-id="2b94e-107">Syntax</span></span>


```C++
HRESULT GetDeviceVertexBuffer(
  [in]  UINT         iBuffer,
  [out] ID3D10Buffer **ppVertexBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="2b94e-108">參數</span><span class="sxs-lookup"><span data-stu-id="2b94e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b94e-109">*windows.storage.streams.ibuffer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2b94e-109">*iBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b94e-110">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2b94e-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2b94e-111">識別要存取之頂點緩衝區的索引。</span><span class="sxs-lookup"><span data-stu-id="2b94e-111">An index identifying which vertex buffer to access.</span></span>

</dd> <dt>

<span data-ttu-id="2b94e-112">*ppVertexBuffer* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2b94e-112">*ppVertexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b94e-113">類型： **[ **ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***</span><span class="sxs-lookup"><span data-stu-id="2b94e-113">Type: **[**ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***</span></span>

<span data-ttu-id="2b94e-114">將頂點緩衝區認可至裝置之後。</span><span class="sxs-lookup"><span data-stu-id="2b94e-114">The vertex buffer after it has been committed to the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b94e-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="2b94e-115">Return value</span></span>

<span data-ttu-id="2b94e-116">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2b94e-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2b94e-117">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="2b94e-117">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2b94e-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="2b94e-118">Requirements</span></span>



| <span data-ttu-id="2b94e-119">需求</span><span class="sxs-lookup"><span data-stu-id="2b94e-119">Requirement</span></span> | <span data-ttu-id="2b94e-120">值</span><span class="sxs-lookup"><span data-stu-id="2b94e-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2b94e-121">標頭</span><span class="sxs-lookup"><span data-stu-id="2b94e-121">Header</span></span><br/>  | <dl> <span data-ttu-id="2b94e-122"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="2b94e-122"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="2b94e-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="2b94e-123">Library</span></span><br/> | <dl> <span data-ttu-id="2b94e-124"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b94e-124"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b94e-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2b94e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b94e-126">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="2b94e-126">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="2b94e-127">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="2b94e-127">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
