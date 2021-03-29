---
title: 'ID3DX11EffectScalarVariable SetInt 方法 (D3dx11effect .h) '
description: 設定整數變數。
ms.assetid: 614284be-8f70-4d7e-b797-b67e813615ab
keywords:
- SetInt 方法 Direct3D 11
- SetInt 方法 Direct3D 11，ID3DX11EffectScalarVariable 介面
- ID3DX11EffectScalarVariable 介面 Direct3D 11，SetInt 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.SetInt
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b4e2f44a3b67db12bd84f5dd23426c033b99b57
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196191"
---
# <a name="id3dx11effectscalarvariablesetint-method"></a><span data-ttu-id="b4fec-106">ID3DX11EffectScalarVariable：： SetInt 方法</span><span class="sxs-lookup"><span data-stu-id="b4fec-106">ID3DX11EffectScalarVariable::SetInt method</span></span>

<span data-ttu-id="b4fec-107">設定整數變數。</span><span class="sxs-lookup"><span data-stu-id="b4fec-107">Set an integer variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4fec-108">語法</span><span class="sxs-lookup"><span data-stu-id="b4fec-108">Syntax</span></span>


```C++
HRESULT SetInt(
   int Value
);
```



## <a name="parameters"></a><span data-ttu-id="b4fec-109">參數</span><span class="sxs-lookup"><span data-stu-id="b4fec-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4fec-110">*值*</span><span class="sxs-lookup"><span data-stu-id="b4fec-110">*Value*</span></span> 
</dt> <dd>

<span data-ttu-id="b4fec-111">類型： **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b4fec-111">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b4fec-112">變數的指標。</span><span class="sxs-lookup"><span data-stu-id="b4fec-112">A pointer to the variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4fec-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="b4fec-113">Return value</span></span>

<span data-ttu-id="b4fec-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b4fec-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b4fec-115">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="b4fec-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b4fec-116">備註</span><span class="sxs-lookup"><span data-stu-id="b4fec-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b4fec-117">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="b4fec-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="b4fec-118">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="b4fec-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="b4fec-119">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="b4fec-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b4fec-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="b4fec-120">Requirements</span></span>



| <span data-ttu-id="b4fec-121">需求</span><span class="sxs-lookup"><span data-stu-id="b4fec-121">Requirement</span></span> | <span data-ttu-id="b4fec-122">值</span><span class="sxs-lookup"><span data-stu-id="b4fec-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4fec-123">標頭</span><span class="sxs-lookup"><span data-stu-id="b4fec-123">Header</span></span><br/>  | <dl> <span data-ttu-id="b4fec-124"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="b4fec-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="b4fec-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="b4fec-125">Library</span></span><br/> | <dl> <span data-ttu-id="b4fec-126"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="b4fec-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4fec-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b4fec-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4fec-128">ID3DX11EffectScalarVariable</span><span class="sxs-lookup"><span data-stu-id="b4fec-128">ID3DX11EffectScalarVariable</span></span>](id3dx11effectscalarvariable.md)
</dt> </dl>

 

