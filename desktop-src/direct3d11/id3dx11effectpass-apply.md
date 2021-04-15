---
title: 'ID3DX11EffectPass Apply 方法 (D3dx11effect. h) '
description: 將傳遞中包含的狀態設定為裝置。
ms.assetid: d67fe968-bfb2-4f3a-b393-3f72f680211f
keywords:
- Apply 方法 Direct3D 11
- Apply 方法 Direct3D 11，ID3DX11EffectPass 介面
- ID3DX11EffectPass 介面 Direct3D 11，Apply 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.Apply
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a061609953e164524e16722222a5ecea81f275b3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974544"
---
# <a name="id3dx11effectpassapply-method"></a><span data-ttu-id="a1660-106">ID3DX11EffectPass：： Apply 方法</span><span class="sxs-lookup"><span data-stu-id="a1660-106">ID3DX11EffectPass::Apply method</span></span>

<span data-ttu-id="a1660-107">將傳遞中包含的狀態設定為裝置。</span><span class="sxs-lookup"><span data-stu-id="a1660-107">Set the state contained in a pass to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1660-108">語法</span><span class="sxs-lookup"><span data-stu-id="a1660-108">Syntax</span></span>


```C++
HRESULT Apply(
   UINT                Flags,
   ID3D11DeviceContext *pContext
);
```



## <a name="parameters"></a><span data-ttu-id="a1660-109">參數</span><span class="sxs-lookup"><span data-stu-id="a1660-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1660-110">*旗標*</span><span class="sxs-lookup"><span data-stu-id="a1660-110">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="a1660-111">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="a1660-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="a1660-112">未使用的。</span><span class="sxs-lookup"><span data-stu-id="a1660-112">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="a1660-113">*pContext*</span><span class="sxs-lookup"><span data-stu-id="a1660-113">*pContext*</span></span> 
</dt> <dd>

<span data-ttu-id="a1660-114">類型： **[ **>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span><span class="sxs-lookup"><span data-stu-id="a1660-114">Type: **[**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***</span></span>

<span data-ttu-id="a1660-115">要套用傳遞的 [**>id3d11devicecoNtext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) 。</span><span class="sxs-lookup"><span data-stu-id="a1660-115">The [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) to apply the pass to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1660-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="a1660-116">Return value</span></span>

<span data-ttu-id="a1660-117">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a1660-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a1660-118">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="a1660-118">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a1660-119">備註</span><span class="sxs-lookup"><span data-stu-id="a1660-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a1660-120">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="a1660-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="a1660-121">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="a1660-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="a1660-122">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="a1660-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a1660-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1660-123">Requirements</span></span>



| <span data-ttu-id="a1660-124">需求</span><span class="sxs-lookup"><span data-stu-id="a1660-124">Requirement</span></span> | <span data-ttu-id="a1660-125">值</span><span class="sxs-lookup"><span data-stu-id="a1660-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1660-126">標頭</span><span class="sxs-lookup"><span data-stu-id="a1660-126">Header</span></span><br/>  | <dl> <span data-ttu-id="a1660-127"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="a1660-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="a1660-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="a1660-128">Library</span></span><br/> | <dl> <span data-ttu-id="a1660-129"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="a1660-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1660-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1660-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1660-131">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="a1660-131">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

