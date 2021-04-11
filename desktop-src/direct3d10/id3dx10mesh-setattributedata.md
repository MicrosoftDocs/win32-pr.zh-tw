---
description: 設定網狀的屬性資料。
ms.assetid: bcf7b1b3-b923-400a-8d12-5094f3844d8f
title: 'ID3DX10Mesh：： SetAttributeData 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetAttributeData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 19d69f8747196d7b25c85cb04fb173adef193098
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196354"
---
# <a name="id3dx10meshsetattributedata-method"></a><span data-ttu-id="8149e-103">ID3DX10Mesh：： SetAttributeData 方法</span><span class="sxs-lookup"><span data-stu-id="8149e-103">ID3DX10Mesh::SetAttributeData method</span></span>

<span data-ttu-id="8149e-104">設定網狀的屬性資料。</span><span class="sxs-lookup"><span data-stu-id="8149e-104">Set the mesh's attribute data.</span></span>

## <a name="syntax"></a><span data-ttu-id="8149e-105">語法</span><span class="sxs-lookup"><span data-stu-id="8149e-105">Syntax</span></span>


```C++
HRESULT SetAttributeData(
  [in] const UINT *pData
);
```



## <a name="parameters"></a><span data-ttu-id="8149e-106">參數</span><span class="sxs-lookup"><span data-stu-id="8149e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8149e-107">*.pdata* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8149e-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8149e-108">類型： **Const [**UINT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="8149e-108">Type: **const [**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8149e-109">要設定的屬性資料。</span><span class="sxs-lookup"><span data-stu-id="8149e-109">The attribute data to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8149e-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="8149e-110">Return value</span></span>

<span data-ttu-id="8149e-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8149e-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8149e-112">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="8149e-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8149e-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="8149e-113">Requirements</span></span>



| <span data-ttu-id="8149e-114">需求</span><span class="sxs-lookup"><span data-stu-id="8149e-114">Requirement</span></span> | <span data-ttu-id="8149e-115">值</span><span class="sxs-lookup"><span data-stu-id="8149e-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8149e-116">標頭</span><span class="sxs-lookup"><span data-stu-id="8149e-116">Header</span></span><br/>  | <dl> <span data-ttu-id="8149e-117"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="8149e-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="8149e-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="8149e-118">Library</span></span><br/> | <dl> <span data-ttu-id="8149e-119"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8149e-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8149e-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8149e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8149e-121">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="8149e-121">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="8149e-122">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="8149e-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
