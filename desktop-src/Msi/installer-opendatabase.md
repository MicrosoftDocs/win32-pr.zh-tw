---
description: 安裝程式物件的 OpenDatabase 方法會開啟現有的資料庫，或建立一個新的資料庫，並傳回資料庫物件。 如果無法成功建立和開啟資料庫物件，它就會產生錯誤。
ms.assetid: a77b3954-db27-41a0-8f8b-2654766bde6a
title: OpenDatabase 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.OpenDatabase
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 897e683fd56ce3e7496dd945ee068a9e6f0c0f77
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2021
ms.locfileid: "107492267"
---
# <a name="installeropendatabase-method"></a><span data-ttu-id="3c012-104">OpenDatabase 方法</span><span class="sxs-lookup"><span data-stu-id="3c012-104">Installer.OpenDatabase method</span></span>

<span data-ttu-id="3c012-105">[**安裝程式**](installer-object.md)物件的 **OpenDatabase** 方法會開啟現有的資料庫，或建立一個新的資料庫，並傳回 [**資料庫**](database-object.md)物件。</span><span class="sxs-lookup"><span data-stu-id="3c012-105">The **OpenDatabase** method of the [**Installer**](installer-object.md) object opens an existing database or creates a new one, returning a [**Database**](database-object.md) object.</span></span> <span data-ttu-id="3c012-106">如果無法成功建立和開啟 **資料庫** 物件，它就會產生錯誤。</span><span class="sxs-lookup"><span data-stu-id="3c012-106">It generates an error if the **Database** object cannot be successfully created and opened.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c012-107">語法</span><span class="sxs-lookup"><span data-stu-id="3c012-107">Syntax</span></span>


```JScript
Installer.OpenDatabase(
  name,
  openMode
)
```



## <a name="parameters"></a><span data-ttu-id="3c012-108">參數</span><span class="sxs-lookup"><span data-stu-id="3c012-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c012-109">*name*</span><span class="sxs-lookup"><span data-stu-id="3c012-109">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="3c012-110">必要的字串，其中包含資料庫的路徑名稱。</span><span class="sxs-lookup"><span data-stu-id="3c012-110">Required string that contains the path name of the database.</span></span> <span data-ttu-id="3c012-111">如果提供空字串，則會建立不會保存的暫存資料庫。</span><span class="sxs-lookup"><span data-stu-id="3c012-111">If an empty string is supplied, a temporary database is created that is not persisted.</span></span>

</dd> <dt>

<span data-ttu-id="3c012-112">*openMode*</span><span class="sxs-lookup"><span data-stu-id="3c012-112">*openMode*</span></span> 
</dt> <dd>

<span data-ttu-id="3c012-113">下列清單中的參數，或字串，其中包含要在認可時寫入之新輸出資料庫檔案的路徑名稱。</span><span class="sxs-lookup"><span data-stu-id="3c012-113">A parameter from the following list or a string that contains the path name of the new output database file that is to be written to upon commit.</span></span>



