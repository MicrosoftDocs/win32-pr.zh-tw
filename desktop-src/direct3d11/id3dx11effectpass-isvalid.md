---
title: 'ID3DX11EffectPass IsValid 方法 (D3dx11effect .h) '
description: 測試 pass 以查看它是否包含有效的語法。
ms.assetid: 3c6ddcef-1303-4161-889c-c3ca271b6ad0
keywords:
- IsValid 方法 Direct3D 11
- IsValid 方法 Direct3D 11、ID3DX11EffectPass 介面
- ID3DX11EffectPass 介面 Direct3D 11，IsValid 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50db900d3cea82197fb56ce3a57a5a548220ca1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974540"
---
# <a name="id3dx11effectpassisvalid-method"></a><span data-ttu-id="6ec53-106">ID3DX11EffectPass：： IsValid 方法</span><span class="sxs-lookup"><span data-stu-id="6ec53-106">ID3DX11EffectPass::IsValid method</span></span>

<span data-ttu-id="6ec53-107">測試 pass 以查看它是否包含有效的語法。</span><span class="sxs-lookup"><span data-stu-id="6ec53-107">Test a pass to see if it contains valid syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ec53-108">語法</span><span class="sxs-lookup"><span data-stu-id="6ec53-108">Syntax</span></span>


```C++
BOOL IsValid();
```



## <a name="parameters"></a><span data-ttu-id="6ec53-109">參數</span><span class="sxs-lookup"><span data-stu-id="6ec53-109">Parameters</span></span>

<span data-ttu-id="6ec53-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="6ec53-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6ec53-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6ec53-111">Return value</span></span>

<span data-ttu-id="6ec53-112">類型： **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="6ec53-112">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="6ec53-113">如果程式碼語法有效，則 **為 TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="6ec53-113">**TRUE** if the code syntax is valid; otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ec53-114">備註</span><span class="sxs-lookup"><span data-stu-id="6ec53-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6ec53-115">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="6ec53-115">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="6ec53-116">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="6ec53-116">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="6ec53-117">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="6ec53-117">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6ec53-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ec53-118">Requirements</span></span>



| <span data-ttu-id="6ec53-119">需求</span><span class="sxs-lookup"><span data-stu-id="6ec53-119">Requirement</span></span> | <span data-ttu-id="6ec53-120">值</span><span class="sxs-lookup"><span data-stu-id="6ec53-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec53-121">標頭</span><span class="sxs-lookup"><span data-stu-id="6ec53-121">Header</span></span><br/>  | <dl> <span data-ttu-id="6ec53-122"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="6ec53-122"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="6ec53-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="6ec53-123">Library</span></span><br/> | <dl> <span data-ttu-id="6ec53-124"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="6ec53-124"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ec53-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6ec53-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ec53-126">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="6ec53-126">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

