---
title: 'ID3DX11Effect Optimize 方法 (D3dx11effect) '
description: 將效果所需的記憶體數量降到最低。
ms.assetid: fa1d0769-6746-44f6-9979-31a534646884
keywords:
- 優化方法 Direct3D 11
- 優化方法 Direct3D 11，ID3DX11Effect 介面
- ID3DX11Effect 介面 Direct3D 11，Optimize 方法
topic_type:
- apiref
api_name:
- ID3DX11Effect.Optimize
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33fd6d200f6b22af46e648040e8299f40ec9ebae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104992331"
---
# <a name="id3dx11effectoptimize-method"></a><span data-ttu-id="4b177-106">ID3DX11Effect：： Optimize 方法</span><span class="sxs-lookup"><span data-stu-id="4b177-106">ID3DX11Effect::Optimize method</span></span>

<span data-ttu-id="4b177-107">將效果所需的記憶體數量降到最低。</span><span class="sxs-lookup"><span data-stu-id="4b177-107">Minimize the amount of memory required for an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b177-108">語法</span><span class="sxs-lookup"><span data-stu-id="4b177-108">Syntax</span></span>


```C++
HRESULT Optimize();
```



## <a name="parameters"></a><span data-ttu-id="4b177-109">參數</span><span class="sxs-lookup"><span data-stu-id="4b177-109">Parameters</span></span>

<span data-ttu-id="4b177-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="4b177-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4b177-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="4b177-111">Return value</span></span>

<span data-ttu-id="4b177-112">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4b177-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4b177-113">傳回下列其中一個 [Direct3D 11 傳回碼](d3d11-graphics-reference-returnvalues.md)。</span><span class="sxs-lookup"><span data-stu-id="4b177-113">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4b177-114">備註</span><span class="sxs-lookup"><span data-stu-id="4b177-114">Remarks</span></span>

<span data-ttu-id="4b177-115">效果會使用兩種不同方式的記憶體空間：儲存執行時間執行效果所需的資訊，以及儲存使用 API 將資訊反映回應用程式所需的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="4b177-115">An effect uses memory space two different ways: to store the information required by the runtime to execute an effect, and to store the metadata required to reflect information back to an application using the API.</span></span> <span data-ttu-id="4b177-116">您可以藉由呼叫 **ID3DX11Effect：： Optimize** 來將反映中繼資料從記憶體中移除，以將效果所需的記憶體數量降到最低。</span><span class="sxs-lookup"><span data-stu-id="4b177-116">You can minimize the amount of memory required by an effect by calling **ID3DX11Effect::Optimize** which removes the reflection metadata from memory.</span></span> <span data-ttu-id="4b177-117">移除反映資料之後，用來讀取變數的 API 方法將無法再運作。</span><span class="sxs-lookup"><span data-stu-id="4b177-117">API methods to read variables will no longer work once reflection data has been removed.</span></span>

<span data-ttu-id="4b177-118">在效果上呼叫 Optimize 之後，下列方法將會失敗。</span><span class="sxs-lookup"><span data-stu-id="4b177-118">The following methods will fail after Optimize has been called on an effect.</span></span>

-   [<span data-ttu-id="4b177-119">**ID3DX11Effect::GetConstantBufferByIndex**</span><span class="sxs-lookup"><span data-stu-id="4b177-119">**ID3DX11Effect::GetConstantBufferByIndex**</span></span>](id3dx11effect-getconstantbufferbyindex.md)
-   [<span data-ttu-id="4b177-120">**ID3DX11Effect::GetConstantBufferByName**</span><span class="sxs-lookup"><span data-stu-id="4b177-120">**ID3DX11Effect::GetConstantBufferByName**</span></span>](id3dx11effect-getconstantbufferbyname.md)
-   [<span data-ttu-id="4b177-121">**ID3DX11Effect::GetDesc**</span><span class="sxs-lookup"><span data-stu-id="4b177-121">**ID3DX11Effect::GetDesc**</span></span>](id3dx11effect-getdesc.md)
-   [<span data-ttu-id="4b177-122">**ID3DX11Effect：： GetDevice**</span><span class="sxs-lookup"><span data-stu-id="4b177-122">**ID3DX11Effect::GetDevice**</span></span>](id3dx11effect-getdevice.md)
-   [<span data-ttu-id="4b177-123">**ID3DX11Effect::GetTechniqueByIndex**</span><span class="sxs-lookup"><span data-stu-id="4b177-123">**ID3DX11Effect::GetTechniqueByIndex**</span></span>](id3dx11effect-gettechniquebyindex.md)
-   [<span data-ttu-id="4b177-124">**ID3DX11Effect::GetTechniqueByName**</span><span class="sxs-lookup"><span data-stu-id="4b177-124">**ID3DX11Effect::GetTechniqueByName**</span></span>](id3dx11effect-gettechniquebyname.md)
-   [<span data-ttu-id="4b177-125">**ID3DX11Effect::GetVariableByIndex**</span><span class="sxs-lookup"><span data-stu-id="4b177-125">**ID3DX11Effect::GetVariableByIndex**</span></span>](id3dx11effect-getvariablebyindex.md)
-   [<span data-ttu-id="4b177-126">**ID3DX11Effect::GetVariableByName**</span><span class="sxs-lookup"><span data-stu-id="4b177-126">**ID3DX11Effect::GetVariableByName**</span></span>](id3dx11effect-getvariablebyname.md)
-   [<span data-ttu-id="4b177-127">**ID3DX11Effect::GetVariableBySemantic**</span><span class="sxs-lookup"><span data-stu-id="4b177-127">**ID3DX11Effect::GetVariableBySemantic**</span></span>](id3dx11effect-getvariablebysemantic.md)

> [!Note]  
> <span data-ttu-id="4b177-128">在呼叫 **ID3DX11Effect：** ： optimize 之前，使用這些方法抓取的參考在呼叫 **ID3DX11Effect：： optimize** 之後仍有效。</span><span class="sxs-lookup"><span data-stu-id="4b177-128">References retrieved with these methods before calling **ID3DX11Effect::Optimize** are still valid after **ID3DX11Effect::Optimize** is called.</span></span> <span data-ttu-id="4b177-129">這可讓應用程式取得所有將使用的變數、技術和傳遞、呼叫 Optimize，然後使用效果。</span><span class="sxs-lookup"><span data-stu-id="4b177-129">This allows the application to get all the variables, techniques, and passes it will use, call Optimize, and then use the effect.</span></span>

 

> [!Note]  
> <span data-ttu-id="4b177-130">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="4b177-130">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="4b177-131">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="4b177-131">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="4b177-132">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="4b177-132">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4b177-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="4b177-133">Requirements</span></span>



| <span data-ttu-id="4b177-134">需求</span><span class="sxs-lookup"><span data-stu-id="4b177-134">Requirement</span></span> | <span data-ttu-id="4b177-135">值</span><span class="sxs-lookup"><span data-stu-id="4b177-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b177-136">標頭</span><span class="sxs-lookup"><span data-stu-id="4b177-136">Header</span></span><br/>  | <dl> <span data-ttu-id="4b177-137"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="4b177-137"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="4b177-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="4b177-138">Library</span></span><br/> | <dl> <span data-ttu-id="4b177-139"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="4b177-139"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b177-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4b177-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b177-141">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="4b177-141">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

 





