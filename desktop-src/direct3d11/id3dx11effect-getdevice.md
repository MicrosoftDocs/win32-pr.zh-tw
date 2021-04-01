---
title: 'ID3DX11Effect GetDevice 方法 (D3dx11effect .h) '
description: 取得建立效果的裝置。
ms.assetid: efcc0358-9842-46eb-a521-ea220ec18735
keywords:
- GetDevice 方法 Direct3D 11
- GetDevice 方法 Direct3D 11，ID3DX11Effect 介面
- ID3DX11Effect 介面 Direct3D 11，GetDevice 方法
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetDevice
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25317740cade8a937aeeeac29f5a608bb4a43931
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196390"
---
# <a name="id3dx11effectgetdevice-method"></a><span data-ttu-id="93be5-106">ID3DX11Effect：： GetDevice 方法</span><span class="sxs-lookup"><span data-stu-id="93be5-106">ID3DX11Effect::GetDevice method</span></span>

<span data-ttu-id="93be5-107">取得建立效果的裝置。</span><span class="sxs-lookup"><span data-stu-id="93be5-107">Get the device that created the effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="93be5-108">語法</span><span class="sxs-lookup"><span data-stu-id="93be5-108">Syntax</span></span>


```C++
HRESULT GetDevice(
   ID3D11Device **ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="93be5-109">參數</span><span class="sxs-lookup"><span data-stu-id="93be5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93be5-110">*ppDevice*</span><span class="sxs-lookup"><span data-stu-id="93be5-110">*ppDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="93be5-111">類型： **[ **ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\*\***</span><span class="sxs-lookup"><span data-stu-id="93be5-111">Type: **[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)\*\***</span></span>

<span data-ttu-id="93be5-112">[**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)的指標。</span><span class="sxs-lookup"><span data-stu-id="93be5-112">A pointer to an [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93be5-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="93be5-113">Return value</span></span>

<span data-ttu-id="93be5-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="93be5-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="93be5-115">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="93be5-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="93be5-116">備註</span><span class="sxs-lookup"><span data-stu-id="93be5-116">Remarks</span></span>

<span data-ttu-id="93be5-117">藉由呼叫 [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md)之類的函式，為特定裝置建立效果。</span><span class="sxs-lookup"><span data-stu-id="93be5-117">An effect is created for a specific device, by calling a function such as [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).</span></span>

> [!Note]  
> <span data-ttu-id="93be5-118">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="93be5-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="93be5-119">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="93be5-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="93be5-120">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="93be5-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="93be5-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="93be5-121">Requirements</span></span>



| <span data-ttu-id="93be5-122">需求</span><span class="sxs-lookup"><span data-stu-id="93be5-122">Requirement</span></span> | <span data-ttu-id="93be5-123">值</span><span class="sxs-lookup"><span data-stu-id="93be5-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93be5-124">標頭</span><span class="sxs-lookup"><span data-stu-id="93be5-124">Header</span></span><br/>  | <dl> <span data-ttu-id="93be5-125"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="93be5-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="93be5-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="93be5-126">Library</span></span><br/> | <dl> <span data-ttu-id="93be5-127"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="93be5-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93be5-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93be5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93be5-129">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="93be5-129">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

 





