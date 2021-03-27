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
ms.openlocfilehash: 572e52f1461e3d48ab9eba1aa903c7fb690636d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689800"
---
# <a name="createmrulistw-function"></a><span data-ttu-id="26920-103">CreateMRUListW 函式</span><span class="sxs-lookup"><span data-stu-id="26920-103">CreateMRUListW function</span></span>

<span data-ttu-id="26920-104">建立最近使用的新 (MRU) 清單。</span><span class="sxs-lookup"><span data-stu-id="26920-104">Creates a new most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="26920-105">語法</span><span class="sxs-lookup"><span data-stu-id="26920-105">Syntax</span></span>


```C++
int CreateMRUListW(
  _In_ LPMRUINFO lpmi
);
```



## <a name="parameters"></a><span data-ttu-id="26920-106">參數</span><span class="sxs-lookup"><span data-stu-id="26920-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26920-107">*lpmi* \[在\]</span><span class="sxs-lookup"><span data-stu-id="26920-107">*lpmi* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26920-108">類型： **LPMRUINFO**</span><span class="sxs-lookup"><span data-stu-id="26920-108">Type: **LPMRUINFO**</span></span>

<span data-ttu-id="26920-109">定義 MRU 清單的 [**MRUINFO**](mruinfo.md) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="26920-109">A pointer to an [**MRUINFO**](mruinfo.md) structure defining the MRU list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26920-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="26920-110">Return value</span></span>

<span data-ttu-id="26920-111">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="26920-111">Type: **int**</span></span>

<span data-ttu-id="26920-112">傳回新 MRU 清單的控制碼，如果發生錯誤，則傳回0。</span><span class="sxs-lookup"><span data-stu-id="26920-112">Returns a handle to the new MRU list, or 0 in case of an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="26920-113">備註</span><span class="sxs-lookup"><span data-stu-id="26920-113">Remarks</span></span>

<span data-ttu-id="26920-114">此函式不包含在公用標頭或程式庫中。</span><span class="sxs-lookup"><span data-stu-id="26920-114">This function is not included in a public header or library.</span></span> <span data-ttu-id="26920-115">您可以透過 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 來存取它，也可以從 comctl32.dll 中解壓縮它的序數，也就是400（ **CreateMRUListW**）。</span><span class="sxs-lookup"><span data-stu-id="26920-115">It can be accessed through [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) or extracted from comctl32.dll by its ordinal, which is 400 for **CreateMRUListW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="26920-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="26920-116">Requirements</span></span>



| <span data-ttu-id="26920-117">需求</span><span class="sxs-lookup"><span data-stu-id="26920-117">Requirement</span></span> | <span data-ttu-id="26920-118">值</span><span class="sxs-lookup"><span data-stu-id="26920-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26920-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="26920-119">Minimum supported client</span></span><br/> | <span data-ttu-id="26920-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="26920-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="26920-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="26920-121">Minimum supported server</span></span><br/> | <span data-ttu-id="26920-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="26920-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="26920-123">DLL</span><span class="sxs-lookup"><span data-stu-id="26920-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26920-124"><dt>Comctl32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="26920-124"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="26920-125">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="26920-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="26920-126">**CreateMRUListW** (Unicode) </span><span class="sxs-lookup"><span data-stu-id="26920-126">**CreateMRUListW** (Unicode)</span></span><br/>                                                                        |



 

 
