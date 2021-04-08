---
description: LookupDwordSetString 函式會傳回對應至已加上標籤集合之指定值的字串。
ms.assetid: ee2b1b7a-6b64-4c8c-a71d-de970b66d46e
title: 'LookupDwordSetString 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupDwordSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 57688edab7421f939e03322b8b244219b00d31fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690771"
---
# <a name="lookupdwordsetstring-function"></a><span data-ttu-id="c8d7e-103">LookupDwordSetString 函式</span><span class="sxs-lookup"><span data-stu-id="c8d7e-103">LookupDwordSetString function</span></span>

<span data-ttu-id="c8d7e-104">**LookupDwordSetString** 函式會傳回對應至已加上標籤集合之指定值的字串。</span><span class="sxs-lookup"><span data-stu-id="c8d7e-104">The **LookupDwordSetString** function returns the string corresponding to the specified value of a labeled set.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8d7e-105">語法</span><span class="sxs-lookup"><span data-stu-id="c8d7e-105">Syntax</span></span>


```C++
LPBYTE WINAPI LookupDwordSetString(
   LPSET lpSet,
   DWORD Value
);
```



## <a name="parameters"></a><span data-ttu-id="c8d7e-106">參數</span><span class="sxs-lookup"><span data-stu-id="c8d7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8d7e-107">*lpSet*</span><span class="sxs-lookup"><span data-stu-id="c8d7e-107">*lpSet*</span></span> 
</dt> <dd>

<span data-ttu-id="c8d7e-108">標示為 [設定]，您可以從中解壓縮值的標籤。</span><span class="sxs-lookup"><span data-stu-id="c8d7e-108">Labeled set, from which you can extract the value's label.</span></span>

</dd> <dt>

<span data-ttu-id="c8d7e-109">*值*</span><span class="sxs-lookup"><span data-stu-id="c8d7e-109">*Value*</span></span> 
</dt> <dd>

<span data-ttu-id="c8d7e-110">已加上標籤之集合的值。</span><span class="sxs-lookup"><span data-stu-id="c8d7e-110">Value of a labeled set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8d7e-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c8d7e-111">Return value</span></span>

<span data-ttu-id="c8d7e-112">如果函式成功，則傳回值會是對應至指定值的字串。</span><span class="sxs-lookup"><span data-stu-id="c8d7e-112">If the function is successful, the return value is the string that corresponds to the specified value.</span></span>

<span data-ttu-id="c8d7e-113">如果函式不成功，則指定的值不在集合中，傳回值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c8d7e-113">If the function is unsuccessful, the specified value is not in the set, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8d7e-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="c8d7e-114">Requirements</span></span>



| <span data-ttu-id="c8d7e-115">需求</span><span class="sxs-lookup"><span data-stu-id="c8d7e-115">Requirement</span></span> | <span data-ttu-id="c8d7e-116">值</span><span class="sxs-lookup"><span data-stu-id="c8d7e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c8d7e-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c8d7e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c8d7e-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8d7e-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="c8d7e-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c8d7e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c8d7e-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8d7e-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c8d7e-121">標頭</span><span class="sxs-lookup"><span data-stu-id="c8d7e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8d7e-122"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="c8d7e-122"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="c8d7e-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="c8d7e-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="c8d7e-124"><dt>剖析器 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8d7e-124"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="c8d7e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c8d7e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8d7e-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8d7e-126"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




