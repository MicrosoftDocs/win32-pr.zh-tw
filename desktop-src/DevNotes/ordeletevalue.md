---
description: 從離線登錄區的指定登錄機碼中移除指定的值。
ms.assetid: d2192607-34b8-4915-ac86-8ee206993071
title: 'ORDeleteValue 函式 (Offreg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORDeleteValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 426765950fd38cbb3e3c99f4001db2965ddb07e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995454"
---
# <a name="ordeletevalue-function"></a><span data-ttu-id="e0e4b-103">ORDeleteValue 函式</span><span class="sxs-lookup"><span data-stu-id="e0e4b-103">ORDeleteValue function</span></span>

<span data-ttu-id="e0e4b-104">從離線登錄區的指定登錄機碼中移除指定的值。</span><span class="sxs-lookup"><span data-stu-id="e0e4b-104">Removes a named value from the specified registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0e4b-105">語法</span><span class="sxs-lookup"><span data-stu-id="e0e4b-105">Syntax</span></span>


```C++
DWORD ORDeleteValue(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpValueName
);
```



## <a name="parameters"></a><span data-ttu-id="e0e4b-106">參數</span><span class="sxs-lookup"><span data-stu-id="e0e4b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0e4b-107">*控制碼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e0e4b-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0e4b-108">離線登錄 hive 中開啟登錄機碼的控制碼。</span><span class="sxs-lookup"><span data-stu-id="e0e4b-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="e0e4b-109">*lpValueName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="e0e4b-109">*lpValueName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e0e4b-110">要移除的登錄值。</span><span class="sxs-lookup"><span data-stu-id="e0e4b-110">The registry value to be removed.</span></span> <span data-ttu-id="e0e4b-111">如果此參數為 **Null** 或空字串，則會移除 [**ORSetValue**](orsetvalue.md) 函數所設定的預設未命名值。</span><span class="sxs-lookup"><span data-stu-id="e0e4b-111">If this parameter is **NULL** or an empty string, the default unnamed value set by the [**ORSetValue**](orsetvalue.md) function is removed.</span></span>

<span data-ttu-id="e0e4b-112">值名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="e0e4b-112">Value names are not case sensitive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0e4b-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="e0e4b-113">Return value</span></span>

<span data-ttu-id="e0e4b-114">如果函式成功，則傳回值為「錯誤 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="e0e4b-114">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="e0e4b-115">如果函式失敗，則傳回值為 Winerror.h 中定義的非零錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e0e4b-115">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="e0e4b-116">您可以使用 [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) 函數搭配系統旗標的格式 \_ 訊息 \_ \_ ，以取得錯誤的一般描述。</span><span class="sxs-lookup"><span data-stu-id="e0e4b-116">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0e4b-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="e0e4b-117">Requirements</span></span>



| <span data-ttu-id="e0e4b-118">需求</span><span class="sxs-lookup"><span data-stu-id="e0e4b-118">Requirement</span></span> | <span data-ttu-id="e0e4b-119">值</span><span class="sxs-lookup"><span data-stu-id="e0e4b-119">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e0e4b-120">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="e0e4b-120">Redistributable</span></span><br/> | <span data-ttu-id="e0e4b-121">Windows Offline Registry library 1.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="e0e4b-121">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="e0e4b-122">標頭</span><span class="sxs-lookup"><span data-stu-id="e0e4b-122">Header</span></span><br/>          | <dl> <span data-ttu-id="e0e4b-123"><dt>Offreg。h</dt></span><span class="sxs-lookup"><span data-stu-id="e0e4b-123"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="e0e4b-124">DLL</span><span class="sxs-lookup"><span data-stu-id="e0e4b-124">DLL</span></span><br/>             | <dl> <span data-ttu-id="e0e4b-125"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0e4b-125"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0e4b-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e0e4b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0e4b-127">**ORSetValue**</span><span class="sxs-lookup"><span data-stu-id="e0e4b-127">**ORSetValue**</span></span>](orsetvalue.md)
</dt> </dl>

 

 
