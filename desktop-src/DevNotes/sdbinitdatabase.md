---
description: 開啟填充碼資料庫。
ms.assetid: ece1bd39-20a1-42e6-8e2b-1d38f7223d42
title: SdbInitDatabase 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbInitDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 7a3c63fa712aec988dbf13c4fb7f9fddbf159fdd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468033"
---
# <a name="sdbinitdatabase-function"></a><span data-ttu-id="29ea3-103">SdbInitDatabase 函式</span><span class="sxs-lookup"><span data-stu-id="29ea3-103">SdbInitDatabase function</span></span>

<span data-ttu-id="29ea3-104">開啟填充碼資料庫。</span><span class="sxs-lookup"><span data-stu-id="29ea3-104">Opens the shim database.</span></span>

## <a name="syntax"></a><span data-ttu-id="29ea3-105">語法</span><span class="sxs-lookup"><span data-stu-id="29ea3-105">Syntax</span></span>


```C++
HSDB WINAPI SdbInitDatabase(
  _In_ DWORD   dwFlags,
  _In_ LPCTSTR pszDatabasePath
);
```



## <a name="parameters"></a><span data-ttu-id="29ea3-106">參數</span><span class="sxs-lookup"><span data-stu-id="29ea3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29ea3-107">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="29ea3-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29ea3-108">此參數會在 *pszDatabasePath* 參數中指定路徑的格式。</span><span class="sxs-lookup"><span data-stu-id="29ea3-108">This parameter specifies the format of the path in the *pszDatabasePath* parameter.</span></span> <span data-ttu-id="29ea3-109">它可以是下列值之一。</span><span class="sxs-lookup"><span data-stu-id="29ea3-109">It can be one of the following values.</span></span>



| <span data-ttu-id="29ea3-110">值</span><span class="sxs-lookup"><span data-stu-id="29ea3-110">Value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="29ea3-111">意義</span><span class="sxs-lookup"><span data-stu-id="29ea3-111">Meaning</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span id="HID_DOS_PATHS"></span><span id="hid_dos_paths"></span><dl> <span data-ttu-id="29ea3-112"><dt>**HID \_DOS \_ 路徑**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="29ea3-112"><dt>**HID\_DOS\_PATHS**</dt> <dt>0x00000001</dt></span></span> </dl>                             | <span data-ttu-id="29ea3-113">MS-DOS 樣式路徑。</span><span class="sxs-lookup"><span data-stu-id="29ea3-113">An MS-DOS style path.</span></span><br/>                                                                       |
| <span id="HID_DATABASE_FULLPATH"></span><span id="hid_database_fullpath"></span><dl> <span data-ttu-id="29ea3-114"><dt>**HID \_資料庫 \_ FULLPATH**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="29ea3-114"><dt>**HID\_DATABASE\_FULLPATH**</dt> <dt>0x00000002</dt></span></span> </dl>     | <span data-ttu-id="29ea3-115">完整路徑。</span><span class="sxs-lookup"><span data-stu-id="29ea3-115">A full path.</span></span><br/>                                                                                |
| <span id="HID_NO_DATABASE"></span><span id="hid_no_database"></span><dl> <span data-ttu-id="29ea3-116"><dt>**HID \_無 \_ 資料庫**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="29ea3-116"><dt>**HID\_NO\_DATABASE**</dt> <dt>0x00000004</dt></span></span> </dl>                       | <span data-ttu-id="29ea3-117">*PszDatabasePath* 參數會被忽略，且不會開啟任何資料庫。</span><span class="sxs-lookup"><span data-stu-id="29ea3-117">The *pszDatabasePath* parameter is ignored and no database is opened.</span></span><br/>                       |
| <span id="HID_DATABASE_TYPE_MASK"></span><span id="hid_database_type_mask"></span><dl> <span data-ttu-id="29ea3-118"><dt>**HID \_資料庫 \_ 類型 \_ 遮罩**</dt> <dt>0xF00F0000</dt></span><span class="sxs-lookup"><span data-stu-id="29ea3-118"><dt>**HID\_DATABASE\_TYPE\_MASK**</dt> <dt>0xF00F0000</dt></span></span> </dl> | <span data-ttu-id="29ea3-119">此參數會指定預先定義的資料庫。</span><span class="sxs-lookup"><span data-stu-id="29ea3-119">This parameter specifies a predefined database.</span></span> <span data-ttu-id="29ea3-120">*PszDatabasePath* 參數會被忽略。</span><span class="sxs-lookup"><span data-stu-id="29ea3-120">The *pszDatabasePath* parameter is ignored.</span></span><br/> |



 

<span data-ttu-id="29ea3-121">如果 *dwFlags* 包含 **隱藏的 \_ 資料 \_ 類型 \_ 遮罩**，此參數也可以包含下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="29ea3-121">If *dwFlags* contains **HID\_DATA\_TYPE\_MASK**, this parameter can also include one of the following values.</span></span>



