---
description: 釋出與最近使用的 (MRU) 清單相關聯的控制碼，並將快取的資料寫入登錄中。
title: FreeMRUList 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeMRUList
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: 51db9352-7188-4fb7-9c92-1d9579cd7250
ms.openlocfilehash: 8140586d5f428a66f27a71ea665ae6761380e3a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973197"
---
# <a name="freemrulist-function"></a><span data-ttu-id="04bb1-103">FreeMRUList 函式</span><span class="sxs-lookup"><span data-stu-id="04bb1-103">FreeMRUList function</span></span>

<span data-ttu-id="04bb1-104">釋出與最近使用的 (MRU) 清單相關聯的控制碼，並將快取的資料寫入登錄中。</span><span class="sxs-lookup"><span data-stu-id="04bb1-104">Frees the handle associated with the most recently used (MRU) list and writes cached data to the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="04bb1-105">語法</span><span class="sxs-lookup"><span data-stu-id="04bb1-105">Syntax</span></span>


```C++
int FreeMRUList(
  _In_ HANDLE hMRU
);
```



## <a name="parameters"></a><span data-ttu-id="04bb1-106">參數</span><span class="sxs-lookup"><span data-stu-id="04bb1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04bb1-107">*hMRU* \[在\]</span><span class="sxs-lookup"><span data-stu-id="04bb1-107">*hMRU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04bb1-108">類型： **控制碼**</span><span class="sxs-lookup"><span data-stu-id="04bb1-108">Type: **HANDLE**</span></span>

<span data-ttu-id="04bb1-109">要釋放之 MRU 清單的控制碼。</span><span class="sxs-lookup"><span data-stu-id="04bb1-109">The handle of the MRU list to free.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04bb1-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="04bb1-110">Return value</span></span>

<span data-ttu-id="04bb1-111">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="04bb1-111">Type: **int**</span></span>

<span data-ttu-id="04bb1-112">如果成功，則傳回非負數值，否則為-1。</span><span class="sxs-lookup"><span data-stu-id="04bb1-112">Returns a non-negative value if successful, -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="04bb1-113">備註</span><span class="sxs-lookup"><span data-stu-id="04bb1-113">Remarks</span></span>

<span data-ttu-id="04bb1-114">如果 MRU 清單是使用 **mru \_ CACHEWRITE** 旗標建立的，則呼叫 **FreeMRUList** 會導致目前尚未寫入儲存在登錄中的 mru 清單版本的任何變更。</span><span class="sxs-lookup"><span data-stu-id="04bb1-114">If the MRU list was created using the **MRU\_CACHEWRITE** flag, calling **FreeMRUList** causes any changes not yet written to the version of the MRU list stored in registry to be written at this time.</span></span>

<span data-ttu-id="04bb1-115">此函式不包含在公用標頭或程式庫中。</span><span class="sxs-lookup"><span data-stu-id="04bb1-115">This function is not included in a public header or library.</span></span> <span data-ttu-id="04bb1-116">它必須由序數152從 comctl32.dll 解壓縮。</span><span class="sxs-lookup"><span data-stu-id="04bb1-116">It must be extracted from comctl32.dll by ordinal 152.</span></span>

## <a name="requirements"></a><span data-ttu-id="04bb1-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="04bb1-117">Requirements</span></span>



| <span data-ttu-id="04bb1-118">需求</span><span class="sxs-lookup"><span data-stu-id="04bb1-118">Requirement</span></span> | <span data-ttu-id="04bb1-119">值</span><span class="sxs-lookup"><span data-stu-id="04bb1-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04bb1-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="04bb1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="04bb1-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04bb1-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="04bb1-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="04bb1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="04bb1-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04bb1-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="04bb1-124">DLL</span><span class="sxs-lookup"><span data-stu-id="04bb1-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04bb1-125"><dt>Comctl32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="04bb1-125"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




