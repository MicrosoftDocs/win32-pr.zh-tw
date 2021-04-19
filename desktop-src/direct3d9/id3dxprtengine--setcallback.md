---
description: 設定選擇性回呼函式的指標，此函式會計算已完成的球面調和 (SH) 計算的百分比，並為呼叫端提供中止模擬器的選項。
ms.assetid: 0a47610d-fa4e-4094-9adb-4fd9306b8a12
title: 'ID3DXPRTEngine：： SetCallBack 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetCallBack
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e9c2cfe710bc41ff71267e381fa0bf576688f9df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992726"
---
# <a name="id3dxprtenginesetcallback-method"></a><span data-ttu-id="44fca-103">ID3DXPRTEngine：： SetCallBack 方法</span><span class="sxs-lookup"><span data-stu-id="44fca-103">ID3DXPRTEngine::SetCallBack method</span></span>

<span data-ttu-id="44fca-104">設定選擇性回呼函式的指標，此函式會計算已完成的球面調和 (SH) 計算的百分比，並為呼叫端提供中止模擬器的選項。</span><span class="sxs-lookup"><span data-stu-id="44fca-104">Sets a pointer to an optional callback function that computes the percentage of spherical harmonic (SH) computations completed and gives the caller the option of aborting the simulator.</span></span>

## <a name="syntax"></a><span data-ttu-id="44fca-105">語法</span><span class="sxs-lookup"><span data-stu-id="44fca-105">Syntax</span></span>


```C++
HRESULT SetCallBack(
  [in] LPD3DXSHPRTSIMCB pCB,
  [in] FLOAT            Frequency,
  [in] LPVOID           lpUserContext
);
```



## <a name="parameters"></a><span data-ttu-id="44fca-106">參數</span><span class="sxs-lookup"><span data-stu-id="44fca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44fca-107">*pCB* \[在\]</span><span class="sxs-lookup"><span data-stu-id="44fca-107">*pCB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44fca-108">類型： **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**</span><span class="sxs-lookup"><span data-stu-id="44fca-108">Type: **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**</span></span>

<span data-ttu-id="44fca-109">[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)回呼函式的指標，此函式會計算已完成的 SH 計算百分比。</span><span class="sxs-lookup"><span data-stu-id="44fca-109">Pointer to the [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) callback function that computes the percentage of SH computations completed.</span></span> <span data-ttu-id="44fca-110">必須實回呼函式，以傳回「 \_ 確定」，以繼續執行模擬器。</span><span class="sxs-lookup"><span data-stu-id="44fca-110">The callback function must be implemented to return S\_OK to keep running the simulator.</span></span> <span data-ttu-id="44fca-111">任何其他值都會中止模擬器。</span><span class="sxs-lookup"><span data-stu-id="44fca-111">Any other value will abort the simulator.</span></span>

</dd> <dt>

<span data-ttu-id="44fca-112">*頻率* \[在\]</span><span class="sxs-lookup"><span data-stu-id="44fca-112">*Frequency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44fca-113">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="44fca-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="44fca-114">回呼呼叫的頻率。</span><span class="sxs-lookup"><span data-stu-id="44fca-114">Frequency of callback calls.</span></span> <span data-ttu-id="44fca-115">頻率的反函數大約是回呼函數的呼叫次數。</span><span class="sxs-lookup"><span data-stu-id="44fca-115">The inverse of Frequency is approximately the number of times the callback function will be called.</span></span>

</dd> <dt>

<span data-ttu-id="44fca-116">*lpUserCoNtext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="44fca-116">*lpUserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44fca-117">類型： **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="44fca-117">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="44fca-118">傳遞給回呼函式的使用者定義值的指標。</span><span class="sxs-lookup"><span data-stu-id="44fca-118">Pointer to a user-defined value which is passed to the callback function.</span></span> <span data-ttu-id="44fca-119">通常由應用程式用來傳遞資料結構的指標，以提供回呼函數的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="44fca-119">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44fca-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="44fca-120">Return value</span></span>

<span data-ttu-id="44fca-121">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="44fca-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="44fca-122">傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="44fca-122">The return value is S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="44fca-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="44fca-123">Requirements</span></span>



| <span data-ttu-id="44fca-124">需求</span><span class="sxs-lookup"><span data-stu-id="44fca-124">Requirement</span></span> | <span data-ttu-id="44fca-125">值</span><span class="sxs-lookup"><span data-stu-id="44fca-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="44fca-126">標頭</span><span class="sxs-lookup"><span data-stu-id="44fca-126">Header</span></span><br/>  | <dl> <span data-ttu-id="44fca-127"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="44fca-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="44fca-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="44fca-128">Library</span></span><br/> | <dl> <span data-ttu-id="44fca-129"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="44fca-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="44fca-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="44fca-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44fca-131">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="44fca-131">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
