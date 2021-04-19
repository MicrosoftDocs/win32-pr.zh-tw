---
description: 列舉離線登錄區中指定之開啟登錄機碼的值。 函數會在每次呼叫函式時，取得指定索引鍵下某個值的資訊。
ms.assetid: 592a404f-a35d-4d89-ad1e-d572787bcb12
title: 'OREnumValue 函式 (Offreg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OREnumValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: b8049a5d16a88dc87bf4c0f6f5e8ef18b30beadc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977528"
---
# <a name="orenumvalue-function"></a><span data-ttu-id="d2244-104">OREnumValue 函式</span><span class="sxs-lookup"><span data-stu-id="d2244-104">OREnumValue function</span></span>

<span data-ttu-id="d2244-105">列舉離線登錄區中指定之開啟登錄機碼的值。</span><span class="sxs-lookup"><span data-stu-id="d2244-105">Enumerates the values for the specified open registry key in an offline registry hive.</span></span> <span data-ttu-id="d2244-106">函數會在每次呼叫函式時，取得指定索引鍵下某個值的資訊。</span><span class="sxs-lookup"><span data-stu-id="d2244-106">The function retrieves information for one value under the specified key each time the function is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2244-107">語法</span><span class="sxs-lookup"><span data-stu-id="d2244-107">Syntax</span></span>


```C++
DWORD OREnumValue(
  _In_        ORHKEY Handle,
  _In_        DWORD  dwIndex,
  _Out_       PWSTR  lpValueName,
  _Inout_     PDWORD lpcValueName,
  _Out_opt_   PDWORD lpType,
  _Out_opt_   PBYTE  lpData,
  _Inout_opt_ PDWORD lpcbData
);
```



## <a name="parameters"></a><span data-ttu-id="d2244-108">參數</span><span class="sxs-lookup"><span data-stu-id="d2244-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2244-109">*控制碼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d2244-109">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2244-110">離線登錄 hive 中開啟登錄機碼的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d2244-110">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="d2244-111">*dwIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d2244-111">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2244-112">要抓取之值的索引。</span><span class="sxs-lookup"><span data-stu-id="d2244-112">The index of the value to be retrieved.</span></span> <span data-ttu-id="d2244-113">第一次呼叫函式時，此參數應為零，然後在後續呼叫中遞增。</span><span class="sxs-lookup"><span data-stu-id="d2244-113">This parameter should be zero for the first call to the function and then be incremented for subsequent calls.</span></span>

<span data-ttu-id="d2244-114">因為值未排序，所以任何新的值都會有任意的索引。</span><span class="sxs-lookup"><span data-stu-id="d2244-114">Because values are not ordered, any new value will have an arbitrary index.</span></span> <span data-ttu-id="d2244-115">這表示函數可能會以任何順序傳回值。</span><span class="sxs-lookup"><span data-stu-id="d2244-115">This means that the function may return values in any order.</span></span>

</dd> <dt>

<span data-ttu-id="d2244-116">*lpValueName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d2244-116">*lpValueName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2244-117">緩衝區的指標，此緩衝區會以 null 終止字串的形式接收值的名稱。</span><span class="sxs-lookup"><span data-stu-id="d2244-117">A pointer to a buffer that receives the name of the value as a null-terminated string.</span></span> <span data-ttu-id="d2244-118">這個緩衝區必須夠大，才能包含終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="d2244-118">This buffer must be large enough to include the terminating null character.</span></span>

