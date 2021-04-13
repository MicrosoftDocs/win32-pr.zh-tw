---
title: D3DPERF_GetStatus 函式
description: 從目的程式判斷 profiler 的目前狀態。
ms.localizationpriority: low
ms.topic: reference
ms.date: 04/06/2020
req.lib: d3d9.lib
req.dll: d3d9.dll
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- d3d9.dll
api_name:
- D3DPERF_GetStatus
targetos: Windows
ms.openlocfilehash: 626d56dd449b0a0aa92e85c82dabda119900680d
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/08/2020
ms.locfileid: "104314466"
---
# <a name="d3dperf_getstatus-function"></a><span data-ttu-id="53d04-103">D3DPERF_GetStatus 函式</span><span class="sxs-lookup"><span data-stu-id="53d04-103">D3DPERF_GetStatus function</span></span>

<span data-ttu-id="53d04-104">從目的程式判斷 profiler 的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="53d04-104">Determine the current state of the profiler from the target program.</span></span>

## <a name="syntax"></a><span data-ttu-id="53d04-105">語法</span><span class="sxs-lookup"><span data-stu-id="53d04-105">Syntax</span></span>

```cpp
DWORD WINAPI D3DPERF_GetStatus( void );
```

## <a name="return-value"></a><span data-ttu-id="53d04-106">傳回值</span><span class="sxs-lookup"><span data-stu-id="53d04-106">Return value</span></span>

<span data-ttu-id="53d04-107">當 PIX 正在分析目的程式時，非零值;否則為零。</span><span class="sxs-lookup"><span data-stu-id="53d04-107">A non-zero value when PIX is profiling the target program; otherwise, zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="53d04-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="53d04-108">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="53d04-109">**目標平台**</span><span class="sxs-lookup"><span data-stu-id="53d04-109">**Target Platform**</span></span> | <span data-ttu-id="53d04-110">Windows</span><span class="sxs-lookup"><span data-stu-id="53d04-110">Windows</span></span> |
| <span data-ttu-id="53d04-111">**標頭**</span><span class="sxs-lookup"><span data-stu-id="53d04-111">**Header**</span></span> | <span data-ttu-id="53d04-112">d3d9。h</span><span class="sxs-lookup"><span data-stu-id="53d04-112">d3d9.h</span></span> |
| <span data-ttu-id="53d04-113">**程式庫**</span><span class="sxs-lookup"><span data-stu-id="53d04-113">**Library**</span></span> | <span data-ttu-id="53d04-114">d3d9 .lib</span><span class="sxs-lookup"><span data-stu-id="53d04-114">d3d9.lib</span></span> |
| <span data-ttu-id="53d04-115">**DLL**</span><span class="sxs-lookup"><span data-stu-id="53d04-115">**DLL**</span></span> | <span data-ttu-id="53d04-116">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="53d04-116">d3d9.dll</span></span> |