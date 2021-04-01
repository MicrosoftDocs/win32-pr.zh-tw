---
title: 'ID3DX11EffectRasterizerVariable UndoSetRasterizerState 方法 (D3dx11effect .h) '
description: 還原先前設定的轉譯器狀態。
ms.assetid: 2801479c-cb70-4950-9888-73e271b669aa
keywords:
- UndoSetRasterizerState 方法 Direct3D 11
- UndoSetRasterizerState 方法 Direct3D 11，ID3DX11EffectRasterizerVariable 介面
- ID3DX11EffectRasterizerVariable 介面 Direct3D 11，UndoSetRasterizerState 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.UndoSetRasterizerState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed05aa7380a1fb08bbd12d36328d33fa64fb7500
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196459"
---
# <a name="id3dx11effectrasterizervariableundosetrasterizerstate-method"></a><span data-ttu-id="80ac8-106">ID3DX11EffectRasterizerVariable：： UndoSetRasterizerState 方法</span><span class="sxs-lookup"><span data-stu-id="80ac8-106">ID3DX11EffectRasterizerVariable::UndoSetRasterizerState method</span></span>

<span data-ttu-id="80ac8-107">還原先前設定的轉譯器狀態。</span><span class="sxs-lookup"><span data-stu-id="80ac8-107">Reverts a previously set rasterizer state.</span></span>

## <a name="syntax"></a><span data-ttu-id="80ac8-108">語法</span><span class="sxs-lookup"><span data-stu-id="80ac8-108">Syntax</span></span>


```C++
HRESULT UndoSetRasterizerState(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="80ac8-109">參數</span><span class="sxs-lookup"><span data-stu-id="80ac8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80ac8-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="80ac8-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="80ac8-111">類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="80ac8-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="80ac8-112">在轉譯器介面陣列中編制索引。</span><span class="sxs-lookup"><span data-stu-id="80ac8-112">Index into an array of rasterizer interfaces.</span></span> <span data-ttu-id="80ac8-113">如果只有一個轉譯器介面，請使用0。</span><span class="sxs-lookup"><span data-stu-id="80ac8-113">If there is only one rasterizer interface, use 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80ac8-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="80ac8-114">Return value</span></span>

<span data-ttu-id="80ac8-115">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="80ac8-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="80ac8-116">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="80ac8-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="80ac8-117">備註</span><span class="sxs-lookup"><span data-stu-id="80ac8-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="80ac8-118">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="80ac8-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="80ac8-119">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="80ac8-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="80ac8-120">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="80ac8-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="80ac8-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="80ac8-121">Requirements</span></span>



| <span data-ttu-id="80ac8-122">需求</span><span class="sxs-lookup"><span data-stu-id="80ac8-122">Requirement</span></span> | <span data-ttu-id="80ac8-123">值</span><span class="sxs-lookup"><span data-stu-id="80ac8-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80ac8-124">標頭</span><span class="sxs-lookup"><span data-stu-id="80ac8-124">Header</span></span><br/>  | <dl> <span data-ttu-id="80ac8-125"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="80ac8-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="80ac8-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="80ac8-126">Library</span></span><br/> | <dl> <span data-ttu-id="80ac8-127"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="80ac8-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80ac8-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="80ac8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80ac8-129">ID3DX11EffectRasterizerVariable</span><span class="sxs-lookup"><span data-stu-id="80ac8-129">ID3DX11EffectRasterizerVariable</span></span>](id3dx11effectrasterizervariable.md)
</dt> </dl>

 