| <span data-ttu-id="3c012-114">參數</span><span class="sxs-lookup"><span data-stu-id="3c012-114">Parameter</span></span>                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="3c012-115">意義</span><span class="sxs-lookup"><span data-stu-id="3c012-115">Meaning</span></span>                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiOpenDatabaseModeReadOnly"></span><span id="msiopendatabasemodereadonly"></span><span id="MSIOPENDATABASEMODEREADONLY"></span><dl> <span data-ttu-id="3c012-116"><dt>**msiOpenDatabaseModeReadOnly**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3c012-116"><dt>**msiOpenDatabaseModeReadOnly**</dt> <dt>0</dt></span></span> </dl>                 | <span data-ttu-id="3c012-117">開啟資料庫唯讀，無持續性變更。</span><span class="sxs-lookup"><span data-stu-id="3c012-117">Opens a database read-only, no persistent changes.</span></span><br/>                                                                                                           |
| <span id="msiOpenDatabaseModeTransact"></span><span id="msiopendatabasemodetransact"></span><span id="MSIOPENDATABASEMODETRANSACT"></span><dl> <span data-ttu-id="3c012-118"><dt>**msiOpenDatabaseModeTransact**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="3c012-118"><dt>**msiOpenDatabaseModeTransact**</dt> <dt>1</dt></span></span> </dl>                 | <span data-ttu-id="3c012-119">在交易模式中開啟資料庫的讀取/寫入。</span><span class="sxs-lookup"><span data-stu-id="3c012-119">Opens a database read/write in transaction mode.</span></span><br/>                                                                                                             |
| <span id="msiOpenDatabaseModeDirect"></span><span id="msiopendatabasemodedirect"></span><span id="MSIOPENDATABASEMODEDIRECT"></span><dl> <span data-ttu-id="3c012-120"><dt>**msiOpenDatabaseModeDirect**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3c012-120"><dt>**msiOpenDatabaseModeDirect**</dt> <dt>2</dt></span></span> </dl>                         | <span data-ttu-id="3c012-121">開啟無交易的資料庫直接讀取/寫入。</span><span class="sxs-lookup"><span data-stu-id="3c012-121">Opens a database direct read/write without transaction.</span></span><br/>                                                                                                      |
| <span id="msiOpenDatabaseModeCreate"></span><span id="msiopendatabasemodecreate"></span><span id="MSIOPENDATABASEMODECREATE"></span><dl> <span data-ttu-id="3c012-122"><dt>**msiOpenDatabaseModeCreate**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="3c012-122"><dt>**msiOpenDatabaseModeCreate**</dt> <dt>3</dt></span></span> </dl>                         | <span data-ttu-id="3c012-123">建立新的資料庫（交易模式讀取/寫入）。</span><span class="sxs-lookup"><span data-stu-id="3c012-123">Creates a new database, transact mode read/write.</span></span><br/>                                                                                                            |
| <span id="msiOpenDatabaseModeCreateDirect"></span><span id="msiopendatabasemodecreatedirect"></span><span id="MSIOPENDATABASEMODECREATEDIRECT"></span><dl> <span data-ttu-id="3c012-124"><dt>**msiOpenDatabaseModeCreateDirect**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="3c012-124"><dt>**msiOpenDatabaseModeCreateDirect**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="3c012-125">建立新的資料庫，直接模式讀取/寫入。</span><span class="sxs-lookup"><span data-stu-id="3c012-125">Creates a new database, direct mode read/write.</span></span><br/>                                                                                                              |
| <span id="msiOpenDatabaseModeListScript"></span><span id="msiopendatabasemodelistscript"></span><span id="MSIOPENDATABASEMODELISTSCRIPT"></span><dl> <span data-ttu-id="3c012-126"><dt>**msiOpenDatabaseModeListScript**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="3c012-126"><dt>**msiOpenDatabaseModeListScript**</dt> <dt>5</dt></span></span> </dl>         | <span data-ttu-id="3c012-127">開啟資料庫以查看公告腳本檔，例如 [**CreateAdvertiseScript**](installer-createadvertisescript.md) 方法所產生的檔案。</span><span class="sxs-lookup"><span data-stu-id="3c012-127">Opens a database to view advertise script files, such as the files generated by the [**CreateAdvertiseScript**](installer-createadvertisescript.md) method.</span></span><br/> |
| <span id="msiOpenDatabaseModePatchFile"></span><span id="msiopendatabasemodepatchfile"></span><span id="MSIOPENDATABASEMODEPATCHFILE"></span><dl> <span data-ttu-id="3c012-128"><dt>**msiOpenDatabaseModePatchFile**</dt> <dt>32</dt></span><span class="sxs-lookup"><span data-stu-id="3c012-128"><dt>**msiOpenDatabaseModePatchFile**</dt> <dt>32</dt></span></span> </dl>            | <span data-ttu-id="3c012-129">新增此旗標以表示修補檔案。</span><span class="sxs-lookup"><span data-stu-id="3c012-129">Adds this flag to indicate a patch file.</span></span><br/>                                                                                                                     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c012-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="3c012-130">Return value</span></span>

