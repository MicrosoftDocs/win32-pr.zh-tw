---
title: 'ID3DX11EffectVariable IsValid 方法 (D3dx11effect .h) '
description: 比較資料類型與儲存的資料。
ms.assetid: 3384afa3-6ae5-4c7c-b95d-4fe3c87cc2fe
keywords:
- IsValid 方法 Direct3D 11
- IsValid 方法 Direct3D 11、ID3DX11EffectVariable 介面
- ID3DX11EffectVariable 介面 Direct3D 11，IsValid 方法
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5136005e675a6f5e54cc3863ef2d80ffadfb7c5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992349"
---
# <a name="id3dx11effectvariableisvalid-method"></a><span data-ttu-id="e1d07-106">ID3DX11EffectVariable：： IsValid 方法</span><span class="sxs-lookup"><span data-stu-id="e1d07-106">ID3DX11EffectVariable::IsValid method</span></span>

<span data-ttu-id="e1d07-107">比較資料類型與儲存的資料。</span><span class="sxs-lookup"><span data-stu-id="e1d07-107">Compare the data type with the data stored.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1d07-108">語法</span><span class="sxs-lookup"><span data-stu-id="e1d07-108">Syntax</span></span>


```C++
BOOL IsValid();
```



## <a name="parameters"></a><span data-ttu-id="e1d07-109">參數</span><span class="sxs-lookup"><span data-stu-id="e1d07-109">Parameters</span></span>

<span data-ttu-id="e1d07-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="e1d07-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e1d07-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e1d07-111">Return value</span></span>

<span data-ttu-id="e1d07-112">類型： **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="e1d07-112">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="e1d07-113">如果語法有效，則 **為 TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="e1d07-113">**TRUE** if the syntax is valid; otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1d07-114">備註</span><span class="sxs-lookup"><span data-stu-id="e1d07-114">Remarks</span></span>

<span data-ttu-id="e1d07-115">這個方法會檢查資料類型是否符合將某個介面轉換成 (另一個介面之後所儲存的資料，) 使用任何 As 方法。</span><span class="sxs-lookup"><span data-stu-id="e1d07-115">This method checks that the data type matches the data stored after casting one interface to another (using any of the As methods).</span></span>

> [!Note]  
> <span data-ttu-id="e1d07-116">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="e1d07-116">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="e1d07-117">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="e1d07-117">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="e1d07-118">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="e1d07-118">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e1d07-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="e1d07-119">Requirements</span></span>



| <span data-ttu-id="e1d07-120">需求</span><span class="sxs-lookup"><span data-stu-id="e1d07-120">Requirement</span></span> | <span data-ttu-id="e1d07-121">值</span><span class="sxs-lookup"><span data-stu-id="e1d07-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1d07-122">標頭</span><span class="sxs-lookup"><span data-stu-id="e1d07-122">Header</span></span><br/>  | <dl> <span data-ttu-id="e1d07-123"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="e1d07-123"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e1d07-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="e1d07-124">Library</span></span><br/> | <dl> <span data-ttu-id="e1d07-125"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="e1d07-125"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1d07-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e1d07-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1d07-127">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="e1d07-127">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

