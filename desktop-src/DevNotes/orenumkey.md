---
description: 列舉離線登錄 hive 中指定之開啟登錄機碼的子機碼。 函式會在每次呼叫時，捕獲一個子機碼的相關資訊。
ms.assetid: 46d13c37-473a-4772-992c-a565ad702fb9
title: 'OREnumKey 函式 (Offreg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OREnumKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 24278bc59c75f32aed92c2ea5b5428f6ef6d9b45
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990937"
---
# <a name="orenumkey-function"></a><span data-ttu-id="316ca-104">OREnumKey 函式</span><span class="sxs-lookup"><span data-stu-id="316ca-104">OREnumKey function</span></span>

<span data-ttu-id="316ca-105">列舉離線登錄 hive 中指定之開啟登錄機碼的子機碼。</span><span class="sxs-lookup"><span data-stu-id="316ca-105">Enumerates the subkeys of the specified open registry key in an offline registry hive.</span></span> <span data-ttu-id="316ca-106">函式會在每次呼叫時，捕獲一個子機碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="316ca-106">The function retrieves information about one subkey each time it is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="316ca-107">語法</span><span class="sxs-lookup"><span data-stu-id="316ca-107">Syntax</span></span>


```C++
DWORD OREnumKey(
  _In_        ORHKEY    Handle,
  _In_        DWORD     dwIndex,
  _Out_       PWSTR     lpName,
  _Inout_     PDWORD    lpcName,
  _Out_opt_   PWSTR     lpClass,
  _Inout_opt_ PDWORD    lpcClass,
  _Out_opt_   PFILETIME lpftLastWriteTime
);
```



## <a name="parameters"></a><span data-ttu-id="316ca-108">參數</span><span class="sxs-lookup"><span data-stu-id="316ca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="316ca-109">*控制碼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="316ca-109">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="316ca-110">離線登錄 hive 中開啟登錄機碼的控制碼。</span><span class="sxs-lookup"><span data-stu-id="316ca-110">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="316ca-111">*dwIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="316ca-111">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="316ca-112">要取出的子機碼索引。</span><span class="sxs-lookup"><span data-stu-id="316ca-112">The index of the subkey to retrieve.</span></span> <span data-ttu-id="316ca-113">第一次呼叫函式時，此參數應為零，然後在後續呼叫中遞增。</span><span class="sxs-lookup"><span data-stu-id="316ca-113">This parameter should be zero for the first call to the function and then incremented for subsequent calls.</span></span>

<span data-ttu-id="316ca-114">因為子機碼不會排序，所以任何新的子機碼都會有任意的索引。</span><span class="sxs-lookup"><span data-stu-id="316ca-114">Because subkeys are not ordered, any new subkey will have an arbitrary index.</span></span> <span data-ttu-id="316ca-115">這表示函數可能會以任何順序傳回子機碼。</span><span class="sxs-lookup"><span data-stu-id="316ca-115">This means that the function may return subkeys in any order.</span></span>

</dd> <dt>

<span data-ttu-id="316ca-116">*lpName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="316ca-116">*lpName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="316ca-117">接收子機碼名稱之緩衝區的指標，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="316ca-117">A pointer to a buffer that receives the name of the subkey, including the terminating null character.</span></span> <span data-ttu-id="316ca-118">此函式只會將子機碼名稱（而不是完整金鑰階層）複製到緩衝區。</span><span class="sxs-lookup"><span data-stu-id="316ca-118">The function copies only the name of the subkey, not the full key hierarchy, to the buffer.</span></span> <span data-ttu-id="316ca-119">如果函式失敗，則不會將任何資訊複製到這個緩衝區。</span><span class="sxs-lookup"><span data-stu-id="316ca-119">If the function fails, no information is copied to this buffer.</span></span>

<span data-ttu-id="316ca-120">如需詳細資訊，請參閱登錄 [元素大小限制](../sysinfo/registry-element-size-limits.md)。</span><span class="sxs-lookup"><span data-stu-id="316ca-120">For more information, see [Registry Element Size Limits](../sysinfo/registry-element-size-limits.md).</span></span>

