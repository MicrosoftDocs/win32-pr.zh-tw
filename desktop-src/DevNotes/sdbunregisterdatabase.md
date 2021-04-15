---
description: 取消註冊指定的資料庫，使其無法再使用。
ms.assetid: 7e6c50f4-85f6-4b33-b639-d8fda143e5e7
title: SdbUnregisterDatabase 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbUnregisterDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 72171e1f9ae20ac2213a285046b2499093be4313
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468145"
---
# <a name="sdbunregisterdatabase-function"></a><span data-ttu-id="a947c-103">SdbUnregisterDatabase 函式</span><span class="sxs-lookup"><span data-stu-id="a947c-103">SdbUnregisterDatabase function</span></span>

<span data-ttu-id="a947c-104">取消註冊指定的資料庫，使其無法再使用。</span><span class="sxs-lookup"><span data-stu-id="a947c-104">Unregisters the specified database, making it no longer available.</span></span>

## <a name="syntax"></a><span data-ttu-id="a947c-105">語法</span><span class="sxs-lookup"><span data-stu-id="a947c-105">Syntax</span></span>


```C++
BOOL WINAPI SdbUnregisterDatabase(
  _In_ GUID *pguidDB
);
```



## <a name="parameters"></a><span data-ttu-id="a947c-106">參數</span><span class="sxs-lookup"><span data-stu-id="a947c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a947c-107">*pguidDB* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a947c-107">*pguidDB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a947c-108">資料庫的 GUID。</span><span class="sxs-lookup"><span data-stu-id="a947c-108">The GUID of the database.</span></span> <span data-ttu-id="a947c-109">此參數不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a947c-109">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a947c-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="a947c-110">Return value</span></span>

<span data-ttu-id="a947c-111">當失敗時，函數會傳回 **TRUE** 或 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="a947c-111">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="a947c-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="a947c-112">Requirements</span></span>



| <span data-ttu-id="a947c-113">需求</span><span class="sxs-lookup"><span data-stu-id="a947c-113">Requirement</span></span> | <span data-ttu-id="a947c-114">值</span><span class="sxs-lookup"><span data-stu-id="a947c-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a947c-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a947c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a947c-116">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a947c-116">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="a947c-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a947c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a947c-118">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a947c-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a947c-119">DLL</span><span class="sxs-lookup"><span data-stu-id="a947c-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a947c-120"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a947c-120"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a947c-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a947c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a947c-122">**SdbRegisterDatabaseEx**</span><span class="sxs-lookup"><span data-stu-id="a947c-122">**SdbRegisterDatabaseEx**</span></span>](sdbregisterdatabaseex.md)
</dt> </dl>

 

 