<span data-ttu-id="3c012-131">代表已開啟之現有或新安裝程式資料庫的 [**資料庫**](database-object.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="3c012-131">A [**Database**](database-object.md) object that represents the existing or new installer database that was opened.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c012-132">備註</span><span class="sxs-lookup"><span data-stu-id="3c012-132">Remarks</span></span>

<span data-ttu-id="3c012-133">當資料庫開啟為另一個資料庫的輸出時，輸出資料庫的摘要資訊資料流程實際上是原始資料庫的唯讀鏡像，因此無法變更。</span><span class="sxs-lookup"><span data-stu-id="3c012-133">When a database is opened as the output of another database, the summary information stream of the output database is actually a read-only mirror of the original database and thus cannot be changed.</span></span> <span data-ttu-id="3c012-134">此外，它也不會與資料庫一起保存。</span><span class="sxs-lookup"><span data-stu-id="3c012-134">Additionally, it is not persisted with the database.</span></span> <span data-ttu-id="3c012-135">若要建立或修改輸出資料庫的摘要資訊，必須將其關閉並重新開啟。</span><span class="sxs-lookup"><span data-stu-id="3c012-135">To create or modify the summary information for the output database it must be closed and reopened.</span></span>

<span data-ttu-id="3c012-136">若要進行並儲存資料庫的變更，請先在交易 (msiOpenDatabaseModeTransact) 中開啟資料庫，並建立 (msiOpenDatabaseModeCreate 或 msiOpenDatabaseModeCreateDirect) ，或直接 (msiOpenDatabaseModeDirect) 模式。</span><span class="sxs-lookup"><span data-stu-id="3c012-136">To make and save changes to a database first open the database in transaction (msiOpenDatabaseModeTransact), create (msiOpenDatabaseModeCreate or msiOpenDatabaseModeCreateDirect), or direct (msiOpenDatabaseModeDirect) mode.</span></span> <span data-ttu-id="3c012-137">進行變更之後，請一律在關閉資料庫控制碼之前呼叫 [**Commit**](database-commit.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="3c012-137">After making the changes, always call the [**Commit**](database-commit.md) method before closing the database handle.</span></span> <span data-ttu-id="3c012-138">**Commit** 方法會清空所有緩衝區。</span><span class="sxs-lookup"><span data-stu-id="3c012-138">The **Commit** method flushes all buffers.</span></span>

<span data-ttu-id="3c012-139">請一律在關閉資料庫之前 (msiOpenDatabaseModeDirect 或 msiOpenDatabaseModeCreateDirect) 在直接模式中開啟的資料庫上，呼叫 [**Commit**](database-commit.md) 方法或。</span><span class="sxs-lookup"><span data-stu-id="3c012-139">Always call the [**Commit**](database-commit.md) method on a database that has been opened in direct mode (msiOpenDatabaseModeDirect or msiOpenDatabaseModeCreateDirect) before closing the database.</span></span> <span data-ttu-id="3c012-140">若無法這樣做，可能會損毀資料庫。</span><span class="sxs-lookup"><span data-stu-id="3c012-140">Failure to do this may corrupt the database.</span></span>

<span data-ttu-id="3c012-141">由於 **OpenDatabase** 方法會起始資料庫存取，因此不能與執行中的安裝一起使用。</span><span class="sxs-lookup"><span data-stu-id="3c012-141">Because the **OpenDatabase** method initiates database access, it cannot be used with a running installation.</span></span>

<span data-ttu-id="3c012-142">如果方法失敗，您可以使用 [**LastErrorRecord**](installer-lasterrorrecord.md) 方法來取得擴充的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="3c012-142">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c012-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c012-143">Requirements</span></span>



| <span data-ttu-id="3c012-144">需求</span><span class="sxs-lookup"><span data-stu-id="3c012-144">Requirement</span></span> | <span data-ttu-id="3c012-145">值</span><span class="sxs-lookup"><span data-stu-id="3c012-145">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c012-146">版本</span><span class="sxs-lookup"><span data-stu-id="3c012-146">Version</span></span><br/> | <span data-ttu-id="3c012-147">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="3c012-147">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3c012-148">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="3c012-148">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3c012-149">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="3c012-149">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="3c012-150">DLL</span><span class="sxs-lookup"><span data-stu-id="3c012-150">DLL</span></span><br/>     | <dl> <span data-ttu-id="3c012-151"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c012-151"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="3c012-152">IID</span><span class="sxs-lookup"><span data-stu-id="3c012-152">IID</span></span><br/>     | <span data-ttu-id="3c012-153">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="3c012-153">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




