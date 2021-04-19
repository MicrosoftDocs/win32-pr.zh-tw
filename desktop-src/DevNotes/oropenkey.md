---
description: 在離線登錄 hive 中開啟指定的登錄機碼。
ms.assetid: 4a4afbef-5107-4006-bd67-aecb5d3b5112
title: 'OROpenKey 函式 (Offreg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OROpenKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 4a55bb2c06d8b2d13491b766bf08184631fa2164
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987830"
---
# <a name="oropenkey-function"></a><span data-ttu-id="450b2-103">OROpenKey 函式</span><span class="sxs-lookup"><span data-stu-id="450b2-103">OROpenKey function</span></span>

<span data-ttu-id="450b2-104">在離線登錄 hive 中開啟指定的登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="450b2-104">Opens the specified registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="450b2-105">語法</span><span class="sxs-lookup"><span data-stu-id="450b2-105">Syntax</span></span>


```C++
DWORD OROpenKey(
  _In_     ORHKEY  Handle,
  _In_opt_ PCWSTR  lpSubKeyName,
  _Out_    PORHKEY phkResult
);
```



## <a name="parameters"></a><span data-ttu-id="450b2-106">參數</span><span class="sxs-lookup"><span data-stu-id="450b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="450b2-107">*控制碼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="450b2-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="450b2-108">離線登錄 hive 中開啟登錄機碼的控制碼。</span><span class="sxs-lookup"><span data-stu-id="450b2-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="450b2-109">*lpSubKeyName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="450b2-109">*lpSubKeyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="450b2-110">UNICODE 字串的指標，其中包含要開啟的登錄機碼名稱。</span><span class="sxs-lookup"><span data-stu-id="450b2-110">A pointer to a UNICODE string that contains the name of the registry key to be opened.</span></span> <span data-ttu-id="450b2-111">此索引鍵必須是 *控制碼* 參數所識別之機碼的子機碼。</span><span class="sxs-lookup"><span data-stu-id="450b2-111">This key must be a subkey of the key identified by the *Handle* parameter.</span></span>

<span data-ttu-id="450b2-112">索引鍵名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="450b2-112">Key names are not case sensitive.</span></span>

<span data-ttu-id="450b2-113">如果此參數為 **Null** 或空字串的指標，則函數會傳回傳入的相同控制碼。</span><span class="sxs-lookup"><span data-stu-id="450b2-113">If this parameter is **NULL** or a pointer to an empty string, the function returns the same handle that was passed in.</span></span> <span data-ttu-id="450b2-114">如果 *Handle* 參數所指定的索引鍵是 hive 的根金鑰，則函式會傳回錯誤 \_ 不正確 \_ 參數。</span><span class="sxs-lookup"><span data-stu-id="450b2-114">If the key specified by the *Handle* parameter is the root key of the hive, the function returns ERROR\_INVALID\_PARAMETER.</span></span>

<span data-ttu-id="450b2-115">如需詳細資訊，請參閱登錄 [元素大小限制](../sysinfo/registry-element-size-limits.md)。</span><span class="sxs-lookup"><span data-stu-id="450b2-115">For more information, see [Registry Element Size Limits](../sysinfo/registry-element-size-limits.md).</span></span>

</dd> <dt>

<span data-ttu-id="450b2-116">*phkResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="450b2-116">*phkResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="450b2-117">變數的指標，此變數會接收開啟之索引鍵的控制碼。</span><span class="sxs-lookup"><span data-stu-id="450b2-117">A pointer to a variable that receives a handle to the opened key.</span></span> <span data-ttu-id="450b2-118">當您完成使用控制碼之後，請使用 [**ORCloseKey**](orclosekey.md) 函數來關閉金鑰。</span><span class="sxs-lookup"><span data-stu-id="450b2-118">Use the [**ORCloseKey**](orclosekey.md) function to close the key after you have finished using the handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="450b2-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="450b2-119">Return value</span></span>

<span data-ttu-id="450b2-120">如果函式成功，則傳回值為「錯誤 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="450b2-120">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="450b2-121">如果函式失敗，則傳回值為 Winerror.h 中定義的非零錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="450b2-121">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="450b2-122">您可以使用 [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) 函數搭配系統旗標的格式 \_ 訊息 \_ \_ ，以取得錯誤的一般描述。</span><span class="sxs-lookup"><span data-stu-id="450b2-122">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="450b2-123">如果要傳回的控制碼會是 hive 根金鑰的控制碼，則函式會傳回錯誤不正確 \_ \_ 參數。</span><span class="sxs-lookup"><span data-stu-id="450b2-123">If the handle to be returned would be a handle to the root key of the hive, the function returns ERROR\_INVALID\_PARAMETER.</span></span>

<span data-ttu-id="450b2-124">如果指定的索引鍵已標示為已刪除，則此函式會傳回已刪除的錯誤索引 \_ 鍵 \_ 。</span><span class="sxs-lookup"><span data-stu-id="450b2-124">If the specified key has been marked as deleted, this function returns ERROR\_KEY\_DELETED.</span></span>

## <a name="remarks"></a><span data-ttu-id="450b2-125">備註</span><span class="sxs-lookup"><span data-stu-id="450b2-125">Remarks</span></span>

<span data-ttu-id="450b2-126">**OROpenKey** 函式不能用來開啟離線登錄區中的根機碼。</span><span class="sxs-lookup"><span data-stu-id="450b2-126">The **OROpenKey** function cannot be used to open the root key in an offline registry hive.</span></span> <span data-ttu-id="450b2-127">若要取得 hive 根金鑰的控制碼，請使用 [**OROpenHive**](oropenhive.md) 函式將 hive 載入記憶體中。</span><span class="sxs-lookup"><span data-stu-id="450b2-127">To obtain a handle to the root key of a hive, use the [**OROpenHive**](oropenhive.md) function to load the hive into memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="450b2-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="450b2-128">Requirements</span></span>



| <span data-ttu-id="450b2-129">需求</span><span class="sxs-lookup"><span data-stu-id="450b2-129">Requirement</span></span> | <span data-ttu-id="450b2-130">值</span><span class="sxs-lookup"><span data-stu-id="450b2-130">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="450b2-131">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="450b2-131">Redistributable</span></span><br/> | <span data-ttu-id="450b2-132">Windows Offline Registry library 1.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="450b2-132">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="450b2-133">標頭</span><span class="sxs-lookup"><span data-stu-id="450b2-133">Header</span></span><br/>          | <dl> <span data-ttu-id="450b2-134"><dt>Offreg。h</dt></span><span class="sxs-lookup"><span data-stu-id="450b2-134"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="450b2-135">DLL</span><span class="sxs-lookup"><span data-stu-id="450b2-135">DLL</span></span><br/>             | <dl> <span data-ttu-id="450b2-136"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="450b2-136"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="450b2-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="450b2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="450b2-138">**ORCloseKey**</span><span class="sxs-lookup"><span data-stu-id="450b2-138">**ORCloseKey**</span></span>](orclosekey.md)
</dt> <dt>

[<span data-ttu-id="450b2-139">**ORCreateKey**</span><span class="sxs-lookup"><span data-stu-id="450b2-139">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="450b2-140">**ORDeleteKey**</span><span class="sxs-lookup"><span data-stu-id="450b2-140">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> <dt>

[<span data-ttu-id="450b2-141">**OROpenHive**</span><span class="sxs-lookup"><span data-stu-id="450b2-141">**OROpenHive**</span></span>](oropenhive.md)
</dt> </dl>

 

 
