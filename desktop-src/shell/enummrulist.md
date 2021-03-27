---
description: 列舉最近使用 (MRU) 清單的內容。 （選擇性）從列舉中抓取專案。
title: EnumMRUListW 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumMRUListW
- EnumMRUListW
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: 630e5f27-96bf-4e88-b01a-127b301cc051
ms.openlocfilehash: 6b6e9588588e44a2c3b40f6ac012b11f21c875e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851632"
---
# <a name="enummrulistw-function"></a><span data-ttu-id="39d33-104">EnumMRUListW 函式</span><span class="sxs-lookup"><span data-stu-id="39d33-104">EnumMRUListW function</span></span>

<span data-ttu-id="39d33-105">\[您可以透過 Windows XP Service Pack 2 (SP2) 和 Windows Server 2003 來取得此函式。</span><span class="sxs-lookup"><span data-stu-id="39d33-105">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="39d33-106">它可能會在後續版本的 Windows 中改變或無法使用。</span><span class="sxs-lookup"><span data-stu-id="39d33-106">It might be altered or unavailable in subsequent versions of Windows.</span></span> <span data-ttu-id="39d33-107">\]</span><span class="sxs-lookup"><span data-stu-id="39d33-107">\]</span></span>

<span data-ttu-id="39d33-108">列舉最近使用 (MRU) 清單的內容。</span><span class="sxs-lookup"><span data-stu-id="39d33-108">Enumerates the contents of the most recently used (MRU) list.</span></span> <span data-ttu-id="39d33-109">（選擇性）從列舉中抓取專案。</span><span class="sxs-lookup"><span data-stu-id="39d33-109">Optionally retrieves an item from the enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="39d33-110">語法</span><span class="sxs-lookup"><span data-stu-id="39d33-110">Syntax</span></span>


```C++
int EnumMRUListW(
  _In_  HANDLE hMRU,
  _In_  int    nItem,
  _Out_ void   *lpData,
  _In_  UINT   uLen
);
```



## <a name="parameters"></a><span data-ttu-id="39d33-111">參數</span><span class="sxs-lookup"><span data-stu-id="39d33-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39d33-112">*hMRU* \[在\]</span><span class="sxs-lookup"><span data-stu-id="39d33-112">*hMRU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39d33-113">類型： **控制碼**</span><span class="sxs-lookup"><span data-stu-id="39d33-113">Type: **HANDLE**</span></span>

<span data-ttu-id="39d33-114">建立清單時所取得之 MRU 清單的控制碼。</span><span class="sxs-lookup"><span data-stu-id="39d33-114">The handle of the MRU list, obtained when the list was created.</span></span>

</dd> <dt>

<span data-ttu-id="39d33-115">*nItem* \[在\]</span><span class="sxs-lookup"><span data-stu-id="39d33-115">*nItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39d33-116">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="39d33-116">Type: **int**</span></span>

<span data-ttu-id="39d33-117">要傳回的專案。</span><span class="sxs-lookup"><span data-stu-id="39d33-117">The item to return.</span></span> <span data-ttu-id="39d33-118">如果這個值小於0，函數會傳回 MRU 清單中的專案數。</span><span class="sxs-lookup"><span data-stu-id="39d33-118">If this value is less than 0, the function returns the number of items in the MRU list.</span></span>

</dd> <dt>

<span data-ttu-id="39d33-119">*lpData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="39d33-119">*lpData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39d33-120">類型： \**void \** _</span><span class="sxs-lookup"><span data-stu-id="39d33-120">Type: \**void\** _</span></span>

<span data-ttu-id="39d33-121">接收 _nItem \* 中所要求之專案的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="39d33-121">A pointer to a buffer that receives the item requested in _nItem\*.</span></span> <span data-ttu-id="39d33-122">如果 *nItem* 小於0，則這個緩衝區的內容不會變更。</span><span class="sxs-lookup"><span data-stu-id="39d33-122">If *nItem* is less than 0, the contents of this buffer are unchanged.</span></span>

</dd> <dt>

<span data-ttu-id="39d33-123">*uLen* \[在\]</span><span class="sxs-lookup"><span data-stu-id="39d33-123">*uLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39d33-124">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="39d33-124">Type: **UINT**</span></span>

