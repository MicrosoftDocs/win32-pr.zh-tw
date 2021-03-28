---
title: 'ID3DX11EffectVectorVariable SetFloatVector 方法 (D3dx11effect .h) '
description: 設定包含浮點數據的四個元件向量。
ms.assetid: fb646df6-b9f9-4d71-93c3-38833076b781
keywords:
- SetFloatVector 方法 Direct3D 11
- SetFloatVector 方法 Direct3D 11，ID3DX11EffectVectorVariable 介面
- ID3DX11EffectVectorVariable 介面 Direct3D 11，SetFloatVector 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.SetFloatVector
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5541f2773e992c4c52bf748bceb832d67b28825
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386495"
---
# <a name="id3dx11effectvectorvariablesetfloatvector-method"></a><span data-ttu-id="06c1e-106">ID3DX11EffectVectorVariable：： SetFloatVector 方法</span><span class="sxs-lookup"><span data-stu-id="06c1e-106">ID3DX11EffectVectorVariable::SetFloatVector method</span></span>

<span data-ttu-id="06c1e-107">設定包含浮點數據的四個元件向量。</span><span class="sxs-lookup"><span data-stu-id="06c1e-107">Set a four-component vector that contains floating-point data.</span></span>

## <a name="syntax"></a><span data-ttu-id="06c1e-108">語法</span><span class="sxs-lookup"><span data-stu-id="06c1e-108">Syntax</span></span>


```C++
HRESULT SetFloatVector(
   float *pData
);
```



## <a name="parameters"></a><span data-ttu-id="06c1e-109">參數</span><span class="sxs-lookup"><span data-stu-id="06c1e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06c1e-110">*.Pdata*</span><span class="sxs-lookup"><span data-stu-id="06c1e-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="06c1e-111">類型： **float \***</span><span class="sxs-lookup"><span data-stu-id="06c1e-111">Type: **float\***</span></span>

<span data-ttu-id="06c1e-112">第一個元件的指標。</span><span class="sxs-lookup"><span data-stu-id="06c1e-112">A pointer to the first component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06c1e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="06c1e-113">Return value</span></span>

<span data-ttu-id="06c1e-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="06c1e-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="06c1e-115">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="06c1e-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="06c1e-116">備註</span><span class="sxs-lookup"><span data-stu-id="06c1e-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="06c1e-117">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="06c1e-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="06c1e-118">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="06c1e-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="06c1e-119">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="06c1e-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="06c1e-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="06c1e-120">Requirements</span></span>



| <span data-ttu-id="06c1e-121">需求</span><span class="sxs-lookup"><span data-stu-id="06c1e-121">Requirement</span></span> | <span data-ttu-id="06c1e-122">值</span><span class="sxs-lookup"><span data-stu-id="06c1e-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06c1e-123">標頭</span><span class="sxs-lookup"><span data-stu-id="06c1e-123">Header</span></span><br/>  | <dl> <span data-ttu-id="06c1e-124"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="06c1e-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="06c1e-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="06c1e-125">Library</span></span><br/> | <dl> <span data-ttu-id="06c1e-126"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="06c1e-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06c1e-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="06c1e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06c1e-128">ID3DX11EffectVectorVariable</span><span class="sxs-lookup"><span data-stu-id="06c1e-128">ID3DX11EffectVectorVariable</span></span>](id3dx11effectvectorvariable.md)
</dt> </dl>

 

 





