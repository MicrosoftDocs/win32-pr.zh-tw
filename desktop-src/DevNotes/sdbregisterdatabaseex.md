---
description: 註冊指定的資料庫。
ms.assetid: 65eceb1a-9ce1-4b97-98d7-731932797794
title: SdbRegisterDatabaseEx 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbRegisterDatabaseEx
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 74872f8895032abe02b024396fda12c43dc1611d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510497"
---
# <a name="sdbregisterdatabaseex-function"></a><span data-ttu-id="c2537-103">SdbRegisterDatabaseEx 函式</span><span class="sxs-lookup"><span data-stu-id="c2537-103">SdbRegisterDatabaseEx function</span></span>

<span data-ttu-id="c2537-104">註冊指定的資料庫。</span><span class="sxs-lookup"><span data-stu-id="c2537-104">Registers the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2537-105">語法</span><span class="sxs-lookup"><span data-stu-id="c2537-105">Syntax</span></span>


```C++
BOOL WINAPI SdbRegisterDatabaseEx(
  _In_     LPCTSTR    pszDatabasePath,
  _In_     DWORD      dwDatabaseType,
  _In_opt_ PULONGLONG pTimeStamp
);
```



## <a name="parameters"></a><span data-ttu-id="c2537-106">參數</span><span class="sxs-lookup"><span data-stu-id="c2537-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2537-107">*pszDatabasePath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c2537-107">*pszDatabasePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2537-108">資料庫路徑。</span><span class="sxs-lookup"><span data-stu-id="c2537-108">The database path.</span></span> <span data-ttu-id="c2537-109">此參數不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c2537-109">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c2537-110">*dwDatabaseType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c2537-110">*dwDatabaseType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2537-111">資料庫類型。</span><span class="sxs-lookup"><span data-stu-id="c2537-111">The database type.</span></span> <span data-ttu-id="c2537-112">如需值清單，請參閱 [填充碼資料庫類型](shim-database-types.md) 。</span><span class="sxs-lookup"><span data-stu-id="c2537-112">See [Shim Database Types](shim-database-types.md) for a list of values.</span></span>

</dd> <dt>

<span data-ttu-id="c2537-113">*pTimeStamp* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="c2537-113">*pTimeStamp* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c2537-114">資料庫的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="c2537-114">The time stamp for the database.</span></span> <span data-ttu-id="c2537-115">如果此參數為 **Null**，則會使用系統時間。</span><span class="sxs-lookup"><span data-stu-id="c2537-115">If this parameter is **NULL**, the system time is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2537-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="c2537-116">Return value</span></span>

<span data-ttu-id="c2537-117">當失敗時，函數會傳回 **TRUE** 或 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="c2537-117">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2537-118">備註</span><span class="sxs-lookup"><span data-stu-id="c2537-118">Remarks</span></span>

<span data-ttu-id="c2537-119">您必須先註冊資料庫，才能使用任何其他的 SDB 函數。</span><span class="sxs-lookup"><span data-stu-id="c2537-119">A database must be registered before you can use any other SDB functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2537-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="c2537-120">Requirements</span></span>



| <span data-ttu-id="c2537-121">需求</span><span class="sxs-lookup"><span data-stu-id="c2537-121">Requirement</span></span> | <span data-ttu-id="c2537-122">值</span><span class="sxs-lookup"><span data-stu-id="c2537-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2537-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c2537-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c2537-124">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c2537-124">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="c2537-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c2537-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c2537-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c2537-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c2537-127">DLL</span><span class="sxs-lookup"><span data-stu-id="c2537-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2537-128"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2537-128"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2537-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c2537-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2537-130">**SdbUnregisterDatabase**</span><span class="sxs-lookup"><span data-stu-id="c2537-130">**SdbUnregisterDatabase**</span></span>](sdbunregisterdatabase.md)
</dt> </dl>

 

 




