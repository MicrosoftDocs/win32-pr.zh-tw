---
title: 'ID3DX11EffectMatrixVariable SetMatrixTransposeArray 方法 (D3dx11effect .h) '
description: 變換並設定浮點數矩陣的陣列。
ms.assetid: 08223022-5e77-4a84-9b68-b9b0c9a02270
keywords:
- SetMatrixTransposeArray 方法 Direct3D 11
- SetMatrixTransposeArray 方法 Direct3D 11，ID3DX11EffectMatrixVariable 介面
- ID3DX11EffectMatrixVariable 介面 Direct3D 11，SetMatrixTransposeArray 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.SetMatrixTransposeArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f70676b76658b5732c1a2ee15858f83694272b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946210"
---
# <a name="id3dx11effectmatrixvariablesetmatrixtransposearray-method"></a><span data-ttu-id="def12-106">ID3DX11EffectMatrixVariable：： SetMatrixTransposeArray 方法</span><span class="sxs-lookup"><span data-stu-id="def12-106">ID3DX11EffectMatrixVariable::SetMatrixTransposeArray method</span></span>

<span data-ttu-id="def12-107">變換並設定浮點數矩陣的陣列。</span><span class="sxs-lookup"><span data-stu-id="def12-107">Transpose and set an array of floating-point matrices.</span></span>

## <a name="syntax"></a><span data-ttu-id="def12-108">語法</span><span class="sxs-lookup"><span data-stu-id="def12-108">Syntax</span></span>


```C++
HRESULT SetMatrixTransposeArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a><span data-ttu-id="def12-109">參數</span><span class="sxs-lookup"><span data-stu-id="def12-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="def12-110">*.Pdata*</span><span class="sxs-lookup"><span data-stu-id="def12-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="def12-111">類型： **float \***</span><span class="sxs-lookup"><span data-stu-id="def12-111">Type: **float\***</span></span>

<span data-ttu-id="def12-112">矩陣陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="def12-112">A pointer to an array of matrices.</span></span>

</dd> <dt>

<span data-ttu-id="def12-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="def12-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="def12-114">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="def12-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="def12-115">位移 (在陣列的開頭與要設定的第一個矩陣之間的矩陣數目) 。</span><span class="sxs-lookup"><span data-stu-id="def12-115">The offset (in number of matrices) between the start of the array and the first matrix to set.</span></span>

</dd> <dt>

<span data-ttu-id="def12-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="def12-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="def12-117">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="def12-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="def12-118">要設定的陣列中的矩陣數目。</span><span class="sxs-lookup"><span data-stu-id="def12-118">The number of matrices in the array to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="def12-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="def12-119">Return value</span></span>

<span data-ttu-id="def12-120">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="def12-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="def12-121">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="def12-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="def12-122">備註</span><span class="sxs-lookup"><span data-stu-id="def12-122">Remarks</span></span>

<span data-ttu-id="def12-123">轉型矩陣會將資料順序從資料列資料行順序重新排列成資料行順序 (或反之亦然) 。</span><span class="sxs-lookup"><span data-stu-id="def12-123">Transposing a matrix will rearrange the data order from row-column order to column-row order (or vice versa).</span></span>

> [!Note]  
> <span data-ttu-id="def12-124">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="def12-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="def12-125">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="def12-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="def12-126">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="def12-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="def12-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="def12-127">Requirements</span></span>



| <span data-ttu-id="def12-128">需求</span><span class="sxs-lookup"><span data-stu-id="def12-128">Requirement</span></span> | <span data-ttu-id="def12-129">值</span><span class="sxs-lookup"><span data-stu-id="def12-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="def12-130">標頭</span><span class="sxs-lookup"><span data-stu-id="def12-130">Header</span></span><br/>  | <dl> <span data-ttu-id="def12-131"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="def12-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="def12-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="def12-132">Library</span></span><br/> | <dl> <span data-ttu-id="def12-133"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="def12-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="def12-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="def12-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="def12-135">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="def12-135">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

