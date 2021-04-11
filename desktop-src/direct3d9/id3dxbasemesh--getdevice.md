---
description: 捕獲與網格相關聯的裝置。
ms.assetid: 16ff5267-0c64-4c3d-925d-6fc10f54c9c4
title: 'ID3DXBaseMesh：： GetDevice 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetDevice
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2b866c86bf759305a4626f0ff5ecaa8e35bfd75d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035376"
---
# <a name="id3dxbasemeshgetdevice-method"></a><span data-ttu-id="7c55f-103">ID3DXBaseMesh：： GetDevice 方法</span><span class="sxs-lookup"><span data-stu-id="7c55f-103">ID3DXBaseMesh::GetDevice method</span></span>

<span data-ttu-id="7c55f-104">捕獲與網格相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="7c55f-104">Retrieves the device associated with the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c55f-105">語法</span><span class="sxs-lookup"><span data-stu-id="7c55f-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out, retval] LPDIRECT3DDEVICE9 *ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="7c55f-106">參數</span><span class="sxs-lookup"><span data-stu-id="7c55f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c55f-107">*ppDevice* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="7c55f-107">*ppDevice* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="7c55f-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span><span class="sxs-lookup"><span data-stu-id="7c55f-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)\***</span></span>

<span data-ttu-id="7c55f-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面指標的位址，表示與網格相關聯的 Direct3D 裝置物件。</span><span class="sxs-lookup"><span data-stu-id="7c55f-109">Address of a pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the Direct3D device object associated with the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c55f-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="7c55f-110">Return value</span></span>

<span data-ttu-id="7c55f-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7c55f-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7c55f-112">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="7c55f-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="7c55f-113">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="7c55f-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c55f-114">備註</span><span class="sxs-lookup"><span data-stu-id="7c55f-114">Remarks</span></span>

<span data-ttu-id="7c55f-115">呼叫這個方法將會增加 [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) 介面上的內部參考計數。</span><span class="sxs-lookup"><span data-stu-id="7c55f-115">Calling this method will increase the internal reference count on the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span> <span data-ttu-id="7c55f-116">當您使用這個 **IDirect3DDevice9** 介面完成時，請務必呼叫 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) ，否則會發生記憶體流失。</span><span class="sxs-lookup"><span data-stu-id="7c55f-116">Be sure to call [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) when you are done using this **IDirect3DDevice9** interface or you will have a memory leak.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c55f-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="7c55f-117">Requirements</span></span>



| <span data-ttu-id="7c55f-118">需求</span><span class="sxs-lookup"><span data-stu-id="7c55f-118">Requirement</span></span> | <span data-ttu-id="7c55f-119">值</span><span class="sxs-lookup"><span data-stu-id="7c55f-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c55f-120">標頭</span><span class="sxs-lookup"><span data-stu-id="7c55f-120">Header</span></span><br/>  | <dl> <span data-ttu-id="7c55f-121"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="7c55f-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="7c55f-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="7c55f-122">Library</span></span><br/> | <dl> <span data-ttu-id="7c55f-123"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c55f-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7c55f-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7c55f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c55f-125">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="7c55f-125">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
