---
description: 設定頂點宣告。
ms.assetid: cbb802ac-f0ba-41e6-8c67-a787982f975f
title: 'ID3DXSkinInfo：： SetDeclaration 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetDeclaration
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 821801647ca1aee3deabe69d911bd1cab5f7eb4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322596"
---
# <a name="id3dxskininfosetdeclaration-method"></a><span data-ttu-id="698bb-103">ID3DXSkinInfo：： SetDeclaration 方法</span><span class="sxs-lookup"><span data-stu-id="698bb-103">ID3DXSkinInfo::SetDeclaration method</span></span>

<span data-ttu-id="698bb-104">設定頂點宣告。</span><span class="sxs-lookup"><span data-stu-id="698bb-104">Sets the vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="698bb-105">語法</span><span class="sxs-lookup"><span data-stu-id="698bb-105">Syntax</span></span>


```C++
HRESULT SetDeclaration(
  [in] const D3DVERTEXELEMENT9 *pDeclaration
);
```



## <a name="parameters"></a><span data-ttu-id="698bb-106">參數</span><span class="sxs-lookup"><span data-stu-id="698bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="698bb-107">*pDeclaration* \[在\]</span><span class="sxs-lookup"><span data-stu-id="698bb-107">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="698bb-108">Type： **Const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="698bb-108">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="698bb-109">[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)元素陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="698bb-109">Pointer to an array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="698bb-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="698bb-110">Return value</span></span>

<span data-ttu-id="698bb-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="698bb-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="698bb-112">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="698bb-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="698bb-113">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="698bb-113">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="698bb-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="698bb-114">Requirements</span></span>



| <span data-ttu-id="698bb-115">需求</span><span class="sxs-lookup"><span data-stu-id="698bb-115">Requirement</span></span> | <span data-ttu-id="698bb-116">值</span><span class="sxs-lookup"><span data-stu-id="698bb-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="698bb-117">標頭</span><span class="sxs-lookup"><span data-stu-id="698bb-117">Header</span></span><br/>  | <dl> <span data-ttu-id="698bb-118"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="698bb-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="698bb-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="698bb-119">Library</span></span><br/> | <dl> <span data-ttu-id="698bb-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="698bb-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="698bb-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="698bb-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="698bb-122">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="698bb-122">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="698bb-123">**ID3DXSkinInfo：： GetDeclaration**</span><span class="sxs-lookup"><span data-stu-id="698bb-123">**ID3DXSkinInfo::GetDeclaration**</span></span>](id3dxskininfo--getdeclaration.md)
</dt> </dl>

 

 




