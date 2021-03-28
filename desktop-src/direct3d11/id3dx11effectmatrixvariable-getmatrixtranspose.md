---
title: 'ID3DX11EffectMatrixVariable GetMatrixTranspose 方法 (D3dx11effect .h) '
description: 調換和取得浮點數矩陣。
ms.assetid: a261128c-d1f9-4864-b562-5fe9a69c9969
keywords:
- GetMatrixTranspose 方法 Direct3D 11
- GetMatrixTranspose 方法 Direct3D 11，ID3DX11EffectMatrixVariable 介面
- ID3DX11EffectMatrixVariable 介面 Direct3D 11，GetMatrixTranspose 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.GetMatrixTranspose
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fa5c8eb8e424041a05461636d1eaf7b65c7cd4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035382"
---
# <a name="id3dx11effectmatrixvariablegetmatrixtranspose-method"></a><span data-ttu-id="7b30e-106">ID3DX11EffectMatrixVariable：： GetMatrixTranspose 方法</span><span class="sxs-lookup"><span data-stu-id="7b30e-106">ID3DX11EffectMatrixVariable::GetMatrixTranspose method</span></span>

<span data-ttu-id="7b30e-107">調換和取得浮點數矩陣。</span><span class="sxs-lookup"><span data-stu-id="7b30e-107">Transpose and get a floating-point matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b30e-108">語法</span><span class="sxs-lookup"><span data-stu-id="7b30e-108">Syntax</span></span>


```C++
HRESULT GetMatrixTranspose(
   float *pData
);
```



## <a name="parameters"></a><span data-ttu-id="7b30e-109">參數</span><span class="sxs-lookup"><span data-stu-id="7b30e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b30e-110">*.Pdata*</span><span class="sxs-lookup"><span data-stu-id="7b30e-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="7b30e-111">類型： **float \***</span><span class="sxs-lookup"><span data-stu-id="7b30e-111">Type: **float\***</span></span>

<span data-ttu-id="7b30e-112">已轉置矩陣之第一個元素的指標。</span><span class="sxs-lookup"><span data-stu-id="7b30e-112">A pointer to the first element of a transposed matrix.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b30e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="7b30e-113">Return value</span></span>

<span data-ttu-id="7b30e-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7b30e-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7b30e-115">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="7b30e-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7b30e-116">備註</span><span class="sxs-lookup"><span data-stu-id="7b30e-116">Remarks</span></span>

<span data-ttu-id="7b30e-117">轉型矩陣會將資料順序從資料列資料行順序重新排列成資料行順序 (或反之亦然) 。</span><span class="sxs-lookup"><span data-stu-id="7b30e-117">Transposing a matrix will rearrange the data order from row-column order to column-row order (or vice versa).</span></span>

> [!Note]  
> <span data-ttu-id="7b30e-118">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="7b30e-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="7b30e-119">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="7b30e-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="7b30e-120">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="7b30e-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7b30e-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="7b30e-121">Requirements</span></span>



| <span data-ttu-id="7b30e-122">需求</span><span class="sxs-lookup"><span data-stu-id="7b30e-122">Requirement</span></span> | <span data-ttu-id="7b30e-123">值</span><span class="sxs-lookup"><span data-stu-id="7b30e-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b30e-124">標頭</span><span class="sxs-lookup"><span data-stu-id="7b30e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="7b30e-125"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="7b30e-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="7b30e-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="7b30e-126">Library</span></span><br/> | <dl> <span data-ttu-id="7b30e-127"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="7b30e-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b30e-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7b30e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b30e-129">ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="7b30e-129">ID3DX11EffectMatrixVariable</span></span>](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

 





