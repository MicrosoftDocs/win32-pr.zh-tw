---
description: 包含定義最近使用的新 (MRU) 清單的資訊。 由 CreateMRUListW 使用。
title: MRUINFO 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _MRUINFO
- MRUINFOA
- MRUINFOW
api_type:
- NA
api_location: ''
ms.assetid: 31d5831d-9a19-4bd9-8439-ce844966c414
ms.openlocfilehash: 91c0b1a2c10f4ac77afa5f8af2380b3d14ced8f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991118"
---
# <a name="mruinfo-structure"></a><span data-ttu-id="10166-104">MRUINFO 結構</span><span class="sxs-lookup"><span data-stu-id="10166-104">MRUINFO structure</span></span>

<span data-ttu-id="10166-105">包含定義最近使用的新 (MRU) 清單的資訊。</span><span class="sxs-lookup"><span data-stu-id="10166-105">Contains information that defines a new most recently used (MRU) list.</span></span> <span data-ttu-id="10166-106">由 [**CreateMRUListW**](createmrulist.md)使用。</span><span class="sxs-lookup"><span data-stu-id="10166-106">Used by [**CreateMRUListW**](createmrulist.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="10166-107">語法</span><span class="sxs-lookup"><span data-stu-id="10166-107">Syntax</span></span>


```C++
typedef struct {
  DWORD      cbSize;
  UINT       uMax;
  UINT       fFlags;
  HKEY       hKey;
  LPCTSTR    lpszSubKey;
  MRUCMPPROC lpfnCompare;
} _MRUINFO;
```



## <a name="members"></a><span data-ttu-id="10166-108">成員</span><span class="sxs-lookup"><span data-stu-id="10166-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="10166-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="10166-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="10166-110">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="10166-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="10166-111">結構的大小。</span><span class="sxs-lookup"><span data-stu-id="10166-111">The size of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="10166-112">**uMax**</span><span class="sxs-lookup"><span data-stu-id="10166-112">**uMax**</span></span>
</dt> <dd>

<span data-ttu-id="10166-113">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="10166-113">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="10166-114">MRU 清單中專案的最大數目。</span><span class="sxs-lookup"><span data-stu-id="10166-114">The maximum number of entries in the MRU list.</span></span>

</dd> <dt>

<span data-ttu-id="10166-115">**fFlags**</span><span class="sxs-lookup"><span data-stu-id="10166-115">**fFlags**</span></span>
</dt> <dd>

<span data-ttu-id="10166-116">類型： **UINT**</span><span class="sxs-lookup"><span data-stu-id="10166-116">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="10166-117">下列一或多個旗標。</span><span class="sxs-lookup"><span data-stu-id="10166-117">One or more of the following flags.</span></span>

<dt>

<span id="MRU_BINARY"></span><span id="mru_binary"></span>

<span data-ttu-id="10166-118"><span id="MRU_BINARY"></span><span id="mru_binary"></span>**MRU \_二元** (0x0001) </span><span class="sxs-lookup"><span data-stu-id="10166-118"><span id="MRU_BINARY"></span><span id="mru_binary"></span>**MRU\_BINARY** (0x0001)</span></span>


</dt> <dd>

<span data-ttu-id="10166-119">資料會以二進位資料的形式儲存在登錄中，而不是以字串資料的形式儲存。</span><span class="sxs-lookup"><span data-stu-id="10166-119">Data is stored in the registry as binary data rather than string data.</span></span>

</dd> <dt>

<span id="MRU_CACHEWRITE"></span><span id="mru_cachewrite"></span>

<span data-ttu-id="10166-120"><span id="MRU_CACHEWRITE"></span><span id="mru_cachewrite"></span>**MRU \_CACHEWRITE** (0x0002) </span><span class="sxs-lookup"><span data-stu-id="10166-120"><span id="MRU_CACHEWRITE"></span><span id="mru_cachewrite"></span>**MRU\_CACHEWRITE** (0x0002)</span></span>


</dt> <dd>

<span data-ttu-id="10166-121">只有在新增專案或從記憶體釋放 MRU 清單的資源時，才會將變更寫入儲存在登錄中的 MRU 版本。</span><span class="sxs-lookup"><span data-stu-id="10166-121">Write changes to the version of the MRU stored in the registry only when a new item is added or the MRU list's resources are freed from memory.</span></span> <span data-ttu-id="10166-122">請注意，在記憶體中，作用中的 MRU 版本會立即更新以回應任何內容變更或排序。</span><span class="sxs-lookup"><span data-stu-id="10166-122">Note that the active version of the MRU in memory is updated immediately in response to any change in contents or ordering.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="10166-123">**hKey**</span><span class="sxs-lookup"><span data-stu-id="10166-123">**hKey**</span></span>
</dt> <dd>

<span data-ttu-id="10166-124">類型： **HKEY**</span><span class="sxs-lookup"><span data-stu-id="10166-124">Type: **HKEY**</span></span>

</dd> <dd>

<span data-ttu-id="10166-125">目前開啟之索引鍵的控制碼，或下列其中一個預先定義的值，用來儲存 MRU 資料。</span><span class="sxs-lookup"><span data-stu-id="10166-125">A handle to the currently open key, or one of the following predefined values under which to store the MRU data.</span></span>

<dl><span id="HKEY_CURRENT_USER"></span><span id="hkey_current_user"></span><dt>

<span data-ttu-id="10166-126">**HKEY \_ 目前的 \_ 使用者**</span><span class="sxs-lookup"><span data-stu-id="10166-126">**HKEY\_CURRENT\_USER**</span></span>
</dt><span id="HKEY_LOCAL_MACHINE"></span><span id="hkey_local_machine"></span><dt>

<span data-ttu-id="10166-127">**HKEY \_ 本機 \_ 電腦**</span><span class="sxs-lookup"><span data-stu-id="10166-127">**HKEY\_LOCAL\_MACHINE**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="10166-128">**lpszSubKey**</span><span class="sxs-lookup"><span data-stu-id="10166-128">**lpszSubKey**</span></span>
</dt> <dd>

<span data-ttu-id="10166-129">類型： **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="10166-129">Type: **LPCTSTR**</span></span>

</dd> <dd>

<span data-ttu-id="10166-130">用來儲存 MRU 資料的子機碼。</span><span class="sxs-lookup"><span data-stu-id="10166-130">The subkey under which to store the MRU data.</span></span>

</dd> <dt>

<span data-ttu-id="10166-131">**lpfnCompare**</span><span class="sxs-lookup"><span data-stu-id="10166-131">**lpfnCompare**</span></span>
</dt> <dd>

<span data-ttu-id="10166-132">類型： **[ **MRUCMPPROC**](mrucmpproc.md)**</span><span class="sxs-lookup"><span data-stu-id="10166-132">Type: **[**MRUCMPPROC**](mrucmpproc.md)**</span></span>

</dd> <dd>

<span data-ttu-id="10166-133">選擇性資料比較函式的指標，可用來判斷專案是否存在於 MRU 清單中。</span><span class="sxs-lookup"><span data-stu-id="10166-133">A pointer to an optional data comparison function that can be used to determine whether an item is present in the MRU list.</span></span> <span data-ttu-id="10166-134">當使用 **mru \_ 二進位** 旗標建立 mru 清單時，這非常有用。</span><span class="sxs-lookup"><span data-stu-id="10166-134">This is useful when the MRU list was created with the **MRU\_BINARY** flag.</span></span> <span data-ttu-id="10166-135">如果這個成員是 **Null**，則會使用標準字串比較函數;若為二進位資料，則會使用直接記憶體比較。</span><span class="sxs-lookup"><span data-stu-id="10166-135">If this member is **NULL**, standard string comparison functions are used; for binary data, a direct memory comparison is used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="10166-136">備註</span><span class="sxs-lookup"><span data-stu-id="10166-136">Remarks</span></span>

<span data-ttu-id="10166-137">標頭檔中未定義此結構。</span><span class="sxs-lookup"><span data-stu-id="10166-137">This structure is not defined in a header file.</span></span> <span data-ttu-id="10166-138">您必須自行定義。</span><span class="sxs-lookup"><span data-stu-id="10166-138">You must define it yourself.</span></span>

## <a name="requirements"></a><span data-ttu-id="10166-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="10166-139">Requirements</span></span>



| <span data-ttu-id="10166-140">需求</span><span class="sxs-lookup"><span data-stu-id="10166-140">Requirement</span></span> | <span data-ttu-id="10166-141">值</span><span class="sxs-lookup"><span data-stu-id="10166-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="10166-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="10166-142">Minimum supported client</span></span><br/> | <span data-ttu-id="10166-143">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10166-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="10166-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="10166-144">Minimum supported server</span></span><br/> | <span data-ttu-id="10166-145">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10166-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="10166-146">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="10166-146">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="10166-147">**MRUINFOW** (Unicode) 和 **MRUINFOA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="10166-147">**MRUINFOW** (Unicode) and **MRUINFOA** (ANSI)</span></span><br/>  |



 

 