<span data-ttu-id="d2244-119">如需詳細資訊，請參閱登錄 [元素大小限制](../sysinfo/registry-element-size-limits.md)。</span><span class="sxs-lookup"><span data-stu-id="d2244-119">For more information, see [Registry Element Size Limits](../sysinfo/registry-element-size-limits.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2244-120">*lpcValueName* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="d2244-120">*lpcValueName* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d2244-121">變數的指標，該變數會指定 *lpValueName* 參數所指向的緩衝區大小（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="d2244-121">A pointer to a variable that specifies the size of the buffer pointed to by the *lpValueName* parameter, in characters.</span></span> <span data-ttu-id="d2244-122">當函式傳回時，變數會接收儲存在緩衝區中的字元數，而不包含終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="d2244-122">When the function returns, the variable receives the number of characters stored in the buffer, not including the terminating null character.</span></span>

</dd> <dt>

<span data-ttu-id="d2244-123">*lpType* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="d2244-123">*lpType* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d2244-124">變數的指標，此變數會接收程式碼，指出儲存在指定值中的資料類型。</span><span class="sxs-lookup"><span data-stu-id="d2244-124">A pointer to a variable that receives a code indicating the type of data stored in the specified value.</span></span> <span data-ttu-id="d2244-125">如需可能的類型代碼清單，請參閱登錄 [數值型別](../sysinfo/registry-value-types.md)。</span><span class="sxs-lookup"><span data-stu-id="d2244-125">For a list of the possible type codes, see [Registry Value Types](../sysinfo/registry-value-types.md).</span></span> <span data-ttu-id="d2244-126">如果不需要類型程式碼，則 *lpType* 參數可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="d2244-126">The *lpType* parameter can be **NULL** if the type code is not required.</span></span>

</dd> <dt>

<span data-ttu-id="d2244-127">*lpData* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="d2244-127">*lpData* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d2244-128">接收值專案資料之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="d2244-128">A pointer to a buffer that receives the data for the value entry.</span></span> <span data-ttu-id="d2244-129">如果資料不是必要的，則此參數可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="d2244-129">This parameter can be **NULL** if the data is not required.</span></span>

<span data-ttu-id="d2244-130">如果 *lpData* 為 **Null** ，而 *lpcbData* 為非 **Null**，則函式會將資料大小（以位元組為單位）儲存在 *lpcbData* 所指向的變數中。</span><span class="sxs-lookup"><span data-stu-id="d2244-130">If *lpData* is **NULL** and *lpcbData* is non-**NULL**, the function stores the size of the data, in bytes, in the variable pointed to by *lpcbData*.</span></span> <span data-ttu-id="d2244-131">這可讓應用程式判斷為數據配置緩衝區的最佳方式。</span><span class="sxs-lookup"><span data-stu-id="d2244-131">This enables an application to determine the best way to allocate a buffer for the data.</span></span>

</dd> <dt>

<span data-ttu-id="d2244-132">*lpcbData* \[in、out、optional\]</span><span class="sxs-lookup"><span data-stu-id="d2244-132">*lpcbData* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d2244-133">變數的指標，該變數會指定 *lpData* 參數所指向的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="d2244-133">A pointer to a variable that specifies the size of the buffer pointed to by the *lpData* parameter, in bytes.</span></span> <span data-ttu-id="d2244-134">當函式傳回時，變數會接收儲存在緩衝區中的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="d2244-134">When the function returns, the variable receives the number of bytes stored in the buffer.</span></span>

<span data-ttu-id="d2244-135">只有當 *lpData* 為 **null** 時，此參數才可以是 **null** 。</span><span class="sxs-lookup"><span data-stu-id="d2244-135">This parameter can be **NULL** only if *lpData* is **NULL**.</span></span>

<span data-ttu-id="d2244-136">如果資料具有 REG \_ sz、reg \_ 多重 \_ SZ 或 reg \_ EXPAND 型別 \_ ，則此大小包含任何終止的 null 字元或字元。</span><span class="sxs-lookup"><span data-stu-id="d2244-136">If the data has the REG\_SZ, REG\_MULTI\_SZ or REG\_EXPAND\_SZ type, this size includes any terminating null character or characters.</span></span> <span data-ttu-id="d2244-137">如需詳細資訊，請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="d2244-137">For more information, see Remarks.</span></span>

<span data-ttu-id="d2244-138">如果 *lpData* 所指定的緩衝區不夠大，無法容納資料，則函數會傳回錯誤 \_ \_ 的資料，並將所需的緩衝區大小儲存在 *lpcbData* 所指向的變數中。</span><span class="sxs-lookup"><span data-stu-id="d2244-138">If the buffer specified by *lpData* is not large enough to hold the data, the function returns ERROR\_MORE\_DATA and stores the required buffer size in the variable pointed to by *lpcbData*.</span></span> <span data-ttu-id="d2244-139">在此情況下， *lpData* 的內容是未定義的。</span><span class="sxs-lookup"><span data-stu-id="d2244-139">In this case, the contents of *lpData* are undefined.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2244-140">傳回值</span><span class="sxs-lookup"><span data-stu-id="d2244-140">Return value</span></span>

<span data-ttu-id="d2244-141">如果函式成功，則傳回值為「錯誤 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="d2244-141">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="d2244-142">如果函式失敗，則傳回值為 Winerror.h 中定義的非零錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d2244-142">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="d2244-143">您可以使用 [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) 函數搭配系統旗標的格式 \_ 訊息 \_ \_ ，以取得錯誤的一般描述。</span><span class="sxs-lookup"><span data-stu-id="d2244-143">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="d2244-144">如果 *lpData* 緩衝區太小而無法接收值，函數會傳回錯誤的 \_ \_ 資料。</span><span class="sxs-lookup"><span data-stu-id="d2244-144">If the *lpData* buffer is too small to receive the value, the function returns ERROR\_MORE\_DATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2244-145">備註</span><span class="sxs-lookup"><span data-stu-id="d2244-145">Remarks</span></span>

<span data-ttu-id="d2244-146">若要列舉值，應用程式一開始應該呼叫 **OREnumValue** 函數，並將 *dwIndex* 參數設定為零。</span><span class="sxs-lookup"><span data-stu-id="d2244-146">To enumerate values, an application should initially call the **OREnumValue** function with the *dwIndex* parameter set to zero.</span></span> <span data-ttu-id="d2244-147">然後，應用程式應該遞增 *dwIndex* 並呼叫 **OREnumValue** 函式，直到不再有值 (為止，直到函式傳回錯誤 \_ \_) 沒有其他專案為止 \_ 。</span><span class="sxs-lookup"><span data-stu-id="d2244-147">The application should then increment *dwIndex* and call the **OREnumValue** function until there are no more values (until the function returns ERROR\_NO\_MORE\_ITEMS).</span></span>

<span data-ttu-id="d2244-148">應用程式也可以在第一次呼叫函式時，將 *dwIndex* 設定為最後一個值的索引，並遞減索引，直到列舉索引0的值為止。</span><span class="sxs-lookup"><span data-stu-id="d2244-148">The application can also set *dwIndex* to the index of the last value on the first call to the function and decrement the index until the value with index 0 is enumerated.</span></span> <span data-ttu-id="d2244-149">若要取出最後一個值的索引，請使用 [**ORQueryInfoKey**](orqueryinfokey.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="d2244-149">To retrieve the index of the last value, use the [**ORQueryInfoKey**](orqueryinfokey.md) function.</span></span>

<span data-ttu-id="d2244-150">使用 **OREnumValue** 時，應用程式不應該呼叫可能會變更所查詢金鑰的任何離線登錄功能。</span><span class="sxs-lookup"><span data-stu-id="d2244-150">While using **OREnumValue**, an application should not call any offline registry functions that might change the key being queried.</span></span>

<span data-ttu-id="d2244-151">如果資料具有 REG \_ sz、reg \_ 多重 \_ SZ 或 reg \_ EXPAND 型別 \_ ，則字串可能未以正確的 null 終止字元儲存。</span><span class="sxs-lookup"><span data-stu-id="d2244-151">If the data has the REG\_SZ, REG\_MULTI\_SZ or REG\_EXPAND\_SZ type, the string may not have been stored with the proper null-terminating characters.</span></span> <span data-ttu-id="d2244-152">因此，即使函式傳回錯誤 \_ 成功，應用程式仍應確定字串在使用之前已正確地終止; 否則，它可能會覆寫緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d2244-152">Therefore, even if the function returns ERROR\_SUCCESS, the application should ensure that the string is properly terminated before using it; otherwise, it may overwrite a buffer.</span></span> <span data-ttu-id="d2244-153"> (請注意，REG \_ 多重 \_ SZ 字串應該要有兩個 null 終止字元。 ) </span><span class="sxs-lookup"><span data-stu-id="d2244-153">(Note that REG\_MULTI\_SZ strings should have two null-terminating characters.)</span></span>

<span data-ttu-id="d2244-154">若要判斷名稱和資料緩衝區的大小上限，請使用 [**ORQueryInfoKey**](orqueryinfokey.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="d2244-154">To determine the maximum size of the name and data buffers, use the [**ORQueryInfoKey**](orqueryinfokey.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2244-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="d2244-155">Requirements</span></span>



| <span data-ttu-id="d2244-156">需求</span><span class="sxs-lookup"><span data-stu-id="d2244-156">Requirement</span></span> | <span data-ttu-id="d2244-157">值</span><span class="sxs-lookup"><span data-stu-id="d2244-157">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2244-158">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="d2244-158">Redistributable</span></span><br/> | <span data-ttu-id="d2244-159">Windows Offline Registry library 1.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="d2244-159">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="d2244-160">標頭</span><span class="sxs-lookup"><span data-stu-id="d2244-160">Header</span></span><br/>          | <dl> <span data-ttu-id="d2244-161"><dt>Offreg。h</dt></span><span class="sxs-lookup"><span data-stu-id="d2244-161"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="d2244-162">DLL</span><span class="sxs-lookup"><span data-stu-id="d2244-162">DLL</span></span><br/>             | <dl> <span data-ttu-id="d2244-163"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2244-163"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2244-164">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d2244-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2244-165">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="d2244-165">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="d2244-166">**OREnumKey**</span><span class="sxs-lookup"><span data-stu-id="d2244-166">**OREnumKey**</span></span>](orenumkey.md)
</dt> <dt>

[<span data-ttu-id="d2244-167">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="d2244-167">**OROpenKey**</span></span>](oropenkey.md)
</dt> <dt>

[<span data-ttu-id="d2244-168">**ORQueryInfoKey**</span><span class="sxs-lookup"><span data-stu-id="d2244-168">**ORQueryInfoKey**</span></span>](orqueryinfokey.md)
</dt> </dl>

 

 