</dd> <dt>

<span data-ttu-id="316ca-121">*lpcName* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="316ca-121">*lpcName* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="316ca-122">變數的指標，這個變數會指定 *lpName* 參數在 **WCHARs** 中指定的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="316ca-122">A pointer to a variable that specifies the size of the buffer specified by the *lpName* parameter, in **WCHARs**.</span></span> <span data-ttu-id="316ca-123">此大小應包含終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="316ca-123">This size should include the terminating null character.</span></span> <span data-ttu-id="316ca-124">如果函式成功， *lpcName* 所指向的變數會包含儲存在緩衝區中的字元數，而不包含終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="316ca-124">If the function succeeds, the variable pointed to by *lpcName* contains the number of characters stored in the buffer, not including the terminating null character.</span></span>

</dd> <dt>

<span data-ttu-id="316ca-125">*lpClass* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="316ca-125">*lpClass* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="316ca-126">緩衝區的指標，此緩衝區會接收列舉子機碼之以 null 結束的類別字串。</span><span class="sxs-lookup"><span data-stu-id="316ca-126">A pointer to a buffer that receives the null-terminated class string of the enumerated subkey.</span></span> <span data-ttu-id="316ca-127">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="316ca-127">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="316ca-128">*lpcClass* \[in、out、optional\]</span><span class="sxs-lookup"><span data-stu-id="316ca-128">*lpcClass* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="316ca-129">變數的指標，這個變數會指定 *lpClass* 參數在 **WCHARs** 中指定的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="316ca-129">A pointer to a variable that specifies the size of the buffer specified by the *lpClass* parameter, in **WCHARs**.</span></span> <span data-ttu-id="316ca-130">大小應包含終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="316ca-130">The size should include the terminating null character.</span></span> <span data-ttu-id="316ca-131">如果函式成功， *lpcClass* 會包含儲存在緩衝區中的字元數，不包括終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="316ca-131">If the function succeeds, *lpcClass* contains the number of characters stored in the buffer, not including the terminating null character.</span></span> <span data-ttu-id="316ca-132">只有當 *lpClass* 為 **null** 時，此參數才可以是 **null** 。</span><span class="sxs-lookup"><span data-stu-id="316ca-132">This parameter can be **NULL** only if *lpClass* is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="316ca-133">*lpftLastWriteTime* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="316ca-133">*lpftLastWriteTime* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="316ca-134">[FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime)結構的指標，此結構會接收上次寫入列舉子機碼的時間。</span><span class="sxs-lookup"><span data-stu-id="316ca-134">A pointer to [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure that receives the time at which the enumerated subkey was last written.</span></span> <span data-ttu-id="316ca-135">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="316ca-135">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="316ca-136">傳回值</span><span class="sxs-lookup"><span data-stu-id="316ca-136">Return value</span></span>

<span data-ttu-id="316ca-137">如果函式成功，則傳回值為「錯誤 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="316ca-137">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="316ca-138">如果函式失敗，則傳回值為 Winerror.h 中定義的非零錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="316ca-138">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="316ca-139">您可以使用 [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) 函數搭配系統旗標的格式 \_ 訊息 \_ \_ ，以取得錯誤的一般描述。</span><span class="sxs-lookup"><span data-stu-id="316ca-139">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span> <span data-ttu-id="316ca-140">可能的錯誤代碼包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="316ca-140">Possible error codes include the following:</span></span>

-   <span data-ttu-id="316ca-141">如果 *lpName* 緩衝區太小而無法接收索引鍵的名稱，函數會傳回錯誤的 \_ \_ 資料。</span><span class="sxs-lookup"><span data-stu-id="316ca-141">If the *lpName* buffer is too small to receive the name of the key, the function returns ERROR\_MORE\_DATA.</span></span>
-   <span data-ttu-id="316ca-142">如果沒有其他可用的子機碼，此函式會傳回 \_ 沒有 \_ 其他專案的錯誤 \_ 。</span><span class="sxs-lookup"><span data-stu-id="316ca-142">If there are no more subkeys available, the function returns ERROR\_NO\_MORE\_ITEMS.</span></span>

## <a name="remarks"></a><span data-ttu-id="316ca-143">備註</span><span class="sxs-lookup"><span data-stu-id="316ca-143">Remarks</span></span>

<span data-ttu-id="316ca-144">若要列舉子機碼，應用程式一開始應該呼叫 **OREnumKey** 函數，並將 *dwIndex* 參數設定為零。</span><span class="sxs-lookup"><span data-stu-id="316ca-144">To enumerate subkeys, an application should initially call the **OREnumKey** function with the *dwIndex* parameter set to zero.</span></span> <span data-ttu-id="316ca-145">然後，應用程式應該遞增 *dwIndex* 參數並呼叫 **OREnumKey** ，直到沒有其他子機碼 (表示函式會傳回錯誤 \_) 的 \_ \_ 專案。</span><span class="sxs-lookup"><span data-stu-id="316ca-145">The application should then increment the *dwIndex* parameter and call **OREnumKey** until there are no more subkeys (meaning the function returns ERROR\_NO\_MORE\_ITEMS).</span></span>

<span data-ttu-id="316ca-146">應用程式也可以在第一次呼叫函式時，將 *dwIndex* 設定為最後一個子機碼的索引，並遞減索引，直到列舉索引0的子機碼為止。</span><span class="sxs-lookup"><span data-stu-id="316ca-146">The application can also set *dwIndex* to the index of the last subkey on the first call to the function and decrement the index until the subkey with the index 0 is enumerated.</span></span> <span data-ttu-id="316ca-147">若要取出最後一個子機碼的索引，請使用 [**ORQueryInfoKey**](/windows/win32/api/winreg/nf-winreg-regqueryinfokeya) 函數。</span><span class="sxs-lookup"><span data-stu-id="316ca-147">To retrieve the index of the last subkey, use the [**ORQueryInfoKey**](/windows/win32/api/winreg/nf-winreg-regqueryinfokeya) function.</span></span>

<span data-ttu-id="316ca-148">當應用程式使用 **OREnumKey** 函式時，它不應該呼叫任何可能會變更所列舉之索引鍵的離線登錄功能。</span><span class="sxs-lookup"><span data-stu-id="316ca-148">While an application is using the **OREnumKey** function, it should not make calls to any offline registry functions that might change the key being enumerated.</span></span>

## <a name="requirements"></a><span data-ttu-id="316ca-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="316ca-149">Requirements</span></span>



| <span data-ttu-id="316ca-150">需求</span><span class="sxs-lookup"><span data-stu-id="316ca-150">Requirement</span></span> | <span data-ttu-id="316ca-151">值</span><span class="sxs-lookup"><span data-stu-id="316ca-151">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="316ca-152">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="316ca-152">Redistributable</span></span><br/> | <span data-ttu-id="316ca-153">Windows Offline Registry library 1.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="316ca-153">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="316ca-154">標頭</span><span class="sxs-lookup"><span data-stu-id="316ca-154">Header</span></span><br/>          | <dl> <span data-ttu-id="316ca-155"><dt>Offreg。h</dt></span><span class="sxs-lookup"><span data-stu-id="316ca-155"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="316ca-156">DLL</span><span class="sxs-lookup"><span data-stu-id="316ca-156">DLL</span></span><br/>             | <dl> <span data-ttu-id="316ca-157"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="316ca-157"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="316ca-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="316ca-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="316ca-159">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="316ca-159">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="316ca-160">**ORDeleteKey**</span><span class="sxs-lookup"><span data-stu-id="316ca-160">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> <dt>

[<span data-ttu-id="316ca-161">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="316ca-161">**OROpenKey**</span></span>](oropenkey.md)
</dt> <dt>

[<span data-ttu-id="316ca-162">**ORQueryInfoKey**</span><span class="sxs-lookup"><span data-stu-id="316ca-162">**ORQueryInfoKey**</span></span>](orqueryinfokey.md)
</dt> </dl>

 

 
