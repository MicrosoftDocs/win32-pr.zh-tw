---
title: D3DPERF_EndEvent 函式
description: 標記使用者定義事件的結尾。 PIX 可以使用此事件來觸發動作。
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
- D3DPERF_EndEvent
targetos: Windows
ms.openlocfilehash: 91c2a6a19b926cd9f5549fae084ce8973432b0f2
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/08/2020
ms.locfileid: "104374707"
---
# <a name="d3dperf_endevent-function"></a><span data-ttu-id="b8152-104">D3DPERF_EndEvent 函式</span><span class="sxs-lookup"><span data-stu-id="b8152-104">D3DPERF_EndEvent function</span></span>

<span data-ttu-id="b8152-105">標記使用者定義事件的結尾。</span><span class="sxs-lookup"><span data-stu-id="b8152-105">Marks the end of a user-defined event.</span></span> <span data-ttu-id="b8152-106">PIX 可以使用此事件來觸發動作。</span><span class="sxs-lookup"><span data-stu-id="b8152-106">PIX can use this event to trigger an action.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8152-107">語法</span><span class="sxs-lookup"><span data-stu-id="b8152-107">Syntax</span></span>

```cpp
int WINAPI D3DPERF_EndEvent(void);
```

## <a name="return-value"></a><span data-ttu-id="b8152-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="b8152-108">Return value</span></span>

<span data-ttu-id="b8152-109">事件結束之階層的層級。</span><span class="sxs-lookup"><span data-stu-id="b8152-109">The level of the hierarchy in which the event is ending.</span></span> <span data-ttu-id="b8152-110">如果發生錯誤，此值為負數。</span><span class="sxs-lookup"><span data-stu-id="b8152-110">If an error occurs, this value is negative.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8152-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8152-111">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="b8152-112">**目標平台**</span><span class="sxs-lookup"><span data-stu-id="b8152-112">**Target Platform**</span></span> | <span data-ttu-id="b8152-113">Windows</span><span class="sxs-lookup"><span data-stu-id="b8152-113">Windows</span></span> |
| <span data-ttu-id="b8152-114">**標頭**</span><span class="sxs-lookup"><span data-stu-id="b8152-114">**Header**</span></span> | <span data-ttu-id="b8152-115">d3d9。h</span><span class="sxs-lookup"><span data-stu-id="b8152-115">d3d9.h</span></span> |
| <span data-ttu-id="b8152-116">**程式庫**</span><span class="sxs-lookup"><span data-stu-id="b8152-116">**Library**</span></span> | <span data-ttu-id="b8152-117">d3d9 .lib</span><span class="sxs-lookup"><span data-stu-id="b8152-117">d3d9.lib</span></span> |
| <span data-ttu-id="b8152-118">**DLL**</span><span class="sxs-lookup"><span data-stu-id="b8152-118">**DLL**</span></span> | <span data-ttu-id="b8152-119">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="b8152-119">d3d9.dll</span></span> |