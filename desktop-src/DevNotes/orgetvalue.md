---
description: 抓取離線登錄 hive 中指定之登錄值的類型和資料。
ms.assetid: 83604743-cb59-42a1-9951-620ad5bd8de7
title: 'ORGetValue 函式 (Offreg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 375dae37e2e6b6299a7bf1fd36f9b950d0433d89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994713"
---
# <a name="orgetvalue-function"></a><span data-ttu-id="18e28-103">ORGetValue 函式</span><span class="sxs-lookup"><span data-stu-id="18e28-103">ORGetValue function</span></span>

<span data-ttu-id="18e28-104">抓取離線登錄 hive 中指定之登錄值的類型和資料。</span><span class="sxs-lookup"><span data-stu-id="18e28-104">Retrieves the type and data for the specified registry value in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="18e28-105">語法</span><span class="sxs-lookup"><span data-stu-id="18e28-105">Syntax</span></span>


```C++
DWORD ORGetValue(
  _In_        ORHKEY Handle,
  _In_opt_    PCWSTR lpSubKey,
  _In_opt_    PCWSTR lpValue,
  _Out_opt_   PDWORD pdwType,
  _Out_opt_   PVOID  pvData,
  _Inout_opt_ PDWORD pcbData
);
```



## <a name="parameters"></a><span data-ttu-id="18e28-106">參數</span><span class="sxs-lookup"><span data-stu-id="18e28-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18e28-107">*控制碼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="18e28-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18e28-108">離線登錄 hive 中開啟登錄機碼的控制碼。</span><span class="sxs-lookup"><span data-stu-id="18e28-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="18e28-109">*lpSubKey* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="18e28-109">*lpSubKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="18e28-110">登錄機碼的名稱。</span><span class="sxs-lookup"><span data-stu-id="18e28-110">The name of the registry key.</span></span> <span data-ttu-id="18e28-111">此索引鍵必須是 *控制碼* 參數所指定之金鑰的子機碼。</span><span class="sxs-lookup"><span data-stu-id="18e28-111">This key must be a subkey of the key specified by the *Handle* parameter.</span></span> <span data-ttu-id="18e28-112">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="18e28-112">This parameter can be **NULL**.</span></span>

<span data-ttu-id="18e28-113">索引鍵名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="18e28-113">Key names are not case sensitive.</span></span>

</dd> <dt>

<span data-ttu-id="18e28-114">*lpValue* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="18e28-114">*lpValue* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="18e28-115">登錄值的名稱。</span><span class="sxs-lookup"><span data-stu-id="18e28-115">The name of the registry value.</span></span> <span data-ttu-id="18e28-116">如果此參數為 **Null** 或空字串 ""，則函式會抓取索引鍵未命名或預設值（如果有的話）的類型和資料。</span><span class="sxs-lookup"><span data-stu-id="18e28-116">If this parameter is **NULL** or an empty string, "", the function retrieves the type and data for the key's unnamed or default value, if any.</span></span> <span data-ttu-id="18e28-117">如需詳細資訊，請參閱登錄 [元素大小限制](../sysinfo/registry-element-size-limits.md)。</span><span class="sxs-lookup"><span data-stu-id="18e28-117">For more information, see [Registry Element Size Limits](../sysinfo/registry-element-size-limits.md).</span></span>

<span data-ttu-id="18e28-118">索引鍵不會自動具有未命名或預設值。</span><span class="sxs-lookup"><span data-stu-id="18e28-118">Keys do not automatically have an unnamed or default value.</span></span> <span data-ttu-id="18e28-119">未命名的值可以是任何類型。</span><span class="sxs-lookup"><span data-stu-id="18e28-119">Unnamed values can be of any type.</span></span>

<span data-ttu-id="18e28-120">值名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="18e28-120">Value names are not case sensitive.</span></span>

</dd> <dt>

