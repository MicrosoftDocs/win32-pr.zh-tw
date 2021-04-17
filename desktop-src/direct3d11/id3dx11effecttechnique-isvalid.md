---
title: 'ID3DX11EffectTechnique IsValid 方法 (D3dx11effect .h) '
description: 測試技術以查看其是否包含有效的語法。
ms.assetid: 599b191b-6307-4d36-b4e4-15a1ac36c65e
keywords:
- IsValid 方法 Direct3D 11
- IsValid 方法 Direct3D 11、ID3DX11EffectTechnique 介面
- ID3DX11EffectTechnique 介面 Direct3D 11，IsValid 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectTechnique.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6855e1dc1073eb2ebb4484eba1f03fe4130f0b2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386518"
---
# <a name="id3dx11effecttechniqueisvalid-method"></a><span data-ttu-id="b1529-106">ID3DX11EffectTechnique：： IsValid 方法</span><span class="sxs-lookup"><span data-stu-id="b1529-106">ID3DX11EffectTechnique::IsValid method</span></span>

<span data-ttu-id="b1529-107">測試技術以查看其是否包含有效的語法。</span><span class="sxs-lookup"><span data-stu-id="b1529-107">Test a technique to see if it contains valid syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1529-108">語法</span><span class="sxs-lookup"><span data-stu-id="b1529-108">Syntax</span></span>


```C++
BOOL IsValid();
```



## <a name="parameters"></a><span data-ttu-id="b1529-109">參數</span><span class="sxs-lookup"><span data-stu-id="b1529-109">Parameters</span></span>

<span data-ttu-id="b1529-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="b1529-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b1529-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b1529-111">Return value</span></span>

<span data-ttu-id="b1529-112">類型： **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b1529-112">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b1529-113">如果程式碼語法有效，則 **為 TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="b1529-113">**TRUE** if the code syntax is valid; otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1529-114">備註</span><span class="sxs-lookup"><span data-stu-id="b1529-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b1529-115">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="b1529-115">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="b1529-116">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="b1529-116">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="b1529-117">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="b1529-117">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b1529-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="b1529-118">Requirements</span></span>



| <span data-ttu-id="b1529-119">需求</span><span class="sxs-lookup"><span data-stu-id="b1529-119">Requirement</span></span> | <span data-ttu-id="b1529-120">值</span><span class="sxs-lookup"><span data-stu-id="b1529-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1529-121">標頭</span><span class="sxs-lookup"><span data-stu-id="b1529-121">Header</span></span><br/>  | <dl> <span data-ttu-id="b1529-122"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="b1529-122"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="b1529-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="b1529-123">Library</span></span><br/> | <dl> <span data-ttu-id="b1529-124"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="b1529-124"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1529-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b1529-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1529-126">ID3DX11EffectTechnique</span><span class="sxs-lookup"><span data-stu-id="b1529-126">ID3DX11EffectTechnique</span></span>](id3dx11effecttechnique.md)
</dt> </dl>

 

