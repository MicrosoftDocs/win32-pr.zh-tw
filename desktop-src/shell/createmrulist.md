---
description: 建立最近使用的新 (MRU) 清單。
title: CreateMRUListW 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateMRUListW
- CreateMRUListW
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: b2d9e3c7-8151-45ef-9658-bd33a87b4c9c
ms.openlocfilehash: 34cd3dd9e5b9e62bbdd13b31d95e7205e4427de6
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843379"
---
# <a name="createmrulistw-function"></a><span data-ttu-id="b154f-103">CreateMRUListW 函式</span><span class="sxs-lookup"><span data-stu-id="b154f-103">CreateMRUListW function</span></span>

<span data-ttu-id="b154f-104">建立最近使用的新 (MRU) 清單。</span><span class="sxs-lookup"><span data-stu-id="b154f-104">Creates a new most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="b154f-105">語法</span><span class="sxs-lookup"><span data-stu-id="b154f-105">Syntax</span></span>


```C++
int CreateMRUListW(
  _In_ LPMRUINFO lpmi
);
```



## <a name="parameters"></a><span data-ttu-id="b154f-106">參數</span><span class="sxs-lookup"><span data-stu-id="b154f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b154f-107">*lpmi* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b154f-107">*lpmi* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b154f-108">類型： **LPMRUINFO**</span><span class="sxs-lookup"><span data-stu-id="b154f-108">Type: **LPMRUINFO**</span></span>

<span data-ttu-id="b154f-109">定義 MRU 清單的 [**MRUINFO**](mruinfo.md) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="b154f-109">A pointer to an [**MRUINFO**](mruinfo.md) structure defining the MRU list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b154f-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="b154f-110">Return value</span></span>

<span data-ttu-id="b154f-111">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="b154f-111">Type: **int**</span></span>

<span data-ttu-id="b154f-112">傳回新 MRU 清單的控制碼，如果發生錯誤，則傳回0。</span><span class="sxs-lookup"><span data-stu-id="b154f-112">Returns a handle to the new MRU list, or 0 in case of an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="b154f-113">備註</span><span class="sxs-lookup"><span data-stu-id="b154f-113">Remarks</span></span>

<span data-ttu-id="b154f-114">此函式不包含在公用標頭或程式庫中。</span><span class="sxs-lookup"><span data-stu-id="b154f-114">This function is not included in a public header or library.</span></span> <span data-ttu-id="b154f-115">您可以透過 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 來存取它，也可以從 comctl32.dll 中解壓縮它的序數，也就是400（ **CreateMRUListW**）。</span><span class="sxs-lookup"><span data-stu-id="b154f-115">It can be accessed through [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) or extracted from comctl32.dll by its ordinal, which is 400 for **CreateMRUListW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b154f-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="b154f-116">Requirements</span></span>



| <span data-ttu-id="b154f-117">需求</span><span class="sxs-lookup"><span data-stu-id="b154f-117">Requirement</span></span> | <span data-ttu-id="b154f-118">值</span><span class="sxs-lookup"><span data-stu-id="b154f-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b154f-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b154f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b154f-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b154f-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b154f-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b154f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b154f-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b154f-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b154f-123">DLL</span><span class="sxs-lookup"><span data-stu-id="b154f-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b154f-124"><dt>Comctl32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="b154f-124"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="b154f-125">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="b154f-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b154f-126">**CreateMRUListW** (Unicode) </span><span class="sxs-lookup"><span data-stu-id="b154f-126">**CreateMRUListW** (Unicode)</span></span><br/>                                                                        |



 

 
