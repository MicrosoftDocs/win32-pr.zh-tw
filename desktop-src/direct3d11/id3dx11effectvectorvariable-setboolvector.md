---
title: 'ID3DX11EffectVectorVariable SetBoolVector 方法 (D3dx11effect .h) '
description: 設定包含布林資料的四個元件向量。
ms.assetid: 2138eeb9-6aa0-43f5-852c-1ab9c8117a88
keywords:
- SetBoolVector 方法 Direct3D 11
- SetBoolVector 方法 Direct3D 11，ID3DX11EffectVectorVariable 介面
- ID3DX11EffectVectorVariable 介面 Direct3D 11，SetBoolVector 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.SetBoolVector
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03cc5885353e59d3c95139dcd7d99ce39c6f1015
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946195"
---
# <a name="id3dx11effectvectorvariablesetboolvector-method"></a><span data-ttu-id="63ca5-106">ID3DX11EffectVectorVariable：： SetBoolVector 方法</span><span class="sxs-lookup"><span data-stu-id="63ca5-106">ID3DX11EffectVectorVariable::SetBoolVector method</span></span>

<span data-ttu-id="63ca5-107">設定包含布林資料的四個元件向量。</span><span class="sxs-lookup"><span data-stu-id="63ca5-107">Set a four-component vector that contains boolean data.</span></span>

## <a name="syntax"></a><span data-ttu-id="63ca5-108">語法</span><span class="sxs-lookup"><span data-stu-id="63ca5-108">Syntax</span></span>


```C++
HRESULT SetBoolVector(
   BOOL *pData
);
```



## <a name="parameters"></a><span data-ttu-id="63ca5-109">參數</span><span class="sxs-lookup"><span data-stu-id="63ca5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63ca5-110">*.Pdata*</span><span class="sxs-lookup"><span data-stu-id="63ca5-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="63ca5-111">類型： **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="63ca5-111">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="63ca5-112">第一個元件的指標。</span><span class="sxs-lookup"><span data-stu-id="63ca5-112">A pointer to the first component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63ca5-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="63ca5-113">Return value</span></span>

<span data-ttu-id="63ca5-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="63ca5-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="63ca5-115">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="63ca5-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="63ca5-116">備註</span><span class="sxs-lookup"><span data-stu-id="63ca5-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="63ca5-117">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="63ca5-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="63ca5-118">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="63ca5-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="63ca5-119">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="63ca5-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="63ca5-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="63ca5-120">Requirements</span></span>



| <span data-ttu-id="63ca5-121">需求</span><span class="sxs-lookup"><span data-stu-id="63ca5-121">Requirement</span></span> | <span data-ttu-id="63ca5-122">值</span><span class="sxs-lookup"><span data-stu-id="63ca5-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63ca5-123">標頭</span><span class="sxs-lookup"><span data-stu-id="63ca5-123">Header</span></span><br/>  | <dl> <span data-ttu-id="63ca5-124"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="63ca5-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="63ca5-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="63ca5-125">Library</span></span><br/> | <dl> <span data-ttu-id="63ca5-126"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="63ca5-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63ca5-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="63ca5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63ca5-128">ID3DX11EffectVectorVariable</span><span class="sxs-lookup"><span data-stu-id="63ca5-128">ID3DX11EffectVectorVariable</span></span>](id3dx11effectvectorvariable.md)
</dt> </dl>

 