<span data-ttu-id="39d33-125">緩衝區的大小，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="39d33-125">The size of the buffer, including the terminating null character.</span></span> <span data-ttu-id="39d33-126">如果 MRU 清單是使用 **mru \_ 二進位** 旗標建立的，這就是以位元組為單位的大小。</span><span class="sxs-lookup"><span data-stu-id="39d33-126">If the MRU list was created with the **MRU\_BINARY** flag, this is the size in bytes.</span></span> <span data-ttu-id="39d33-127">否則，它是以字元為單位的大小。</span><span class="sxs-lookup"><span data-stu-id="39d33-127">Otherwise, it is the size in characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39d33-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="39d33-128">Return value</span></span>

<span data-ttu-id="39d33-129">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="39d33-129">Type: **int**</span></span>

<span data-ttu-id="39d33-130">傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="39d33-130">Returns one of the following values.</span></span>

-   <span data-ttu-id="39d33-131">如果 *nItem* 小於0，則傳回列舉中的專案數。</span><span class="sxs-lookup"><span data-stu-id="39d33-131">Returns the number of items in the enumeration, if *nItem* is less than 0.</span></span>
-   <span data-ttu-id="39d33-132">如果發生錯誤，則傳回-1。</span><span class="sxs-lookup"><span data-stu-id="39d33-132">Returns -1 if an error occurred.</span></span>
-   <span data-ttu-id="39d33-133">否則，會傳回 *lpData* 中傳回的字串大小，包括終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="39d33-133">Otherwise, returns the size of the string returned in *lpData*, including the terminating null character.</span></span> <span data-ttu-id="39d33-134">如果 MRU 清單是使用 **mru \_ 二進位** 旗標建立的，這就是以位元組為單位的大小。</span><span class="sxs-lookup"><span data-stu-id="39d33-134">If the MRU list was created with the **MRU\_BINARY** flag, this is the size in bytes.</span></span> <span data-ttu-id="39d33-135">否則，它是以字元為單位的大小。</span><span class="sxs-lookup"><span data-stu-id="39d33-135">Otherwise, it is the size in characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="39d33-136">備註</span><span class="sxs-lookup"><span data-stu-id="39d33-136">Remarks</span></span>

<span data-ttu-id="39d33-137">此函式不包含在公用標頭或程式庫中。</span><span class="sxs-lookup"><span data-stu-id="39d33-137">This function is not included in a public header or library.</span></span> <span data-ttu-id="39d33-138">您可以透過 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 來存取它，也可以從 comctl32.dll 中解壓縮它的序數，也就是403（ **EnumMRUListW**）。</span><span class="sxs-lookup"><span data-stu-id="39d33-138">It can be accessed through [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) or extracted from comctl32.dll by its ordinal, which is 403 for **EnumMRUListW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="39d33-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="39d33-139">Requirements</span></span>



| <span data-ttu-id="39d33-140">需求</span><span class="sxs-lookup"><span data-stu-id="39d33-140">Requirement</span></span> | <span data-ttu-id="39d33-141">值</span><span class="sxs-lookup"><span data-stu-id="39d33-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39d33-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="39d33-142">Minimum supported client</span></span><br/> | <span data-ttu-id="39d33-143">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="39d33-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="39d33-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="39d33-144">Minimum supported server</span></span><br/> | <span data-ttu-id="39d33-145">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="39d33-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="39d33-146">DLL</span><span class="sxs-lookup"><span data-stu-id="39d33-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39d33-147"><dt>Comctl32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="39d33-147"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="39d33-148">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="39d33-148">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="39d33-149">**EnumMRUListW** (Unicode) </span><span class="sxs-lookup"><span data-stu-id="39d33-149">**EnumMRUListW** (Unicode)</span></span><br/>                                                                          |



## <a name="see-also"></a><span data-ttu-id="39d33-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="39d33-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39d33-151">**CreateMRUListW**</span><span class="sxs-lookup"><span data-stu-id="39d33-151">**CreateMRUListW**</span></span>](createmrulist.md)
</dt> <dt>

[<span data-ttu-id="39d33-152">**MRUINFO**</span><span class="sxs-lookup"><span data-stu-id="39d33-152">**MRUINFO**</span></span>](mruinfo.md)
</dt> </dl>

 

 
