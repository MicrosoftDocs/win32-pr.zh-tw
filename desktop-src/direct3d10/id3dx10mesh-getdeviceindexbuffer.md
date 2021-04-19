---
description: 在使用 ID3DX10Mesh：： CommitToDevice 認可至裝置之後，存取網格的索引緩衝區。 這與 ID3DX10Mesh：： GetIndexBuffer 不同，它會在認可至裝置之前，傳回索引緩衝區。
ms.assetid: 94d21f50-91b5-4f8d-ac73-7a851bba8685
title: 'ID3DX10Mesh：： GetDeviceIndexBuffer 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetDeviceIndexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3ec3e65cfc4acb5a903bcf18d2f707d39127e975
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976508"
---
# <a name="id3dx10meshgetdeviceindexbuffer-method"></a><span data-ttu-id="dbb09-104">ID3DX10Mesh：： GetDeviceIndexBuffer 方法</span><span class="sxs-lookup"><span data-stu-id="dbb09-104">ID3DX10Mesh::GetDeviceIndexBuffer method</span></span>

<span data-ttu-id="dbb09-105">在使用 [**ID3DX10Mesh：： CommitToDevice**](id3dx10mesh-committodevice.md)認可至裝置之後，存取網格的索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="dbb09-105">Access the mesh's index buffer after it has been committed to the device with [**ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md).</span></span> <span data-ttu-id="dbb09-106">這與 [**ID3DX10Mesh：： GetIndexBuffer**](id3dx10mesh-getindexbuffer.md)不同，它會在認可至裝置之前，傳回索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="dbb09-106">This is different from [**ID3DX10Mesh::GetIndexBuffer**](id3dx10mesh-getindexbuffer.md), which returns the index buffer before it has been committed to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbb09-107">語法</span><span class="sxs-lookup"><span data-stu-id="dbb09-107">Syntax</span></span>


```C++
HRESULT GetDeviceIndexBuffer(
  [out] ID3D10Buffer **ppIndexBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="dbb09-108">參數</span><span class="sxs-lookup"><span data-stu-id="dbb09-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbb09-109">*ppIndexBuffer* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="dbb09-109">*ppIndexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dbb09-110">類型： **[ **ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***</span><span class="sxs-lookup"><span data-stu-id="dbb09-110">Type: **[**ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***</span></span>

<span data-ttu-id="dbb09-111">索引緩衝區認可至裝置之後。</span><span class="sxs-lookup"><span data-stu-id="dbb09-111">The index buffer after it has been committed to the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbb09-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="dbb09-112">Return value</span></span>

<span data-ttu-id="dbb09-113">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dbb09-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dbb09-114">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="dbb09-114">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="dbb09-115">備註</span><span class="sxs-lookup"><span data-stu-id="dbb09-115">Remarks</span></span>

<span data-ttu-id="dbb09-116">如果網格的索引緩衝區尚未認可至裝置，此 API 將會在傳回緩衝區的指標之前，自動認可索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="dbb09-116">If the mesh's index buffer has not already been committed to the device, this API will automatically commit the index buffer before it returns a pointer to the buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbb09-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="dbb09-117">Requirements</span></span>



| <span data-ttu-id="dbb09-118">需求</span><span class="sxs-lookup"><span data-stu-id="dbb09-118">Requirement</span></span> | <span data-ttu-id="dbb09-119">值</span><span class="sxs-lookup"><span data-stu-id="dbb09-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dbb09-120">標頭</span><span class="sxs-lookup"><span data-stu-id="dbb09-120">Header</span></span><br/>  | <dl> <span data-ttu-id="dbb09-121"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="dbb09-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="dbb09-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="dbb09-122">Library</span></span><br/> | <dl> <span data-ttu-id="dbb09-123"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="dbb09-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbb09-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dbb09-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbb09-125">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="dbb09-125">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="dbb09-126">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="dbb09-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