| <span data-ttu-id="29ea3-122">值</span><span class="sxs-lookup"><span data-stu-id="29ea3-122">Value</span></span>                                                                                                                                                                                                                                                               | <span data-ttu-id="29ea3-123">意義</span><span class="sxs-lookup"><span data-stu-id="29ea3-123">Meaning</span></span>                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="SDB_DATABASE_MAIN_SHIM"></span><span id="sdb_database_main_shim"></span><dl> <span data-ttu-id="29ea3-124"><dt>**SDB \_資料庫 \_ 主要 \_ 填充碼**</dt> <dt>0x80030000</dt></span><span class="sxs-lookup"><span data-stu-id="29ea3-124"><dt>**SDB\_DATABASE\_MAIN\_SHIM**</dt> <dt>0x80030000</dt></span></span> </dl>          | <span data-ttu-id="29ea3-125">應用程式填充碼資料庫。</span><span class="sxs-lookup"><span data-stu-id="29ea3-125">Application shim database.</span></span><br/>         |
| <span id="SDB_DATABASE_MAIN_MSI"></span><span id="sdb_database_main_msi"></span><dl> <span data-ttu-id="29ea3-126"><dt>**SDB \_資料庫 \_ 主要 \_ MSI**</dt> <dt>0x80020000</dt></span><span class="sxs-lookup"><span data-stu-id="29ea3-126"><dt>**SDB\_DATABASE\_MAIN\_MSI**</dt> <dt>0x80020000</dt></span></span> </dl>             | <span data-ttu-id="29ea3-127">MSI 資料庫。</span><span class="sxs-lookup"><span data-stu-id="29ea3-127">MSI database.</span></span><br/>                      |
| <span id="SDB_DATABASE_MAIN_DRIVERS"></span><span id="sdb_database_main_drivers"></span><dl> <span data-ttu-id="29ea3-128"><dt>**SDB \_資料庫 \_ 主要 \_ 驅動程式**</dt> <dt>0x80040000</dt></span><span class="sxs-lookup"><span data-stu-id="29ea3-128"><dt>**SDB\_DATABASE\_MAIN\_DRIVERS**</dt> <dt>0x80040000</dt></span></span> </dl> | <span data-ttu-id="29ea3-129">要封鎖之驅動程式的資料庫。</span><span class="sxs-lookup"><span data-stu-id="29ea3-129">Database of drivers to be blocked.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="29ea3-130">*pszDatabasePath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="29ea3-130">*pszDatabasePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29ea3-131">資料庫的路徑。</span><span class="sxs-lookup"><span data-stu-id="29ea3-131">The path to the database.</span></span> <span data-ttu-id="29ea3-132">如果 *dwFlags* 參數指定預先定義的資料庫，則此參數可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="29ea3-132">This parameter can be **NULL** if the *dwFlags* parameter specifies a predefined database.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29ea3-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="29ea3-133">Return value</span></span>

<span data-ttu-id="29ea3-134">函數會傳回已開啟資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="29ea3-134">The function returns a handle to the opened database.</span></span>

## <a name="requirements"></a><span data-ttu-id="29ea3-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="29ea3-135">Requirements</span></span>



| <span data-ttu-id="29ea3-136">需求</span><span class="sxs-lookup"><span data-stu-id="29ea3-136">Requirement</span></span> | <span data-ttu-id="29ea3-137">值</span><span class="sxs-lookup"><span data-stu-id="29ea3-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="29ea3-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="29ea3-138">Minimum supported client</span></span><br/> | <span data-ttu-id="29ea3-139">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="29ea3-139">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="29ea3-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="29ea3-140">Minimum supported server</span></span><br/> | <span data-ttu-id="29ea3-141">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="29ea3-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="29ea3-142">DLL</span><span class="sxs-lookup"><span data-stu-id="29ea3-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29ea3-143"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29ea3-143"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29ea3-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="29ea3-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29ea3-145">**SdbGetAppPatchDir**</span><span class="sxs-lookup"><span data-stu-id="29ea3-145">**SdbGetAppPatchDir**</span></span>](sdbgetapppatchdir.md)
</dt> <dt>

[<span data-ttu-id="29ea3-146">**SdbGetMatchingExe**</span><span class="sxs-lookup"><span data-stu-id="29ea3-146">**SdbGetMatchingExe**</span></span>](sdbgetmatchingexe.md)
</dt> <dt>

[<span data-ttu-id="29ea3-147">**SdbReleaseMatchingExe**</span><span class="sxs-lookup"><span data-stu-id="29ea3-147">**SdbReleaseMatchingExe**</span></span>](sdbreleasematchingexe.md)
</dt> <dt>

[<span data-ttu-id="29ea3-148">**SdbTagRefToTagID**</span><span class="sxs-lookup"><span data-stu-id="29ea3-148">**SdbTagRefToTagID**</span></span>](sdbtagreftotagid.md)
</dt> </dl>

 

 




