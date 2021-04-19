---
description: 設定 (FVF) 類型的彈性頂點格式。
ms.assetid: e581dcd4-7e17-4c36-aac9-c2942924cf51
title: 'ID3DXSkinInfo：： SetFVF 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.SetFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 010385597442ba1546c20122f6551fca0cfcf81c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988572"
---
# <a name="id3dxskininfosetfvf-method"></a><span data-ttu-id="5d2c6-103">ID3DXSkinInfo：： SetFVF 方法</span><span class="sxs-lookup"><span data-stu-id="5d2c6-103">ID3DXSkinInfo::SetFVF method</span></span>

<span data-ttu-id="5d2c6-104">設定 (FVF) 類型的彈性頂點格式。</span><span class="sxs-lookup"><span data-stu-id="5d2c6-104">Sets the flexible vertex format (FVF) type.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d2c6-105">語法</span><span class="sxs-lookup"><span data-stu-id="5d2c6-105">Syntax</span></span>


```C++
HRESULT SetFVF(
  [in] DWORD FVF
);
```



## <a name="parameters"></a><span data-ttu-id="5d2c6-106">參數</span><span class="sxs-lookup"><span data-stu-id="5d2c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d2c6-107">*FVF* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5d2c6-107">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d2c6-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5d2c6-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5d2c6-109">彈性頂點格式。</span><span class="sxs-lookup"><span data-stu-id="5d2c6-109">Flexible vertex format.</span></span> <span data-ttu-id="5d2c6-110">請參閱 [D3DFVF](d3dfvf.md)。</span><span class="sxs-lookup"><span data-stu-id="5d2c6-110">See [D3DFVF](d3dfvf.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d2c6-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="5d2c6-111">Return value</span></span>

<span data-ttu-id="5d2c6-112">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5d2c6-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5d2c6-113">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="5d2c6-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="5d2c6-114">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="5d2c6-114">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d2c6-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="5d2c6-115">Requirements</span></span>



| <span data-ttu-id="5d2c6-116">需求</span><span class="sxs-lookup"><span data-stu-id="5d2c6-116">Requirement</span></span> | <span data-ttu-id="5d2c6-117">值</span><span class="sxs-lookup"><span data-stu-id="5d2c6-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d2c6-118">標頭</span><span class="sxs-lookup"><span data-stu-id="5d2c6-118">Header</span></span><br/>  | <dl> <span data-ttu-id="5d2c6-119"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="5d2c6-119"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="5d2c6-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="5d2c6-120">Library</span></span><br/> | <dl> <span data-ttu-id="5d2c6-121"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d2c6-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5d2c6-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5d2c6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d2c6-123">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="5d2c6-123">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
