---
description: 用來判斷專案是否存在於最近使用的 (MRU) 清單中。
title: MRUCMPPROC 回呼函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MRUCMPPROC
- MRUCMPPROCA
- MRUCMPPROCW
api_type:
- UserDefined
api_location: ''
ms.assetid: 00f31d6b-2a96-4abd-9647-24a6e66aa22f
ms.openlocfilehash: 83020fbcd0d4cfcfbc643d1360e3671595de6f32
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840779"
---
# <a name="mrucmpproc-callback-function"></a><span data-ttu-id="c7417-103">MRUCMPPROC 回呼函式</span><span class="sxs-lookup"><span data-stu-id="c7417-103">MRUCMPPROC callback function</span></span>

<span data-ttu-id="c7417-104">用來判斷專案是否存在於最近使用的 (MRU) 清單中。</span><span class="sxs-lookup"><span data-stu-id="c7417-104">Used to determine whether an item is present in a most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7417-105">語法</span><span class="sxs-lookup"><span data-stu-id="c7417-105">Syntax</span></span>


```C++
int CALLBACK MRUCMPPROC(
   LPCTSTR pString1,
   LPCTSTR pString2
);
```



## <a name="parameters"></a><span data-ttu-id="c7417-106">參數</span><span class="sxs-lookup"><span data-stu-id="c7417-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7417-107">*pString1*</span><span class="sxs-lookup"><span data-stu-id="c7417-107">*pString1*</span></span> 
</dt> <dd>

<span data-ttu-id="c7417-108">類型： **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="c7417-108">Type: **LPCTSTR**</span></span>

<span data-ttu-id="c7417-109">第一個字串。</span><span class="sxs-lookup"><span data-stu-id="c7417-109">The first string.</span></span>

</dd> <dt>

<span data-ttu-id="c7417-110">*pString2*</span><span class="sxs-lookup"><span data-stu-id="c7417-110">*pString2*</span></span> 
</dt> <dd>

<span data-ttu-id="c7417-111">類型： **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="c7417-111">Type: **LPCTSTR**</span></span>

<span data-ttu-id="c7417-112">要與第一個比較的第二個字串。</span><span class="sxs-lookup"><span data-stu-id="c7417-112">A second string to compare to the first.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7417-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="c7417-113">Return value</span></span>

<span data-ttu-id="c7417-114">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="c7417-114">Type: **int**</span></span>

<span data-ttu-id="c7417-115">如果專案相同，則傳回 0; 否則傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="c7417-115">Returns 0 if the items are identical, a nonzero value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7417-116">備註</span><span class="sxs-lookup"><span data-stu-id="c7417-116">Remarks</span></span>

<span data-ttu-id="c7417-117">您可以選擇性地指定此函數，以便在傳遞至 [**CreateMRUListW**](createmrulist.md)的 [**MRUINFO**](mruinfo.md)結構中使用。</span><span class="sxs-lookup"><span data-stu-id="c7417-117">This function can be optionally specified for use in the [**MRUINFO**](mruinfo.md) structure passed to [**CreateMRUListW**](createmrulist.md).</span></span> <span data-ttu-id="c7417-118">當使用 **mru \_ 二進位** 旗標建立 mru 清單時，這非常有用。</span><span class="sxs-lookup"><span data-stu-id="c7417-118">This is useful when the MRU list was created with the **MRU\_BINARY** flag.</span></span> <span data-ttu-id="c7417-119">如果未指定此函數，則會使用標準字串比較函數。</span><span class="sxs-lookup"><span data-stu-id="c7417-119">When this function is not specified, standard string comparison functions are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7417-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7417-120">Requirements</span></span>



| <span data-ttu-id="c7417-121">需求</span><span class="sxs-lookup"><span data-stu-id="c7417-121">Requirement</span></span> | <span data-ttu-id="c7417-122">值</span><span class="sxs-lookup"><span data-stu-id="c7417-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="c7417-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c7417-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c7417-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c7417-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>      |
| <span data-ttu-id="c7417-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c7417-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c7417-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c7417-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="c7417-127">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="c7417-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c7417-128">**MRUCMPPROCW** (Unicode) 和 **MRUCMPPROCA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="c7417-128">**MRUCMPPROCW** (Unicode) and **MRUCMPPROCA** (ANSI)</span></span><br/> |



 

 




