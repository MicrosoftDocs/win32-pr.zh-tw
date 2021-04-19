---
description: 抓取離線登錄 hive 中指定之登錄機碼的相關資訊。
ms.assetid: b565c55c-acc2-4880-91eb-7bd9188e4749
title: 'ORQueryInfoKey 函式 (Offreg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORQueryInfoKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: b38a0dd35b1fe1755fbcbc3bcac3da379ee57e6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996211"
---
# <a name="orqueryinfokey-function"></a><span data-ttu-id="14e31-103">ORQueryInfoKey 函式</span><span class="sxs-lookup"><span data-stu-id="14e31-103">ORQueryInfoKey function</span></span>

<span data-ttu-id="14e31-104">抓取離線登錄 hive 中指定之登錄機碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="14e31-104">Retrieves information about the specified registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="14e31-105">語法</span><span class="sxs-lookup"><span data-stu-id="14e31-105">Syntax</span></span>


```C++
DWORD ORQueryInfoKey(
  _In_        ORHKEY    Handle,
  _Out_opt_   PWSTR     lpClass,
  _Inout_opt_ PDWORD    lpcClass,
  _Out_opt_   PDWORD    lpcSubKeys,
  _Out_opt_   PDWORD    lpcMaxSubKeyLen,
  _Out_opt_   PDWORD    lpcMaxClassLen,
  _Out_opt_   PDWORD    lpcValues,
  _Out_opt_   PDWORD    lpcMaxValueNameLen,
  _Out_opt_   PDWORD    lpcMaxValueLen,
  _Out_opt_   PDWORD    lpcbSecurityDescriptor,
  _Out_opt_   PFILETIME lpftLastWriteTime
);
```



## <a name="parameters"></a><span data-ttu-id="14e31-106">參數</span><span class="sxs-lookup"><span data-stu-id="14e31-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14e31-107">*控制碼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="14e31-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14e31-108">離線登錄 hive 中開啟登錄機碼的控制碼。</span><span class="sxs-lookup"><span data-stu-id="14e31-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="14e31-109">*lpClass* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="14e31-109">*lpClass* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="14e31-110">接收索引鍵類別的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="14e31-110">A pointer to a buffer that receives the key class.</span></span> <span data-ttu-id="14e31-111">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="14e31-111">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="14e31-112">*lpcClass* \[in、out、optional\]</span><span class="sxs-lookup"><span data-stu-id="14e31-112">*lpcClass* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="14e31-113">變數的指標，該變數會指定 *lpClass* 參數所指向的緩衝區大小（以字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="14e31-113">A pointer to a variable that specifies the size of the buffer pointed to by the *lpClass* parameter, in characters.</span></span>

<span data-ttu-id="14e31-114">大小應包含終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="14e31-114">The size should include the terminating null character.</span></span> <span data-ttu-id="14e31-115">當函式傳回時，這個變數會包含儲存在緩衝區中之類別字串的大小。</span><span class="sxs-lookup"><span data-stu-id="14e31-115">When the function returns, this variable contains the size of the class string that is stored in the buffer.</span></span> <span data-ttu-id="14e31-116">傳回的計數不包含終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="14e31-116">The count returned does not include the terminating null character.</span></span> <span data-ttu-id="14e31-117">如果緩衝區不夠大，則函式會傳回錯誤 \_ \_ 的資料，而變數會包含字串的大小（以字元為單位），而不會計算終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="14e31-117">If the buffer is not big enough, the function returns ERROR\_MORE\_DATA, and the variable contains the size of the string, in characters, without counting the terminating null character.</span></span>

<span data-ttu-id="14e31-118">如果 *lpClass* 為 **null**，則 *lpcClass* 可以是 **null**。</span><span class="sxs-lookup"><span data-stu-id="14e31-118">If *lpClass* is **NULL**, *lpcClass* can be **NULL**.</span></span>

<span data-ttu-id="14e31-119">如果 *lpClass* 參數是有效的位址，但不 (*lpcClass* 參數，例如，如果 *lpcClass* 參數為 **Null**) 則函式會傳回錯誤 \_ 不正確 \_ 參數。</span><span class="sxs-lookup"><span data-stu-id="14e31-119">If the *lpClass* parameter is a valid address, but the *lpcClass* parameter is not (for example, if the *lpcClass* parameter is **NULL**) then the function returns ERROR\_INVALID\_PARAMETER.</span></span>

</dd> <dt>

