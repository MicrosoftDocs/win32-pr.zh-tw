---
description: LookupWordSetString 函式會從已標記的集合傳回對應至所要求值的字串。
ms.assetid: e8d158a1-8544-4c10-b8e8-46888c1097e4
title: 'LookupWordSetString 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupWordSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7487becb195571e1eb88044195293b2c0b226e8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511836"
---
# <a name="lookupwordsetstring-function"></a><span data-ttu-id="af6e0-103">LookupWordSetString 函式</span><span class="sxs-lookup"><span data-stu-id="af6e0-103">LookupWordSetString function</span></span>

<span data-ttu-id="af6e0-104">**LookupWordSetString** 函式會從已標記的集合傳回對應至所要求值的字串。</span><span class="sxs-lookup"><span data-stu-id="af6e0-104">The **LookupWordSetString** function returns the string corresponding to the requested value from a labeled set.</span></span>

## <a name="syntax"></a><span data-ttu-id="af6e0-105">語法</span><span class="sxs-lookup"><span data-stu-id="af6e0-105">Syntax</span></span>


```C++
LPBYTE WINAPI LookupWordSetString(
   LPSET lpSet,
   WORD  Value
);
```



## <a name="parameters"></a><span data-ttu-id="af6e0-106">參數</span><span class="sxs-lookup"><span data-stu-id="af6e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af6e0-107">*lpSet*</span><span class="sxs-lookup"><span data-stu-id="af6e0-107">*lpSet*</span></span> 
</dt> <dd>

<span data-ttu-id="af6e0-108">用來將值的標籤解壓縮的標記集合。</span><span class="sxs-lookup"><span data-stu-id="af6e0-108">Labeled set from which you extract the value's label.</span></span>

</dd> <dt>

<span data-ttu-id="af6e0-109">*值*</span><span class="sxs-lookup"><span data-stu-id="af6e0-109">*Value*</span></span> 
</dt> <dd>

<span data-ttu-id="af6e0-110">已加上標籤之集合的值。</span><span class="sxs-lookup"><span data-stu-id="af6e0-110">Value of a labeled set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af6e0-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="af6e0-111">Return value</span></span>

<span data-ttu-id="af6e0-112">如果函式成功，則傳回值會是對應至所要求值的字串。</span><span class="sxs-lookup"><span data-stu-id="af6e0-112">If the function is successful, the return value is a string that corresponds to the requested value.</span></span>

<span data-ttu-id="af6e0-113">如果函式不成功，則指定的值不在集合中，傳回值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="af6e0-113">If the function is unsuccessful, the specified value is not in the set, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="af6e0-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="af6e0-114">Requirements</span></span>



| <span data-ttu-id="af6e0-115">需求</span><span class="sxs-lookup"><span data-stu-id="af6e0-115">Requirement</span></span> | <span data-ttu-id="af6e0-116">值</span><span class="sxs-lookup"><span data-stu-id="af6e0-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="af6e0-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="af6e0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="af6e0-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af6e0-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="af6e0-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="af6e0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="af6e0-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af6e0-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="af6e0-121">標頭</span><span class="sxs-lookup"><span data-stu-id="af6e0-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="af6e0-122"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="af6e0-122"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="af6e0-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="af6e0-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="af6e0-124"><dt>剖析器 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="af6e0-124"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="af6e0-125">DLL</span><span class="sxs-lookup"><span data-stu-id="af6e0-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af6e0-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af6e0-126"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




