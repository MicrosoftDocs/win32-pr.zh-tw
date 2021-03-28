---
title: 'ID3DX11EffectVectorVariable SetIntVectorArray 方法 (D3dx11effect .h) '
description: 設定包含整數資料之四個元件向量的陣列。
ms.assetid: c9e522d7-5545-4b91-b6b3-6fad9a151cb0
keywords:
- SetIntVectorArray 方法 Direct3D 11
- SetIntVectorArray 方法 Direct3D 11，ID3DX11EffectVectorVariable 介面
- ID3DX11EffectVectorVariable 介面 Direct3D 11，SetIntVectorArray 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.SetIntVectorArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7a450245c589feb41f7078120833cedc01c91d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946194"
---
# <a name="id3dx11effectvectorvariablesetintvectorarray-method"></a><span data-ttu-id="f5b05-106">ID3DX11EffectVectorVariable：： SetIntVectorArray 方法</span><span class="sxs-lookup"><span data-stu-id="f5b05-106">ID3DX11EffectVectorVariable::SetIntVectorArray method</span></span>

<span data-ttu-id="f5b05-107">設定包含整數資料之四個元件向量的陣列。</span><span class="sxs-lookup"><span data-stu-id="f5b05-107">Set an array of four-component vectors that contain integer data.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5b05-108">語法</span><span class="sxs-lookup"><span data-stu-id="f5b05-108">Syntax</span></span>


```C++
HRESULT SetIntVectorArray(
   int  *pData,
   UINT Offset,
   UINT Count
);
```



## <a name="parameters"></a><span data-ttu-id="f5b05-109">參數</span><span class="sxs-lookup"><span data-stu-id="f5b05-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5b05-110">*.Pdata*</span><span class="sxs-lookup"><span data-stu-id="f5b05-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="f5b05-111">類型： **[ **int**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="f5b05-111">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="f5b05-112">要設定之資料開頭的指標。</span><span class="sxs-lookup"><span data-stu-id="f5b05-112">A pointer to the start of the data to set.</span></span>

</dd> <dt>

<span data-ttu-id="f5b05-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="f5b05-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="f5b05-114">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f5b05-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f5b05-115">必須設為 0;這會保留供日後使用。</span><span class="sxs-lookup"><span data-stu-id="f5b05-115">Must be set to 0; this is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="f5b05-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="f5b05-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="f5b05-117">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f5b05-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f5b05-118">要設定的陣列元素數目。</span><span class="sxs-lookup"><span data-stu-id="f5b05-118">The number of array elements to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5b05-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="f5b05-119">Return value</span></span>

<span data-ttu-id="f5b05-120">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f5b05-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f5b05-121">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="f5b05-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f5b05-122">備註</span><span class="sxs-lookup"><span data-stu-id="f5b05-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f5b05-123">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="f5b05-123">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="f5b05-124">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="f5b05-124">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="f5b05-125">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="f5b05-125">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f5b05-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="f5b05-126">Requirements</span></span>



| <span data-ttu-id="f5b05-127">需求</span><span class="sxs-lookup"><span data-stu-id="f5b05-127">Requirement</span></span> | <span data-ttu-id="f5b05-128">值</span><span class="sxs-lookup"><span data-stu-id="f5b05-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5b05-129">標頭</span><span class="sxs-lookup"><span data-stu-id="f5b05-129">Header</span></span><br/>  | <dl> <span data-ttu-id="f5b05-130"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="f5b05-130"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="f5b05-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="f5b05-131">Library</span></span><br/> | <dl> <span data-ttu-id="f5b05-132"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="f5b05-132"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5b05-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f5b05-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5b05-134">ID3DX11EffectVectorVariable</span><span class="sxs-lookup"><span data-stu-id="f5b05-134">ID3DX11EffectVectorVariable</span></span>](id3dx11effectvectorvariable.md)
</dt> </dl>

 