<span data-ttu-id="14e31-120">*lpcSubKeys* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="14e31-120">*lpcSubKeys* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="14e31-121">變數的指標，此變數會接收指定之索引鍵所包含的子機碼數目。</span><span class="sxs-lookup"><span data-stu-id="14e31-121">A pointer to a variable that receives the number of subkeys that are contained by the specified key.</span></span> <span data-ttu-id="14e31-122">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="14e31-122">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="14e31-123">*lpcMaxSubKeyLen* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="14e31-123">*lpcMaxSubKeyLen* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="14e31-124">變數的指標，此變數會接收具有最長名稱的索引鍵子機碼大小（以 Unicode 字元為單位），不包含終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="14e31-124">A pointer to a variable that receives the size of the key's subkey with the longest name, in Unicode characters, not including the terminating null character.</span></span> <span data-ttu-id="14e31-125">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="14e31-125">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="14e31-126">*lpcMaxClassLen* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="14e31-126">*lpcMaxClassLen* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="14e31-127">變數的指標，此變數會接收指定子機碼類別之最長字串的大小（以 Unicode 字元表示）。</span><span class="sxs-lookup"><span data-stu-id="14e31-127">A pointer to a variable that receives the size of the longest string that specifies a subkey class, in Unicode characters.</span></span> <span data-ttu-id="14e31-128">傳回的計數不包含終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="14e31-128">The count returned does not include the terminating null character.</span></span> <span data-ttu-id="14e31-129">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="14e31-129">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="14e31-130">*lpcValues* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="14e31-130">*lpcValues* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="14e31-131">變數的指標，此變數會接收與索引鍵相關聯的值數目。</span><span class="sxs-lookup"><span data-stu-id="14e31-131">A pointer to a variable that receives the number of values that are associated with the key.</span></span> <span data-ttu-id="14e31-132">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="14e31-132">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="14e31-133">*lpcMaxValueNameLen* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="14e31-133">*lpcMaxValueNameLen* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="14e31-134">變數的指標，此變數會接收索引鍵的最大值名稱大小（以 Unicode 字元為單位）。</span><span class="sxs-lookup"><span data-stu-id="14e31-134">A pointer to a variable that receives the size of the key's longest value name, in Unicode characters.</span></span> <span data-ttu-id="14e31-135">大小不包含終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="14e31-135">The size does not include the terminating null character.</span></span> <span data-ttu-id="14e31-136">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="14e31-136">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="14e31-137">*lpcMaxValueLen* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="14e31-137">*lpcMaxValueLen* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="14e31-138">變數的指標，此變數會接收索引鍵值之間最長的資料元件大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="14e31-138">A pointer to a variable that receives the size of the longest data component among the key's values, in bytes.</span></span> <span data-ttu-id="14e31-139">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="14e31-139">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="14e31-140">*lpcbSecurityDescriptor* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="14e31-140">*lpcbSecurityDescriptor* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="14e31-141">變數的指標，此變數會接收金鑰安全描述項的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="14e31-141">A pointer to a variable that receives the size of the key's security descriptor, in bytes.</span></span> <span data-ttu-id="14e31-142">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="14e31-142">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="14e31-143">*lpftLastWriteTime* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="14e31-143">*lpftLastWriteTime* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="14e31-144">接收最後寫入時間的 [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="14e31-144">A pointer to a [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure that receives the last write time.</span></span> <span data-ttu-id="14e31-145">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="14e31-145">This parameter can be **NULL**.</span></span>

<span data-ttu-id="14e31-146">函數會設定 [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) 結構的成員，以表示上次修改索引鍵或其任何值專案的時間。</span><span class="sxs-lookup"><span data-stu-id="14e31-146">The function sets the members of the [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure to indicate the last time that the key or any of its value entries is modified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14e31-147">傳回值</span><span class="sxs-lookup"><span data-stu-id="14e31-147">Return value</span></span>

<span data-ttu-id="14e31-148">如果函式成功，則傳回值為「錯誤 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="14e31-148">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="14e31-149">如果函式失敗，則傳回值為 Winerror.h 中定義的非零錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="14e31-149">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="14e31-150">您可以使用 [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) 函數搭配系統旗標的格式 \_ 訊息 \_ \_ ，以取得錯誤的一般描述。</span><span class="sxs-lookup"><span data-stu-id="14e31-150">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="14e31-151">如果 *lpClass* 緩衝區太小而無法接收類別的名稱，函數會傳回錯誤的 \_ \_ 資料。</span><span class="sxs-lookup"><span data-stu-id="14e31-151">If the *lpClass* buffer is too small to receive the name of the class, the function returns ERROR\_MORE\_DATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="14e31-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="14e31-152">Requirements</span></span>



| <span data-ttu-id="14e31-153">需求</span><span class="sxs-lookup"><span data-stu-id="14e31-153">Requirement</span></span> | <span data-ttu-id="14e31-154">值</span><span class="sxs-lookup"><span data-stu-id="14e31-154">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="14e31-155">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="14e31-155">Redistributable</span></span><br/> | <span data-ttu-id="14e31-156">Windows Offline Registry library 1.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="14e31-156">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="14e31-157">標頭</span><span class="sxs-lookup"><span data-stu-id="14e31-157">Header</span></span><br/>          | <dl> <span data-ttu-id="14e31-158"><dt>Offreg。h</dt></span><span class="sxs-lookup"><span data-stu-id="14e31-158"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="14e31-159">DLL</span><span class="sxs-lookup"><span data-stu-id="14e31-159">DLL</span></span><br/>             | <dl> <span data-ttu-id="14e31-160"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14e31-160"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14e31-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="14e31-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14e31-162">FILETIME</span><span class="sxs-lookup"><span data-stu-id="14e31-162">FILETIME</span></span>](/windows/win32/api/minwinbase/ns-minwinbase-filetime)
</dt> <dt>

[<span data-ttu-id="14e31-163">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="14e31-163">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="14e31-164">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="14e31-164">**OROpenKey**</span></span>](oropenkey.md)
</dt> <dt>

[<span data-ttu-id="14e31-165">**ORDeleteKey**</span><span class="sxs-lookup"><span data-stu-id="14e31-165">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> </dl>

 

 
