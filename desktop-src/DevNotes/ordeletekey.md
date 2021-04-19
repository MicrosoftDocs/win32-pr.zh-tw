---
description: 從離線登錄 hive 刪除子機碼及其值。
ms.assetid: 651795d3-4328-4281-9a7f-ba75b4ec4da1
title: 'ORDeleteKey 函式 (Offreg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORDeleteKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: a122be2e738bb16730eee31772fc2c1c0671eddb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984405"
---
# <a name="ordeletekey-function"></a><span data-ttu-id="0e3f6-103">ORDeleteKey 函式</span><span class="sxs-lookup"><span data-stu-id="0e3f6-103">ORDeleteKey function</span></span>

<span data-ttu-id="0e3f6-104">從離線登錄 hive 刪除子機碼及其值。</span><span class="sxs-lookup"><span data-stu-id="0e3f6-104">Deletes a subkey and its values from an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e3f6-105">語法</span><span class="sxs-lookup"><span data-stu-id="0e3f6-105">Syntax</span></span>


```C++
DWORD ORDeleteKey(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpSubKey
);
```



## <a name="parameters"></a><span data-ttu-id="0e3f6-106">參數</span><span class="sxs-lookup"><span data-stu-id="0e3f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e3f6-107">*控制碼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0e3f6-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e3f6-108">離線登錄 hive 中開啟登錄機碼的控制碼。</span><span class="sxs-lookup"><span data-stu-id="0e3f6-108">A handle to an open registry key in an offline registry hive.</span></span> <span data-ttu-id="0e3f6-109">[**ORCreateKey**](orcreatekey.md)或 [**OROpenKey**](oropenkey.md)函數會傳回此控制碼。</span><span class="sxs-lookup"><span data-stu-id="0e3f6-109">This handle is returned by the [**ORCreateKey**](orcreatekey.md) or [**OROpenKey**](oropenkey.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="0e3f6-110">*lpSubKey* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="0e3f6-110">*lpSubKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0e3f6-111">要刪除之金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e3f6-111">The name of the key to be deleted.</span></span> <span data-ttu-id="0e3f6-112">它必須是 *處理* 識別之金鑰的子機碼，但不能有子機碼。</span><span class="sxs-lookup"><span data-stu-id="0e3f6-112">It must be a subkey of the key that *Handle* identifies, but it cannot have subkeys.</span></span>

<span data-ttu-id="0e3f6-113">如果子機碼不存在，則函式會傳回「找不到錯誤」 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="0e3f6-113">If the subkey does not exist, the function returns ERROR\_NOT\_FOUND.</span></span>

<span data-ttu-id="0e3f6-114">如果這個參數為 **Null**，則函式會刪除 *Handle* 參數所指定的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="0e3f6-114">If this parameter is **NULL**, the function deletes the key specified by the *Handle* parameter.</span></span> <span data-ttu-id="0e3f6-115">如果 *Handle* 參數所指定的索引鍵是 hive 的根金鑰，則函式會傳回錯誤 \_ 不正確 \_ 參數。</span><span class="sxs-lookup"><span data-stu-id="0e3f6-115">If the key specified by the *Handle* parameter is the root key of the hive, the function returns ERROR\_INVALID\_PARAMETER.</span></span>

<span data-ttu-id="0e3f6-116">索引鍵名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="0e3f6-116">Key names are not case sensitive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e3f6-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="0e3f6-117">Return value</span></span>

<span data-ttu-id="0e3f6-118">如果函式成功，則傳回值為「錯誤 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="0e3f6-118">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="0e3f6-119">如果函式失敗，則傳回值為 Winerror.h 中定義的非零錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0e3f6-119">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="0e3f6-120">您可以使用 [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) 函數搭配系統旗標的格式 \_ 訊息 \_ \_ ，以取得錯誤的一般描述。</span><span class="sxs-lookup"><span data-stu-id="0e3f6-120">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span> <span data-ttu-id="0e3f6-121">可能的錯誤代碼包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="0e3f6-121">Possible error codes include the following:</span></span>

