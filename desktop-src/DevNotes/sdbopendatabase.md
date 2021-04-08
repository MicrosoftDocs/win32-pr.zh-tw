---
description: 開啟指定的填充碼資料庫。
ms.assetid: 148181d7-a20a-467c-984b-e32013960783
title: SdbOpenDatabase 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: ae0bca035f203593c43bb36e70119fbaf3024059
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688604"
---
# <a name="sdbopendatabase-function"></a><span data-ttu-id="7a388-103">SdbOpenDatabase 函式</span><span class="sxs-lookup"><span data-stu-id="7a388-103">SdbOpenDatabase function</span></span>

<span data-ttu-id="7a388-104">開啟指定的填充碼資料庫。</span><span class="sxs-lookup"><span data-stu-id="7a388-104">Opens the specified shim database.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a388-105">語法</span><span class="sxs-lookup"><span data-stu-id="7a388-105">Syntax</span></span>


```C++
PDB WINAPI SdbOpenDatabase(
  _In_ LPCTSTR   pwszPath,
  _In_ PATH_TYPE eType
);
```



## <a name="parameters"></a><span data-ttu-id="7a388-106">參數</span><span class="sxs-lookup"><span data-stu-id="7a388-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a388-107">*pwszPath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7a388-107">*pwszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a388-108">資料庫路徑。</span><span class="sxs-lookup"><span data-stu-id="7a388-108">The database path.</span></span> <span data-ttu-id="7a388-109">此參數不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="7a388-109">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7a388-110">*eType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7a388-110">*eType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a388-111">路徑類型。</span><span class="sxs-lookup"><span data-stu-id="7a388-111">The path type.</span></span> <span data-ttu-id="7a388-112">如需值清單，請參閱 [**路徑 \_ 類型**](path-type.md) 。</span><span class="sxs-lookup"><span data-stu-id="7a388-112">See [**PATH\_TYPE**](path-type.md) for a list of values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a388-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="7a388-113">Return value</span></span>

<span data-ttu-id="7a388-114">函數會傳回填充碼資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="7a388-114">The function returns a handle to the shim database.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a388-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="7a388-115">Requirements</span></span>



| <span data-ttu-id="7a388-116">需求</span><span class="sxs-lookup"><span data-stu-id="7a388-116">Requirement</span></span> | <span data-ttu-id="7a388-117">值</span><span class="sxs-lookup"><span data-stu-id="7a388-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a388-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7a388-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7a388-119">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7a388-119">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="7a388-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7a388-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7a388-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7a388-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7a388-122">DLL</span><span class="sxs-lookup"><span data-stu-id="7a388-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a388-123"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a388-123"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a388-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7a388-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a388-125">**SdbCreateDatabase**</span><span class="sxs-lookup"><span data-stu-id="7a388-125">**SdbCreateDatabase**</span></span>](sdbcreatedatabase.md)
</dt> </dl>

 

 




