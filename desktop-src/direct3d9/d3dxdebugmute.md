---
description: 開啟或關閉所有 D3DX 的調試輸出。
ms.assetid: e35cbfd2-401e-47ec-9f5b-e2ed63ea1fcd
title: 'D3DXDebugMute 函式 (D3dx9core) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDebugMute
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9259fa43a6a64829e42cbaa661aa7223a958f22d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196263"
---
# <a name="d3dxdebugmute-function"></a><span data-ttu-id="68f1c-103">D3DXDebugMute 函式</span><span class="sxs-lookup"><span data-stu-id="68f1c-103">D3DXDebugMute function</span></span>

<span data-ttu-id="68f1c-104">開啟或關閉所有 D3DX 的調試輸出。</span><span class="sxs-lookup"><span data-stu-id="68f1c-104">Turns on or off all D3DX debug output.</span></span>

## <a name="syntax"></a><span data-ttu-id="68f1c-105">語法</span><span class="sxs-lookup"><span data-stu-id="68f1c-105">Syntax</span></span>


```C++
BOOL D3DXDebugMute(
  _In_ BOOL Mute
);
```



## <a name="parameters"></a><span data-ttu-id="68f1c-106">參數</span><span class="sxs-lookup"><span data-stu-id="68f1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68f1c-107">*靜音* \[在\]</span><span class="sxs-lookup"><span data-stu-id="68f1c-107">*Mute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68f1c-108">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="68f1c-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="68f1c-109">若 **為 TRUE**，則會停止偵錯工具輸出;如果 **為 FALSE**，則表示已啟用偵錯工具輸出。</span><span class="sxs-lookup"><span data-stu-id="68f1c-109">If **TRUE**, debugger output is halted; if **FALSE**, debug output is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68f1c-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="68f1c-110">Return value</span></span>

<span data-ttu-id="68f1c-111">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="68f1c-111">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="68f1c-112">傳回前一個靜音值。</span><span class="sxs-lookup"><span data-stu-id="68f1c-112">Returns the previous value of Mute.</span></span>

## <a name="requirements"></a><span data-ttu-id="68f1c-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="68f1c-113">Requirements</span></span>



| <span data-ttu-id="68f1c-114">需求</span><span class="sxs-lookup"><span data-stu-id="68f1c-114">Requirement</span></span> | <span data-ttu-id="68f1c-115">值</span><span class="sxs-lookup"><span data-stu-id="68f1c-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68f1c-116">標頭</span><span class="sxs-lookup"><span data-stu-id="68f1c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="68f1c-117"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="68f1c-117"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="68f1c-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="68f1c-118">Library</span></span><br/> | <dl> <span data-ttu-id="68f1c-119"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="68f1c-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="68f1c-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="68f1c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68f1c-121">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="68f1c-121">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
