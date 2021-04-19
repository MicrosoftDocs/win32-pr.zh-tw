---
description: 判斷應用程式是否必須從系統剪貼簿提取資料，而不是從其內部快取中取得資料。
title: 'DlpMustPasteFromSystemClipboard 函式 (endpointdlp) '
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpMustPasteFromSystemClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 5863173b02cb5c63a2de46653c2d268464e82e65
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495521"
---
# <a name="dlpmustpastefromsystemclipboard-function"></a><span data-ttu-id="f91fc-103">DlpMustPasteFromSystemClipboard 函式</span><span class="sxs-lookup"><span data-stu-id="f91fc-103">DlpMustPasteFromSystemClipboard function</span></span>

<span data-ttu-id="f91fc-104">判斷應用程式是否必須從系統剪貼簿提取資料，而不是從其內部快取中取得資料。</span><span class="sxs-lookup"><span data-stu-id="f91fc-104">Determines whether the app must pull the data from the system clipboard rather than taking it from its internal cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="f91fc-105">語法</span><span class="sxs-lookup"><span data-stu-id="f91fc-105">Syntax</span></span>


```C++
BOOL WINAPI DlpMustPasteFromSystemClipboard();
```


## <a name="return-value"></a><span data-ttu-id="f91fc-106">傳回值</span><span class="sxs-lookup"><span data-stu-id="f91fc-106">Return value</span></span>

<span data-ttu-id="f91fc-107">如果呼叫 OS 剪貼簿為必要，則為 TRUE。否則為 FALSE。</span><span class="sxs-lookup"><span data-stu-id="f91fc-107">TRUE if calling into the OS clipboard is mandatory; otherwise, FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="f91fc-108">備註</span><span class="sxs-lookup"><span data-stu-id="f91fc-108">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="f91fc-109">需求</span><span class="sxs-lookup"><span data-stu-id="f91fc-109">Requirements</span></span>



| <span data-ttu-id="f91fc-110">需求</span><span class="sxs-lookup"><span data-stu-id="f91fc-110">Requirement</span></span>          |    <span data-ttu-id="f91fc-111">值</span><span class="sxs-lookup"><span data-stu-id="f91fc-111">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f91fc-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f91fc-112">Minimum supported client</span></span><br/> | <span data-ttu-id="f91fc-113">Windows 10 版本 1809 (10.0;組建 17763) </span><span class="sxs-lookup"><span data-stu-id="f91fc-113">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="f91fc-114">DLL</span><span class="sxs-lookup"><span data-stu-id="f91fc-114">DLL</span></span><br/>                      | <span data-ttu-id="f91fc-115">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="f91fc-115">EndpointDlp.dll</span></span> |