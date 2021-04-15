---
description: 預先計算 Radiance 傳輸 (的回呼函式 PRT) 模擬和壓縮。
ms.assetid: 1d7e2149-d2ca-47da-be1f-8273fd9bd30a
title: LPD3DXSHPRTSIMCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 895d6fd3a7d9f93e858c08d1aaae416f1bf3abad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467783"
---
# <a name="lpd3dxshprtsimcb"></a><span data-ttu-id="fa0e3-103">LPD3DXSHPRTSIMCB</span><span class="sxs-lookup"><span data-stu-id="fa0e3-103">LPD3DXSHPRTSIMCB</span></span>

<span data-ttu-id="fa0e3-104">預先計算 Radiance 傳輸 (的回呼函式 PRT) 模擬和壓縮。</span><span class="sxs-lookup"><span data-stu-id="fa0e3-104">Callback function for Precomputed Radiance Transfer (PRT) simulation and compression.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa0e3-105">語法</span><span class="sxs-lookup"><span data-stu-id="fa0e3-105">Syntax</span></span>


```
typedef HRESULT (WINAPI *LPD3DXSHPRTSIMCB)(
    FLOAT fPercentDone,
    LPVOID lpUserContext
);
```



## <a name="parameters"></a><span data-ttu-id="fa0e3-106">參數</span><span class="sxs-lookup"><span data-stu-id="fa0e3-106">Parameters</span></span>

<span data-ttu-id="fa0e3-107">fPercentDone-介於0和1.0 之間的浮點數，代表已完成的計算百分比 (介於0到 100%) 之間。</span><span class="sxs-lookup"><span data-stu-id="fa0e3-107">fPercentDone - Floating point number between 0 and 1.0 that represents the percentage of calculations completed (between 0 and 100 percent).</span></span>

<span data-ttu-id="fa0e3-108">lpUserCoNtext-傳遞給回呼函式的使用者定義值指標;通常由應用程式用來傳遞資料結構的指標，以提供回呼函數的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="fa0e3-108">lpUserContext - Pointer to a user-defined value which is passed to the callback function; typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

## <a name="return-value"></a><span data-ttu-id="fa0e3-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="fa0e3-109">Return Value</span></span>

<span data-ttu-id="fa0e3-110">必須實作為此函式，才能 \_ 讓執行模擬器的正常運作。</span><span class="sxs-lookup"><span data-stu-id="fa0e3-110">This function must be implemented to return S\_OK to keep running the simulator.</span></span> <span data-ttu-id="fa0e3-111">任何其他值都會終止模擬器。</span><span class="sxs-lookup"><span data-stu-id="fa0e3-111">Any other value will halt the simulator.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa0e3-112">備註</span><span class="sxs-lookup"><span data-stu-id="fa0e3-112">Remarks</span></span>

<span data-ttu-id="fa0e3-113">宣告回呼函數時，請務必指定 [**Windows 資料類型**](../winprog/windows-data-types.md) 呼叫慣例。</span><span class="sxs-lookup"><span data-stu-id="fa0e3-113">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="fa0e3-114">否則，可能會發生堆疊溢位。</span><span class="sxs-lookup"><span data-stu-id="fa0e3-114">Otherwise, stack overflows can occur.</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="fa0e3-115">標頭</span><span class="sxs-lookup"><span data-stu-id="fa0e3-115">Header</span></span>                   | <span data-ttu-id="fa0e3-116">d3dx9mesh。h</span><span class="sxs-lookup"><span data-stu-id="fa0e3-116">d3dx9mesh.h</span></span> |
| <span data-ttu-id="fa0e3-117">匯入程式庫</span><span class="sxs-lookup"><span data-stu-id="fa0e3-117">Import Library</span></span>           | <span data-ttu-id="fa0e3-118">d3dx9 .lib</span><span class="sxs-lookup"><span data-stu-id="fa0e3-118">d3dx9.lib</span></span>   |
| <span data-ttu-id="fa0e3-119">最低作業系統</span><span class="sxs-lookup"><span data-stu-id="fa0e3-119">Minimum Operating System</span></span> | <span data-ttu-id="fa0e3-120">Windows 98</span><span class="sxs-lookup"><span data-stu-id="fa0e3-120">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="fa0e3-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="fa0e3-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa0e3-122">回呼函式</span><span class="sxs-lookup"><span data-stu-id="fa0e3-122">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
