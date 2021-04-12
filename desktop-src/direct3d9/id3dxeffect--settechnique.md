---
description: 設定使用中的技術。
ms.assetid: 18f19773-a9f8-47f9-9334-acc95e0f0eb7
title: 'ID3DXEffect：： SetTechnique 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.SetTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e93fbff9eb74e8885675b7ccf4ea69cc53d5da53
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946058"
---
# <a name="id3dxeffectsettechnique-method"></a><span data-ttu-id="c9b5a-103">ID3DXEffect：： SetTechnique 方法</span><span class="sxs-lookup"><span data-stu-id="c9b5a-103">ID3DXEffect::SetTechnique method</span></span>

<span data-ttu-id="c9b5a-104">設定使用中的技術。</span><span class="sxs-lookup"><span data-stu-id="c9b5a-104">Sets the active technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9b5a-105">語法</span><span class="sxs-lookup"><span data-stu-id="c9b5a-105">Syntax</span></span>


```C++
HRESULT SetTechnique(
  [in] D3DXHANDLE hTechnique
);
```



## <a name="parameters"></a><span data-ttu-id="c9b5a-106">參數</span><span class="sxs-lookup"><span data-stu-id="c9b5a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9b5a-107">*hTechnique* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c9b5a-107">*hTechnique* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9b5a-108">類型： **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="c9b5a-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="c9b5a-109">技術的獨特控制碼。</span><span class="sxs-lookup"><span data-stu-id="c9b5a-109">Unique handle to the technique.</span></span> <span data-ttu-id="c9b5a-110">請參閱 [處理 (Direct3D 9) ](handles.md)。</span><span class="sxs-lookup"><span data-stu-id="c9b5a-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9b5a-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c9b5a-111">Return value</span></span>

<span data-ttu-id="c9b5a-112">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c9b5a-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c9b5a-113">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="c9b5a-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c9b5a-114">如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="c9b5a-114">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9b5a-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9b5a-115">Requirements</span></span>



| <span data-ttu-id="c9b5a-116">需求</span><span class="sxs-lookup"><span data-stu-id="c9b5a-116">Requirement</span></span> | <span data-ttu-id="c9b5a-117">值</span><span class="sxs-lookup"><span data-stu-id="c9b5a-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9b5a-118">標頭</span><span class="sxs-lookup"><span data-stu-id="c9b5a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="c9b5a-119"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="c9b5a-119"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="c9b5a-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="c9b5a-120">Library</span></span><br/> | <dl> <span data-ttu-id="c9b5a-121"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c9b5a-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c9b5a-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9b5a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9b5a-123">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="c9b5a-123">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 