<span data-ttu-id="18e28-121">*pdwType* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="18e28-121">*pdwType* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="18e28-122">變數的指標，此變數會接收程式碼，指出儲存在指定值中的資料類型。</span><span class="sxs-lookup"><span data-stu-id="18e28-122">A pointer to a variable that receives a code indicating the type of data stored in the specified value.</span></span> <span data-ttu-id="18e28-123">如需可能的類型代碼清單，請參閱登錄 [數值型別](../sysinfo/registry-value-types.md)。</span><span class="sxs-lookup"><span data-stu-id="18e28-123">For a list of the possible type codes, see [Registry Value Types](../sysinfo/registry-value-types.md).</span></span> <span data-ttu-id="18e28-124">如果不需要型別，這個參數可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="18e28-124">This parameter can be **NULL** if the type is not required.</span></span>

</dd> <dt>

<span data-ttu-id="18e28-125">*pvData* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="18e28-125">*pvData* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="18e28-126">接收值資料之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="18e28-126">A pointer to a buffer that receives the value's data.</span></span> <span data-ttu-id="18e28-127">如果資料不是必要的，則此參數可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="18e28-127">This parameter can be **NULL** if the data is not required.</span></span>

<span data-ttu-id="18e28-128">如果資料是字串，此函式會檢查終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="18e28-128">If the data is a string, the function checks for a terminating null character.</span></span> <span data-ttu-id="18e28-129">如果找不到，則如果緩衝區夠大而足以容納額外的字元，則會以 null 結束字元儲存字串。</span><span class="sxs-lookup"><span data-stu-id="18e28-129">If one is not found, the string is stored with a null terminator if the buffer is large enough to accommodate the extra character.</span></span> <span data-ttu-id="18e28-130">否則，此函式會失敗並傳回錯誤 \_ \_ 的資料。</span><span class="sxs-lookup"><span data-stu-id="18e28-130">Otherwise, the function fails and returns ERROR\_MORE\_DATA.</span></span>

</dd> <dt>

<span data-ttu-id="18e28-131">*pcbData* \[in、out、optional\]</span><span class="sxs-lookup"><span data-stu-id="18e28-131">*pcbData* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="18e28-132">變數的指標，該變數會指定 *pvData* 參數所指向的緩衝區大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="18e28-132">A pointer to a variable that specifies the size of the buffer pointed to by the *pvData* parameter, in bytes.</span></span> <span data-ttu-id="18e28-133">當函數傳回時，這個變數會包含複製到 *pvData* 的資料大小。</span><span class="sxs-lookup"><span data-stu-id="18e28-133">When the function returns, this variable contains the size of the data copied to *pvData*.</span></span>

<span data-ttu-id="18e28-134">只有在 *pvData* 為 **Null** 時， *PcbData* 參數才可以是 **null** 。</span><span class="sxs-lookup"><span data-stu-id="18e28-134">The *pcbData* parameter can be **NULL** only if *pvData* is **NULL**.</span></span>

<span data-ttu-id="18e28-135">如果資料具有 REG \_ sz、reg \_ 多重 \_ SZ 或 reg \_ EXPAND 型別 \_ ，則此大小包含任何終止的 null 字元或字元。</span><span class="sxs-lookup"><span data-stu-id="18e28-135">If the data has the REG\_SZ, REG\_MULTI\_SZ or REG\_EXPAND\_SZ type, this size includes any terminating null character or characters.</span></span> <span data-ttu-id="18e28-136">如需詳細資訊，請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="18e28-136">For more information, see Remarks.</span></span>

<span data-ttu-id="18e28-137">如果 *pvData* 參數指定的緩衝區不夠大，無法容納資料，則函數會傳回錯誤 \_ \_ 的資料，並將所需的緩衝區大小儲存在 *pcbData* 所指向的變數中。</span><span class="sxs-lookup"><span data-stu-id="18e28-137">If the buffer specified by *pvData* parameter is not large enough to hold the data, the function returns ERROR\_MORE\_DATA and stores the required buffer size in the variable pointed to by *pcbData*.</span></span> <span data-ttu-id="18e28-138">在此情況下， *pvData* 緩衝區的內容是未定義的。</span><span class="sxs-lookup"><span data-stu-id="18e28-138">In this case, the contents of the *pvData* buffer are undefined.</span></span>

