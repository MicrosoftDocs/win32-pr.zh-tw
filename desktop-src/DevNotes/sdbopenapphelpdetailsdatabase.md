---
description: 開啟指定的 Apphelp 詳細資料資料庫。
ms.assetid: c3b07c00-a3c6-419c-94c6-34c573a04d6d
title: SdbOpenApphelpDetailsDatabase 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenApphelpDetailsDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 2810b0bbe1f10f013f39570aecda448a4ceeea6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104109916"
---
# <a name="sdbopenapphelpdetailsdatabase-function"></a><span data-ttu-id="6da57-103">SdbOpenApphelpDetailsDatabase 函式</span><span class="sxs-lookup"><span data-stu-id="6da57-103">SdbOpenApphelpDetailsDatabase function</span></span>

<span data-ttu-id="6da57-104">開啟指定的 Apphelp 詳細資料資料庫。</span><span class="sxs-lookup"><span data-stu-id="6da57-104">Opens the specified Apphelp details database.</span></span>

## <a name="syntax"></a><span data-ttu-id="6da57-105">語法</span><span class="sxs-lookup"><span data-stu-id="6da57-105">Syntax</span></span>


```C++
PDB WINAPI SdbOpenApphelpDetailsDatabase(
  _In_opt_ LPCWSTR pwsDetailsDatabasePath
);
```



## <a name="parameters"></a><span data-ttu-id="6da57-106">參數</span><span class="sxs-lookup"><span data-stu-id="6da57-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6da57-107">*pwsDetailsDatabasePath* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="6da57-107">*pwsDetailsDatabasePath* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6da57-108">資料庫路徑。</span><span class="sxs-lookup"><span data-stu-id="6da57-108">The database path.</span></span> <span data-ttu-id="6da57-109">如果此參數為 **Null**，則會開啟本機系統資料庫。</span><span class="sxs-lookup"><span data-stu-id="6da57-109">If this parameter is **NULL**, the local system database is opened.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6da57-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="6da57-110">Return value</span></span>

<span data-ttu-id="6da57-111">函數會傳回 Apphelp details 資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6da57-111">The function returns a handle to the Apphelp details database.</span></span>

## <a name="requirements"></a><span data-ttu-id="6da57-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="6da57-112">Requirements</span></span>



| <span data-ttu-id="6da57-113">需求</span><span class="sxs-lookup"><span data-stu-id="6da57-113">Requirement</span></span> | <span data-ttu-id="6da57-114">值</span><span class="sxs-lookup"><span data-stu-id="6da57-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6da57-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6da57-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6da57-116">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6da57-116">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="6da57-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6da57-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6da57-118">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6da57-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6da57-119">DLL</span><span class="sxs-lookup"><span data-stu-id="6da57-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6da57-120"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6da57-120"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




