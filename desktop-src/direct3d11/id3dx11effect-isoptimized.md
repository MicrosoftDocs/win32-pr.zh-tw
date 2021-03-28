---
title: 'ID3DX11Effect IsOptimized 方法 (D3dx11effect .h) '
description: 測試效果，以查看反映中繼資料是否已從記憶體中移除。
ms.assetid: fb0a876b-7419-45b7-97fe-8352dd97d8c5
keywords:
- IsOptimized 方法 Direct3D 11
- IsOptimized 方法 Direct3D 11，ID3DX11Effect 介面
- ID3DX11Effect 介面 Direct3D 11，IsOptimized 方法
topic_type:
- apiref
api_name:
- ID3DX11Effect.IsOptimized
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18be8901a58715e3bd8aaaa49ae40be07e7e9dc8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323192"
---
# <a name="id3dx11effectisoptimized-method"></a><span data-ttu-id="88750-106">ID3DX11Effect：： IsOptimized 方法</span><span class="sxs-lookup"><span data-stu-id="88750-106">ID3DX11Effect::IsOptimized method</span></span>

<span data-ttu-id="88750-107">測試效果，以查看反映中繼資料是否已從記憶體中移除。</span><span class="sxs-lookup"><span data-stu-id="88750-107">Test an effect to see if the reflection metadata has been removed from memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="88750-108">語法</span><span class="sxs-lookup"><span data-stu-id="88750-108">Syntax</span></span>


```C++
BOOL IsOptimized();
```



## <a name="parameters"></a><span data-ttu-id="88750-109">參數</span><span class="sxs-lookup"><span data-stu-id="88750-109">Parameters</span></span>

<span data-ttu-id="88750-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="88750-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="88750-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="88750-111">Return value</span></span>

<span data-ttu-id="88750-112">類型： **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="88750-112">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="88750-113">如果效果已優化，則為 **TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="88750-113">**TRUE** if the effect is optimized; otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="88750-114">備註</span><span class="sxs-lookup"><span data-stu-id="88750-114">Remarks</span></span>

<span data-ttu-id="88750-115">效果會使用兩種不同方式的記憶體空間：儲存執行時間執行效果所需的資訊，以及儲存使用 API 將資訊反映回應用程式所需的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="88750-115">An effect uses memory space two different ways: to store the information required by the runtime to execute an effect, and to store the metadata required to reflect information back to an application using the API.</span></span> <span data-ttu-id="88750-116">您可以藉由呼叫 [**ID3DX11Effect：： Optimize**](id3dx11effect-optimize.md) 來將反映中繼資料從記憶體中移除，以將效果所需的記憶體數量降到最低。</span><span class="sxs-lookup"><span data-stu-id="88750-116">You can minimize the amount of memory required by an effect by calling [**ID3DX11Effect::Optimize**](id3dx11effect-optimize.md) which removes the reflection metadata from memory.</span></span> <span data-ttu-id="88750-117">當然，將反映資料移除之後，讀取變數的 API 方法將無法再運作。</span><span class="sxs-lookup"><span data-stu-id="88750-117">Of course, API methods to read variables will no longer work once reflection data has been removed.</span></span>

> [!Note]  
> <span data-ttu-id="88750-118">DirectX SDK 不提供任何已編譯的二進位檔來產生效果。</span><span class="sxs-lookup"><span data-stu-id="88750-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="88750-119">您必須使用效果11來源來建立效果類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="88750-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="88750-120">如需使用效果11來源的詳細資訊，請參閱 [效果的差異10和效果 11](d3d11-graphics-programming-guide-effects-differences.md)。</span><span class="sxs-lookup"><span data-stu-id="88750-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="88750-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="88750-121">Requirements</span></span>



| <span data-ttu-id="88750-122">需求</span><span class="sxs-lookup"><span data-stu-id="88750-122">Requirement</span></span> | <span data-ttu-id="88750-123">值</span><span class="sxs-lookup"><span data-stu-id="88750-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88750-124">標頭</span><span class="sxs-lookup"><span data-stu-id="88750-124">Header</span></span><br/>  | <dl> <span data-ttu-id="88750-125"><dt>D3dx11effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="88750-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="88750-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="88750-126">Library</span></span><br/> | <dl> <span data-ttu-id="88750-127"><dt>N/A (效果11程式庫可在線上作為共用來源使用。 ) </dt></span><span class="sxs-lookup"><span data-stu-id="88750-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88750-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="88750-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88750-129">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="88750-129">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

