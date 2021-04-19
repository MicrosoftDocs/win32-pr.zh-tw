---
description: 設定網格的點代表資料。
ms.assetid: 451a1ff0-68fa-48c4-b3f1-d41d7583cb3f
title: 'ID3DX10Mesh：： SetPointRepData 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetPointRepData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 65114c5411de7932e9cb71166fcf8554fa0bf7b6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106989210"
---
# <a name="id3dx10meshsetpointrepdata-method"></a><span data-ttu-id="dd1ec-103">ID3DX10Mesh：： SetPointRepData 方法</span><span class="sxs-lookup"><span data-stu-id="dd1ec-103">ID3DX10Mesh::SetPointRepData method</span></span>

<span data-ttu-id="dd1ec-104">設定網格的點代表資料。</span><span class="sxs-lookup"><span data-stu-id="dd1ec-104">Set the point rep data for the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd1ec-105">語法</span><span class="sxs-lookup"><span data-stu-id="dd1ec-105">Syntax</span></span>


```C++
HRESULT SetPointRepData(
  [in] const UINT *pPointReps
);
```



## <a name="parameters"></a><span data-ttu-id="dd1ec-106">參數</span><span class="sxs-lookup"><span data-stu-id="dd1ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd1ec-107">*pPointReps* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dd1ec-107">*pPointReps* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd1ec-108">類型： **Const [**UINT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="dd1ec-108">Type: **const [**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="dd1ec-109">要設定的點代表資料。</span><span class="sxs-lookup"><span data-stu-id="dd1ec-109">The point rep data to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd1ec-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="dd1ec-110">Return value</span></span>

<span data-ttu-id="dd1ec-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dd1ec-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dd1ec-112">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="dd1ec-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dd1ec-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="dd1ec-113">Requirements</span></span>



| <span data-ttu-id="dd1ec-114">需求</span><span class="sxs-lookup"><span data-stu-id="dd1ec-114">Requirement</span></span> | <span data-ttu-id="dd1ec-115">值</span><span class="sxs-lookup"><span data-stu-id="dd1ec-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dd1ec-116">標頭</span><span class="sxs-lookup"><span data-stu-id="dd1ec-116">Header</span></span><br/>  | <dl> <span data-ttu-id="dd1ec-117"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="dd1ec-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="dd1ec-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="dd1ec-118">Library</span></span><br/> | <dl> <span data-ttu-id="dd1ec-119"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="dd1ec-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd1ec-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dd1ec-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd1ec-121">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="dd1ec-121">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="dd1ec-122">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="dd1ec-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
