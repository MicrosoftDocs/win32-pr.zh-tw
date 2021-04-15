---
title: D3DPERF_SetOptions 函式
description: 設定目的程式所指定的 profiler 選項。
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
- D3DPERF_SetOptions
targetos: Windows
ms.openlocfilehash: 8bd877469864ccdaa833ce80d00eb06ae5fc18de
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/08/2020
ms.locfileid: "104462753"
---
# <a name="d3dperf_setoptions-function"></a><span data-ttu-id="976dd-103">D3DPERF_SetOptions 函式</span><span class="sxs-lookup"><span data-stu-id="976dd-103">D3DPERF_SetOptions function</span></span>

<span data-ttu-id="976dd-104">設定目的程式所指定的 profiler 選項。</span><span class="sxs-lookup"><span data-stu-id="976dd-104">Set profiler options specified by the target program.</span></span>

## <a name="syntax"></a><span data-ttu-id="976dd-105">語法</span><span class="sxs-lookup"><span data-stu-id="976dd-105">Syntax</span></span>

```cpp
int WINAPI D3DPERF_SetOptions(
  DWORD dwOptions
);
```

## <a name="parameters"></a><span data-ttu-id="976dd-106">參數</span><span class="sxs-lookup"><span data-stu-id="976dd-106">Parameters</span></span>

`dwOptions`

<span data-ttu-id="976dd-107">PIX 可辨識的使用者選項。</span><span class="sxs-lookup"><span data-stu-id="976dd-107">User options recognizable by PIX.</span></span> <span data-ttu-id="976dd-108">將此設定為1，以通知 PIX 目的程式未提供要分析的許可權。</span><span class="sxs-lookup"><span data-stu-id="976dd-108">Set this to 1 to notify PIX that the target program does not give permission to be profiled.</span></span>

## <a name="return-value"></a><span data-ttu-id="976dd-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="976dd-109">Return value</span></span>

<span data-ttu-id="976dd-110">此函數不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="976dd-110">This function doesn't return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="976dd-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="976dd-111">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="976dd-112">**目標平台**</span><span class="sxs-lookup"><span data-stu-id="976dd-112">**Target Platform**</span></span> | <span data-ttu-id="976dd-113">Windows</span><span class="sxs-lookup"><span data-stu-id="976dd-113">Windows</span></span> |
| <span data-ttu-id="976dd-114">**標頭**</span><span class="sxs-lookup"><span data-stu-id="976dd-114">**Header**</span></span> | <span data-ttu-id="976dd-115">d3d9。h</span><span class="sxs-lookup"><span data-stu-id="976dd-115">d3d9.h</span></span> |
| <span data-ttu-id="976dd-116">**程式庫**</span><span class="sxs-lookup"><span data-stu-id="976dd-116">**Library**</span></span> | <span data-ttu-id="976dd-117">d3d9 .lib</span><span class="sxs-lookup"><span data-stu-id="976dd-117">d3d9.lib</span></span> |
| <span data-ttu-id="976dd-118">**DLL**</span><span class="sxs-lookup"><span data-stu-id="976dd-118">**DLL**</span></span> | <span data-ttu-id="976dd-119">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="976dd-119">d3d9.dll</span></span> |