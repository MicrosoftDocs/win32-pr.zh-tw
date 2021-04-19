---
description: 設定離線登錄區中所指定登錄機碼值的資料。
ms.assetid: 62fd3a3a-6ce3-4313-b0e7-37ceea0ce302
title: 'ORSetValue 函式 (Offreg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSetValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 3b11e9cb9a8425989e4ee513e0cfc18d2619ec4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978487"
---
# <a name="orsetvalue-function"></a><span data-ttu-id="7798b-103">ORSetValue 函式</span><span class="sxs-lookup"><span data-stu-id="7798b-103">ORSetValue function</span></span>

<span data-ttu-id="7798b-104">設定離線登錄區中所指定登錄機碼值的資料。</span><span class="sxs-lookup"><span data-stu-id="7798b-104">Sets the data for the value of a specified registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="7798b-105">語法</span><span class="sxs-lookup"><span data-stu-id="7798b-105">Syntax</span></span>


```C++
DWORD ORSetValue(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpValueName,
  _In_     DWORD  dwType,
  _In_opt_ const BYTE *lpData,
  _In_     DWORD  cbData
);
```



## <a name="parameters"></a><span data-ttu-id="7798b-106">參數</span><span class="sxs-lookup"><span data-stu-id="7798b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7798b-107">*控制碼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7798b-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7798b-108">離線登錄 hive 中開啟登錄機碼的控制碼。</span><span class="sxs-lookup"><span data-stu-id="7798b-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="7798b-109">*lpValueName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="7798b-109">*lpValueName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7798b-110">要設定的值名稱。</span><span class="sxs-lookup"><span data-stu-id="7798b-110">The name of the value to be set.</span></span> <span data-ttu-id="7798b-111">如果索引鍵中沒有這個名稱的值，則函式會將它新增至索引鍵。</span><span class="sxs-lookup"><span data-stu-id="7798b-111">If a value with this name is not already present in the key, the function adds it to the key.</span></span>

<span data-ttu-id="7798b-112">如果 *lpValueName* 為 **Null** 或空字串 ""，則函式會設定索引鍵未命名或預設值的類型和資料。</span><span class="sxs-lookup"><span data-stu-id="7798b-112">If *lpValueName* is **NULL** or an empty string, "", the function sets the type and data for the key's unnamed or default value.</span></span>

<span data-ttu-id="7798b-113">如需詳細資訊，請參閱登錄 [元素大小限制](../sysinfo/registry-element-size-limits.md)。</span><span class="sxs-lookup"><span data-stu-id="7798b-113">For more information, see [Registry Element Size Limits](../sysinfo/registry-element-size-limits.md).</span></span>

<span data-ttu-id="7798b-114">登錄機碼沒有預設值，但可以有一個未命名的值，它可以是任何類型。</span><span class="sxs-lookup"><span data-stu-id="7798b-114">Registry keys do not have default values, but they can have one unnamed value, which can be of any type.</span></span>

</dd> <dt>

