---
description: 處理一些資料。
ms.assetid: c64f6a2d-4512-4028-8ed9-bfc5e9e86758
title: 'ID3DX10DataProcessor：:P rocess 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataProcessor.Process
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2ddad2f6350f48f65bc82e094eccb92b1b8bf390
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196469"
---
# <a name="id3dx10dataprocessorprocess-method"></a><span data-ttu-id="e965e-103">ID3DX10DataProcessor：:P rocess 方法</span><span class="sxs-lookup"><span data-stu-id="e965e-103">ID3DX10DataProcessor::Process method</span></span>

<span data-ttu-id="e965e-104">處理一些資料。</span><span class="sxs-lookup"><span data-stu-id="e965e-104">Process some data.</span></span>

## <a name="syntax"></a><span data-ttu-id="e965e-105">語法</span><span class="sxs-lookup"><span data-stu-id="e965e-105">Syntax</span></span>


```C++
HRESULT Process(
  [in] void   *pData,
  [in] SIZE_T cBytes
);
```



## <a name="parameters"></a><span data-ttu-id="e965e-106">參數</span><span class="sxs-lookup"><span data-stu-id="e965e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e965e-107">*.pdata* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e965e-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e965e-108">類型： **void \***</span><span class="sxs-lookup"><span data-stu-id="e965e-108">Type: **void\***</span></span>

<span data-ttu-id="e965e-109">要處理之資料的指標。</span><span class="sxs-lookup"><span data-stu-id="e965e-109">Pointer to the data to be processed.</span></span>

</dd> <dt>

<span data-ttu-id="e965e-110">*cBytes* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e965e-110">*cBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e965e-111">類型： **[**大小 \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e965e-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e965e-112">要處理的資料大小。</span><span class="sxs-lookup"><span data-stu-id="e965e-112">Size of the data to be processed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e965e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="e965e-113">Return value</span></span>

<span data-ttu-id="e965e-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e965e-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e965e-115">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="e965e-115">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e965e-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="e965e-116">Requirements</span></span>



| <span data-ttu-id="e965e-117">需求</span><span class="sxs-lookup"><span data-stu-id="e965e-117">Requirement</span></span> | <span data-ttu-id="e965e-118">值</span><span class="sxs-lookup"><span data-stu-id="e965e-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e965e-119">標頭</span><span class="sxs-lookup"><span data-stu-id="e965e-119">Header</span></span><br/>  | <dl> <span data-ttu-id="e965e-120"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="e965e-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="e965e-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="e965e-121">Library</span></span><br/> | <dl> <span data-ttu-id="e965e-122"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e965e-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e965e-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e965e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e965e-124">ID3DX10DataProcessor</span><span class="sxs-lookup"><span data-stu-id="e965e-124">ID3DX10DataProcessor</span></span>](id3dx10dataprocessor.md)
</dt> <dt>

[<span data-ttu-id="e965e-125">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="e965e-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