-   <span data-ttu-id="0e3f6-122">如果指定的子機碼不存在，則函數會 \_ 傳回 \_ 找不到的錯誤檔案 \_ 。</span><span class="sxs-lookup"><span data-stu-id="0e3f6-122">If the specified subkey does not exist, the function returns ERROR\_FILE\_NOT\_FOUND.</span></span>
-   <span data-ttu-id="0e3f6-123">如果指定的子機碼是登錄區的根金鑰，則函式會傳回錯誤 \_ 不正確 \_ 參數。</span><span class="sxs-lookup"><span data-stu-id="0e3f6-123">If the specified subkey is the root key of the registry hive, the function returns ERROR\_INVALID\_PARAMETER.</span></span>
-   <span data-ttu-id="0e3f6-124">如果指定的子機碼有子機碼，此函式會傳回錯誤索引 \_ 鍵的 \_ 子系 \_ 。</span><span class="sxs-lookup"><span data-stu-id="0e3f6-124">If the specified subkey has subkeys, the function returns ERROR\_KEY\_HAS\_CHILDREN.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e3f6-125">備註</span><span class="sxs-lookup"><span data-stu-id="0e3f6-125">Remarks</span></span>

<span data-ttu-id="0e3f6-126">如果指定的登錄機碼存在，則會標示為已刪除。</span><span class="sxs-lookup"><span data-stu-id="0e3f6-126">If the specified registry key exists, it is marked as deleted.</span></span> <span data-ttu-id="0e3f6-127">未移除已刪除的金鑰，直到其最後一個控制碼關閉為止。</span><span class="sxs-lookup"><span data-stu-id="0e3f6-127">A deleted key is not removed until the last handle to it is closed.</span></span>

<span data-ttu-id="0e3f6-128">要刪除的金鑰不能有子機碼。</span><span class="sxs-lookup"><span data-stu-id="0e3f6-128">The key to be deleted must not have subkeys.</span></span> <span data-ttu-id="0e3f6-129">若要刪除索引鍵及其所有子機碼，請使用 [**OREnumKey**](orenumkey.md) 函式來列舉子機碼，並個別將其刪除。</span><span class="sxs-lookup"><span data-stu-id="0e3f6-129">To delete a key and all its subkeys, use the [**OREnumKey**](orenumkey.md) function to enumerate the subkeys and delete them individually.</span></span>

<span data-ttu-id="0e3f6-130">只有 [**ORCloseKey**](orclosekey.md) 函數可以在已刪除的金鑰上呼叫;所有其他離線登錄作業都會失敗。</span><span class="sxs-lookup"><span data-stu-id="0e3f6-130">Only the [**ORCloseKey**](orclosekey.md) function may be called on a deleted key; all other offline registry operations fail.</span></span> <span data-ttu-id="0e3f6-131">如果已刪除的金鑰是藉由呼叫 [**ORCreateKey**](orcreatekey.md)來明確建立的，則會在最後一個已刪除金鑰的控制碼關閉時釋出與該金鑰相關聯的資源。</span><span class="sxs-lookup"><span data-stu-id="0e3f6-131">If the deleted key was explicitly created by calling [**ORCreateKey**](orcreatekey.md), resources associated with the key are released when the last handle to the deleted key is closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e3f6-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="0e3f6-132">Requirements</span></span>



| <span data-ttu-id="0e3f6-133">需求</span><span class="sxs-lookup"><span data-stu-id="0e3f6-133">Requirement</span></span> | <span data-ttu-id="0e3f6-134">值</span><span class="sxs-lookup"><span data-stu-id="0e3f6-134">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0e3f6-135">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="0e3f6-135">Redistributable</span></span><br/> | <span data-ttu-id="0e3f6-136">Windows Offline Registry library 1.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="0e3f6-136">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="0e3f6-137">標頭</span><span class="sxs-lookup"><span data-stu-id="0e3f6-137">Header</span></span><br/>          | <dl> <span data-ttu-id="0e3f6-138"><dt>Offreg。h</dt></span><span class="sxs-lookup"><span data-stu-id="0e3f6-138"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="0e3f6-139">DLL</span><span class="sxs-lookup"><span data-stu-id="0e3f6-139">DLL</span></span><br/>             | <dl> <span data-ttu-id="0e3f6-140"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e3f6-140"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e3f6-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0e3f6-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e3f6-142">**ORCloseKey**</span><span class="sxs-lookup"><span data-stu-id="0e3f6-142">**ORCloseKey**</span></span>](orclosekey.md)
</dt> <dt>

[<span data-ttu-id="0e3f6-143">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="0e3f6-143">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="0e3f6-144">**OREnumKey**</span><span class="sxs-lookup"><span data-stu-id="0e3f6-144">**OREnumKey**</span></span>](orenumkey.md)
</dt> <dt>

[<span data-ttu-id="0e3f6-145">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="0e3f6-145">**OROpenKey**</span></span>](oropenkey.md)
</dt> </dl>

 

 