<span data-ttu-id="7798b-115">*dwType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7798b-115">*dwType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7798b-116">*LpData* 參數所指向的資料類型。</span><span class="sxs-lookup"><span data-stu-id="7798b-116">The type of data pointed to by the *lpData* parameter.</span></span> <span data-ttu-id="7798b-117">如需可能類型的清單，請參閱登錄 [數值型別](../sysinfo/registry-value-types.md)。</span><span class="sxs-lookup"><span data-stu-id="7798b-117">For a list of the possible types, see [Registry Value Types](../sysinfo/registry-value-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="7798b-118">*lpData* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="7798b-118">*lpData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7798b-119">要儲存的資料。</span><span class="sxs-lookup"><span data-stu-id="7798b-119">The data to be stored.</span></span>

<span data-ttu-id="7798b-120">如果是以字串為基礎的類型，例如 REG \_ SZ，則字串必須以 null 結束。</span><span class="sxs-lookup"><span data-stu-id="7798b-120">For string-based types, such as REG\_SZ, the string must be null-terminated.</span></span> <span data-ttu-id="7798b-121">若為 REG \_ 多重 \_ SZ 資料類型，字串必須以兩個 null 字元結束。</span><span class="sxs-lookup"><span data-stu-id="7798b-121">For the REG\_MULTI\_SZ data type, the string must be terminated with two null characters.</span></span>

</dd> <dt>

<span data-ttu-id="7798b-122">*cbData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7798b-122">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7798b-123">*LpData* 參數所指向的資訊大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7798b-123">The size of the information pointed to by the *lpData* parameter, in bytes.</span></span> <span data-ttu-id="7798b-124">如果資料的類型是 REG \_ SZ、reg \_ EXPAND \_ sz 或 REG \_ 多重 \_ SZ， *cbData* 必須包含終止的 null 字元或字元的大小。</span><span class="sxs-lookup"><span data-stu-id="7798b-124">If the data is of type REG\_SZ, REG\_EXPAND\_SZ, or REG\_MULTI\_SZ, *cbData* must include the size of the terminating null character or characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7798b-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="7798b-125">Return value</span></span>

<span data-ttu-id="7798b-126">如果函式成功，則傳回值為「錯誤 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="7798b-126">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="7798b-127">如果函式失敗，則傳回值為 Winerror.h 中定義的非零錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7798b-127">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="7798b-128">您可以使用 [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) 函數搭配系統旗標的格式 \_ 訊息 \_ \_ ，以取得錯誤的一般描述。</span><span class="sxs-lookup"><span data-stu-id="7798b-128">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="7798b-129">備註</span><span class="sxs-lookup"><span data-stu-id="7798b-129">Remarks</span></span>

<span data-ttu-id="7798b-130">值大小會受到可用記憶體的限制。</span><span class="sxs-lookup"><span data-stu-id="7798b-130">Value sizes are limited by available memory.</span></span> <span data-ttu-id="7798b-131">Long 值 (超過2048個位元組) 應儲存為檔案，並將檔案名儲存在登錄中。</span><span class="sxs-lookup"><span data-stu-id="7798b-131">Long values (more than 2048 bytes) should be stored as files with the file names stored in the registry.</span></span> <span data-ttu-id="7798b-132">這有助於登錄有效率地執行。</span><span class="sxs-lookup"><span data-stu-id="7798b-132">This helps the registry perform efficiently.</span></span> <span data-ttu-id="7798b-133">應用程式元素（例如圖示、點陣圖和可執行檔）應該儲存為檔案，而不是放在登錄中。</span><span class="sxs-lookup"><span data-stu-id="7798b-133">Application elements such as icons, bitmaps, and executable files should be stored as files and not be placed in the registry.</span></span>

## <a name="requirements"></a><span data-ttu-id="7798b-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="7798b-134">Requirements</span></span>



| <span data-ttu-id="7798b-135">需求</span><span class="sxs-lookup"><span data-stu-id="7798b-135">Requirement</span></span> | <span data-ttu-id="7798b-136">值</span><span class="sxs-lookup"><span data-stu-id="7798b-136">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7798b-137">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="7798b-137">Redistributable</span></span><br/> | <span data-ttu-id="7798b-138">Windows Offline Registry library 1.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="7798b-138">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="7798b-139">標頭</span><span class="sxs-lookup"><span data-stu-id="7798b-139">Header</span></span><br/>          | <dl> <span data-ttu-id="7798b-140"><dt>Offreg。h</dt></span><span class="sxs-lookup"><span data-stu-id="7798b-140"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="7798b-141">DLL</span><span class="sxs-lookup"><span data-stu-id="7798b-141">DLL</span></span><br/>             | <dl> <span data-ttu-id="7798b-142"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7798b-142"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7798b-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7798b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7798b-144">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="7798b-144">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="7798b-145">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="7798b-145">**OROpenKey**</span></span>](oropenkey.md)
</dt> </dl>

 

 