<span data-ttu-id="18e28-139">如果 *pvData* 為 **Null**，而 *pcbData* 為非 **Null**，則函式會傳回錯誤 \_ SUCCESS，並將資料的大小（以位元組為單位）儲存在 *pcbData* 所指向的變數中。</span><span class="sxs-lookup"><span data-stu-id="18e28-139">If *pvData* is **NULL**, and *pcbData* is non-**NULL**, the function returns ERROR\_SUCCESS and stores the size of the data, in bytes, in the variable pointed to by *pcbData*.</span></span> <span data-ttu-id="18e28-140">這可讓應用程式判斷為值的資料配置緩衝區的最佳方式。</span><span class="sxs-lookup"><span data-stu-id="18e28-140">This enables an application to determine the best way to allocate a buffer for the value's data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18e28-141">傳回值</span><span class="sxs-lookup"><span data-stu-id="18e28-141">Return value</span></span>

<span data-ttu-id="18e28-142">如果函式成功，則傳回值為「錯誤 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="18e28-142">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="18e28-143">如果函式失敗，則傳回值為 Winerror.h 中定義的非零錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="18e28-143">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="18e28-144">您可以使用 [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) 函數搭配系統旗標的格式 \_ 訊息 \_ \_ ，以取得錯誤的一般描述。</span><span class="sxs-lookup"><span data-stu-id="18e28-144">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="18e28-145">備註</span><span class="sxs-lookup"><span data-stu-id="18e28-145">Remarks</span></span>

<span data-ttu-id="18e28-146">應用程式通常會呼叫 [**OREnumValue**](orenumvalue.md) 函式來判斷值名稱，然後呼叫 **ORGetValue** 函數來取得名稱的資料。</span><span class="sxs-lookup"><span data-stu-id="18e28-146">An application typically calls the [**OREnumValue**](orenumvalue.md) function to determine the value names and then calls the **ORGetValue** function to retrieve the data for the names.</span></span>

## <a name="requirements"></a><span data-ttu-id="18e28-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="18e28-147">Requirements</span></span>



| <span data-ttu-id="18e28-148">需求</span><span class="sxs-lookup"><span data-stu-id="18e28-148">Requirement</span></span> | <span data-ttu-id="18e28-149">值</span><span class="sxs-lookup"><span data-stu-id="18e28-149">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="18e28-150">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="18e28-150">Redistributable</span></span><br/> | <span data-ttu-id="18e28-151">Windows Offline Registry library 1.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="18e28-151">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="18e28-152">標頭</span><span class="sxs-lookup"><span data-stu-id="18e28-152">Header</span></span><br/>          | <dl> <span data-ttu-id="18e28-153"><dt>Offreg。h</dt></span><span class="sxs-lookup"><span data-stu-id="18e28-153"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="18e28-154">DLL</span><span class="sxs-lookup"><span data-stu-id="18e28-154">DLL</span></span><br/>             | <dl> <span data-ttu-id="18e28-155"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18e28-155"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18e28-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18e28-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18e28-157">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="18e28-157">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="18e28-158">**OREnumKey**</span><span class="sxs-lookup"><span data-stu-id="18e28-158">**OREnumKey**</span></span>](orenumkey.md)
</dt> <dt>

[<span data-ttu-id="18e28-159">**OREnumValue**</span><span class="sxs-lookup"><span data-stu-id="18e28-159">**OREnumValue**</span></span>](orenumvalue.md)
</dt> <dt>

[<span data-ttu-id="18e28-160">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="18e28-160">**OROpenKey**</span></span>](oropenkey.md)
</dt> <dt>

[<span data-ttu-id="18e28-161">**ORQueryInfoKey**</span><span class="sxs-lookup"><span data-stu-id="18e28-161">**ORQueryInfoKey**</span></span>](orqueryinfokey.md)
</dt> </dl>

 

 
