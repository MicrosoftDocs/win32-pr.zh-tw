---
title: 'ID3DX11EffectScalarVariable SetBool 方法 (D3dx11effect .h) '
description: 設定布林值變數。
ms.assetid: b5385ed3-6e65-4d65-bb8e-835967e6f610
keywords:
- SetBool 方法 Direct3D 11
- SetBool 方法 Direct3D 11，ID3DX11EffectScalarVariable 介面
- ID3DX11EffectScalarVariable 介面 Direct3D 11，SetBool 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.SetBool
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e1d3670b3a41f47bf1b5ec7ac3d2fb93441e72f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974652"
---
# <a name="id3dx11effectscalarvariablesetbool-method"></a><span data-ttu-id="ce712-106">ID3DX11EffectScalarVariable：： SetBool 方法</span><span class="sxs-lookup"><span data-stu-id="ce712-106">ID3DX11EffectScalarVariable::SetBool method</span></span>

<span data-ttu-id="ce712-107">設定布林值變數。</span><span class="sxs-lookup"><span data-stu-id="ce712-107">Set a boolean variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce712-108">語法</span><span class="sxs-lookup"><span data-stu-id="ce712-108">Syntax</span></span>


```C++
HRESULT SetBool(
   BOOL Value
);
```



## <a name="parameters"></a><span data-ttu-id="ce712-109">參數</span><span class="sxs-lookup"><span data-stu-id="ce712-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce712-110">*值*</span><span class="sxs-lookup"><span data-stu-id="ce712-110">*Value*</span></span> 
</dt> <dd>

<span data-ttu-id="ce712-111">類型： **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ce712-111">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ce712-112">變數的指標。</span><span class="sxs-lookup"><span data-stu-id="ce712-112">A pointer to the variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce712-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ce712-113">Return value</span></span>

<span data-ttu-id="ce712-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ce712-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ce712-115">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="ce712-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ce712-116">備註</span><span class="sxs-lookup"><span data-stu-id="ce712-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ce712-117">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="ce712-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="ce712-118">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="ce712-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="ce712-119">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="ce712-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ce712-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="ce712-120">Requirements</span></span>



| <span data-ttu-id="ce712-121">需求</span><span class="sxs-lookup"><span data-stu-id="ce712-121">Requirement</span></span> | <span data-ttu-id="ce712-122">值</span><span class="sxs-lookup"><span data-stu-id="ce712-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce712-123">標頭</span><span class="sxs-lookup"><span data-stu-id="ce712-123">Header</span></span><br/>  | <dl> <span data-ttu-id="ce712-124"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="ce712-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="ce712-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="ce712-125">Library</span></span><br/> | <dl> <span data-ttu-id="ce712-126"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="ce712-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce712-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ce712-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce712-128">ID3DX11EffectScalarVariable</span><span class="sxs-lookup"><span data-stu-id="ce712-128">ID3DX11EffectScalarVariable</span></span>](id3dx11effectscalarvariable.md)
</dt> </dl>

 

