---
description: UVAtlas 的回呼函數。
ms.assetid: a605ae27-10c9-49b4-98fe-8c788c2c0752
title: LPD3DXU加值稅LASCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfe073b5e6a798ccb74421d42502b089d59be11f
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342793"
---
# <a name="lpd3dxuvatlascb"></a><span data-ttu-id="f3020-103">LPD3DXU加值稅LASCB</span><span class="sxs-lookup"><span data-stu-id="f3020-103">LPD3DXUVATLASCB</span></span>

<span data-ttu-id="f3020-104">UVAtlas 的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="f3020-104">Callback function for UVAtlas.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3020-105">語法</span><span class="sxs-lookup"><span data-stu-id="f3020-105">Syntax</span></span>


```
typedef HRESULT (*LPD3DXUVATLASCB ( 
    FLOAT fPercentDone,
    LPVOID lpUserContext
);
```



## <a name="parameters"></a><span data-ttu-id="f3020-106">參數</span><span class="sxs-lookup"><span data-stu-id="f3020-106">Parameters</span></span>

<span data-ttu-id="f3020-107">\[out \] fPercentDone-介於0和1.0 之間的浮點數，代表已完成的計算百分比 (介於0到 100%) 之間。</span><span class="sxs-lookup"><span data-stu-id="f3020-107">\[out\] fPercentDone - Floating point number between 0 and 1.0 that represents the percentage of calculations completed (between 0 and 100 percent).</span></span>

<span data-ttu-id="f3020-108">\[在 lpUserCoNtext 中，指向 \] 傳遞給回呼函式的使用者定義值的指標; 通常由應用程式用來傳遞資料結構的指標，該結構會提供回呼函數的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="f3020-108">\[in\] lpUserContext - Pointer to a user-defined value which is passed to the callback function; typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

## <a name="return-value"></a><span data-ttu-id="f3020-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="f3020-109">Return Value</span></span>

<span data-ttu-id="f3020-110">必須實作為此函式，才能 \_ 讓執行模擬器的正常運作。</span><span class="sxs-lookup"><span data-stu-id="f3020-110">This function must be implemented to return S\_OK to keep running the simulator.</span></span> <span data-ttu-id="f3020-111">任何其他值都會終止模擬器。</span><span class="sxs-lookup"><span data-stu-id="f3020-111">Any other value will halt the simulator.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3020-112">備註</span><span class="sxs-lookup"><span data-stu-id="f3020-112">Remarks</span></span>

<span data-ttu-id="f3020-113">宣告回呼函數時，請務必指定 [**Windows 資料類型**](../winprog/windows-data-types.md) 呼叫慣例。</span><span class="sxs-lookup"><span data-stu-id="f3020-113">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="f3020-114">否則，可能會發生堆疊溢位。</span><span class="sxs-lookup"><span data-stu-id="f3020-114">Otherwise, stack overflows can occur.</span></span>



| <span data-ttu-id="f3020-115">需求</span><span class="sxs-lookup"><span data-stu-id="f3020-115">Requirement</span></span>                         | <span data-ttu-id="f3020-116">值</span><span class="sxs-lookup"><span data-stu-id="f3020-116">Value</span></span>            |
|--------------------------|-------------|
| <span data-ttu-id="f3020-117">標頭</span><span class="sxs-lookup"><span data-stu-id="f3020-117">Header</span></span>                   | <span data-ttu-id="f3020-118">d3dx9mesh。h</span><span class="sxs-lookup"><span data-stu-id="f3020-118">d3dx9mesh.h</span></span> |
| <span data-ttu-id="f3020-119">匯入程式庫</span><span class="sxs-lookup"><span data-stu-id="f3020-119">Import Library</span></span>           | <span data-ttu-id="f3020-120">d3dx9 .lib</span><span class="sxs-lookup"><span data-stu-id="f3020-120">d3dx9.lib</span></span>   |
| <span data-ttu-id="f3020-121">最低作業系統</span><span class="sxs-lookup"><span data-stu-id="f3020-121">Minimum Operating System</span></span> | <span data-ttu-id="f3020-122">Windows 98</span><span class="sxs-lookup"><span data-stu-id="f3020-122">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="f3020-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="f3020-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3020-124">回呼函式</span><span class="sxs-lookup"><span data-stu-id="f3020-124">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
