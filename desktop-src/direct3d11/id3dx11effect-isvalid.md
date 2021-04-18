---
title: 'ID3DX11Effect IsValid 方法 (D3dx11effect .h) '
description: '測試效果，以查看它是否包含有效的語法。 |ID3DX11Effect IsValid 方法 (D3dx11effect .h) '
ms.assetid: 42bf0069-1828-4f55-99f5-d0f81eb04336
keywords:
- IsValid 方法 Direct3D 11
- IsValid 方法 Direct3D 11、ID3DX11Effect 介面
- ID3DX11Effect 介面 Direct3D 11，IsValid 方法
topic_type:
- apiref
api_name:
- ID3DX11Effect.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea88aef9e3864fc77380b3459860178c8537a6a5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992334"
---
# <a name="id3dx11effectisvalid-method"></a><span data-ttu-id="18656-107">ID3DX11Effect：： IsValid 方法</span><span class="sxs-lookup"><span data-stu-id="18656-107">ID3DX11Effect::IsValid method</span></span>

<span data-ttu-id="18656-108">測試效果，以查看它是否包含有效的語法。</span><span class="sxs-lookup"><span data-stu-id="18656-108">Test an effect to see if it contains valid syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="18656-109">語法</span><span class="sxs-lookup"><span data-stu-id="18656-109">Syntax</span></span>


```C++
BOOL IsValid();
```



## <a name="parameters"></a><span data-ttu-id="18656-110">參數</span><span class="sxs-lookup"><span data-stu-id="18656-110">Parameters</span></span>

<span data-ttu-id="18656-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="18656-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="18656-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="18656-112">Return value</span></span>

<span data-ttu-id="18656-113">類型： **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="18656-113">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="18656-114">如果程式碼語法有效，則 **為 TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="18656-114">**TRUE** if the code syntax is valid; otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="18656-115">備註</span><span class="sxs-lookup"><span data-stu-id="18656-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="18656-116">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="18656-116">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="18656-117">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="18656-117">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="18656-118">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="18656-118">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="18656-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="18656-119">Requirements</span></span>



| <span data-ttu-id="18656-120">需求</span><span class="sxs-lookup"><span data-stu-id="18656-120">Requirement</span></span> | <span data-ttu-id="18656-121">值</span><span class="sxs-lookup"><span data-stu-id="18656-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18656-122">標頭</span><span class="sxs-lookup"><span data-stu-id="18656-122">Header</span></span><br/>  | <dl> <span data-ttu-id="18656-123"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="18656-123"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="18656-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="18656-124">Library</span></span><br/> | <dl> <span data-ttu-id="18656-125"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="18656-125"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18656-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18656-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18656-127">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="18656-127">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

