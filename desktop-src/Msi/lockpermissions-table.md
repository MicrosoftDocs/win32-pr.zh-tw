---
description: 用來在鎖定的環境中保護應用程式的個別部分。 它可用於安裝檔案、登錄機碼和建立的資料夾。
ms.assetid: 7c20e211-7704-49c2-a0c5-aaa695a09764
title: LockPermissions 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c07402b80caec7beff68083567f2ff2fb9bf5eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992453"
---
# <a name="lockpermissions-table"></a><span data-ttu-id="eea32-104">LockPermissions 資料表</span><span class="sxs-lookup"><span data-stu-id="eea32-104">LockPermissions Table</span></span>

<span data-ttu-id="eea32-105">LockPermissions 資料表是用來保護鎖定環境中應用程式的個別部分。</span><span class="sxs-lookup"><span data-stu-id="eea32-105">The LockPermissions Table is used to secure individual portions of an application in a locked-down environment.</span></span> <span data-ttu-id="eea32-106">它可用於安裝檔案、登錄機碼和建立的資料夾。</span><span class="sxs-lookup"><span data-stu-id="eea32-106">It can be used with the installation of files, registry keys, and created folders.</span></span>

<span data-ttu-id="eea32-107">適用于在 Windows Server 2008 R2 或 Windows 7 安裝的套件應該使用 [MsiLockPermissionsEx 資料表](msilockpermissionsex-table.md) ，而不是 LockPermissions 資料表。</span><span class="sxs-lookup"><span data-stu-id="eea32-107">A package intended for installation in Windows Server 2008 R2 or Windows 7 should use the [MsiLockPermissionsEx Table](msilockpermissionsex-table.md) rather than the LockPermissions Table.</span></span> <span data-ttu-id="eea32-108">Windows Installer Windows Installer 5.0 之前的版本會忽略 MsiLockPermissionsEx 資料表。</span><span class="sxs-lookup"><span data-stu-id="eea32-108">Windows Installer versions earlier than Windows Installer 5.0 ignore the MsiLockPermissionsEx Table.</span></span> <span data-ttu-id="eea32-109">Windows Installer 5.0 可以安裝包含 LockPermissions 資料表的封裝。</span><span class="sxs-lookup"><span data-stu-id="eea32-109">Windows Installer 5.0 can install an package that contains the LockPermissions Table.</span></span> <span data-ttu-id="eea32-110">從 Windows Installer 5.0 開始，安裝包含 MsiLockPermissionsEx 資料表和 LockPermissions 資料表的封裝會失敗，並傳回 Windows Installer 錯誤訊息1941。</span><span class="sxs-lookup"><span data-stu-id="eea32-110">Beginning with Windows Installer 5.0, installation of a package that contains both the MsiLockPermissionsEx Table and the LockPermissions Table fails and returns Windows Installer error message 1941.</span></span>

<span data-ttu-id="eea32-111">LockPermissions 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="eea32-111">The LockPermissions Table has the following columns.</span></span>



| <span data-ttu-id="eea32-112">Column</span><span class="sxs-lookup"><span data-stu-id="eea32-112">Column</span></span>     | <span data-ttu-id="eea32-113">類型</span><span class="sxs-lookup"><span data-stu-id="eea32-113">Type</span></span>                               | <span data-ttu-id="eea32-114">答案</span><span class="sxs-lookup"><span data-stu-id="eea32-114">Key</span></span> | <span data-ttu-id="eea32-115">Nullable</span><span class="sxs-lookup"><span data-stu-id="eea32-115">Nullable</span></span> |
|------------|------------------------------------|-----|----------|
| <span data-ttu-id="eea32-116">LockObject</span><span class="sxs-lookup"><span data-stu-id="eea32-116">LockObject</span></span> | [<span data-ttu-id="eea32-117">識別碼</span><span class="sxs-lookup"><span data-stu-id="eea32-117">Identifier</span></span>](identifier.md)       | <span data-ttu-id="eea32-118">Y</span><span class="sxs-lookup"><span data-stu-id="eea32-118">Y</span></span>   | <span data-ttu-id="eea32-119">N</span><span class="sxs-lookup"><span data-stu-id="eea32-119">N</span></span>        |
| <span data-ttu-id="eea32-120">資料表</span><span class="sxs-lookup"><span data-stu-id="eea32-120">Table</span></span>      | [<span data-ttu-id="eea32-121">Text</span><span class="sxs-lookup"><span data-stu-id="eea32-121">Text</span></span>](text.md)                   | <span data-ttu-id="eea32-122">Y</span><span class="sxs-lookup"><span data-stu-id="eea32-122">Y</span></span>   | <span data-ttu-id="eea32-123">N</span><span class="sxs-lookup"><span data-stu-id="eea32-123">N</span></span>        |
| <span data-ttu-id="eea32-124">網域</span><span class="sxs-lookup"><span data-stu-id="eea32-124">Domain</span></span>     | [<span data-ttu-id="eea32-125">格式 化</span><span class="sxs-lookup"><span data-stu-id="eea32-125">Formatted</span></span>](formatted.md)         | <span data-ttu-id="eea32-126">Y</span><span class="sxs-lookup"><span data-stu-id="eea32-126">Y</span></span>   | <span data-ttu-id="eea32-127">Y</span><span class="sxs-lookup"><span data-stu-id="eea32-127">Y</span></span>        |
| <span data-ttu-id="eea32-128">User</span><span class="sxs-lookup"><span data-stu-id="eea32-128">User</span></span>       | [<span data-ttu-id="eea32-129">格式 化</span><span class="sxs-lookup"><span data-stu-id="eea32-129">Formatted</span></span>](formatted.md)         | <span data-ttu-id="eea32-130">Y</span><span class="sxs-lookup"><span data-stu-id="eea32-130">Y</span></span>   | <span data-ttu-id="eea32-131">N</span><span class="sxs-lookup"><span data-stu-id="eea32-131">N</span></span>        |
| <span data-ttu-id="eea32-132">權限</span><span class="sxs-lookup"><span data-stu-id="eea32-132">Permission</span></span> | [<span data-ttu-id="eea32-133">DoubleInteger</span><span class="sxs-lookup"><span data-stu-id="eea32-133">DoubleInteger</span></span>](doubleinteger.md) | <span data-ttu-id="eea32-134">N</span><span class="sxs-lookup"><span data-stu-id="eea32-134">N</span></span>   | <span data-ttu-id="eea32-135">Y</span><span class="sxs-lookup"><span data-stu-id="eea32-135">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="eea32-136">資料行</span><span class="sxs-lookup"><span data-stu-id="eea32-136">Columns</span></span>

<dl> <dt>

<span data-ttu-id="eea32-137"><span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject</span><span class="sxs-lookup"><span data-stu-id="eea32-137"><span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject</span></span>
</dt> <dd>

<span data-ttu-id="eea32-138">這個資料行和資料表資料行會指定要保護的檔案、目錄或登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="eea32-138">This column and the Table column together specify the file, directory, or registry key that is to be secured.</span></span> <span data-ttu-id="eea32-139">LockObject 資料行是一個外鍵，指向資料表資料行所指定之資料表的主鍵。</span><span class="sxs-lookup"><span data-stu-id="eea32-139">The LockObject column is a foreign key that points to the primary key of the table specified by the Table column.</span></span>

</dd> <dt>

<span data-ttu-id="eea32-140"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>表</span><span class="sxs-lookup"><span data-stu-id="eea32-140"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="eea32-141">這個資料行和 LockObject 資料行指定要保護的檔案、目錄或登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="eea32-141">This column and the LockObject column specify the file, directory, or registry key that is to be secured.</span></span> <span data-ttu-id="eea32-142">在 [資料表] 資料行中，輸入 File、Registry 或 CreateFolder，以指定檔案 [資料表](file-table.md)、登錄 [表](registry-table.md)或 [CreateFolder 資料表](createfolder-table.md)中所列的 LockObject。</span><span class="sxs-lookup"><span data-stu-id="eea32-142">In the Table column, enter File, Registry, or CreateFolder to specify a LockObject listed in the [File Table](file-table.md), [Registry Table](registry-table.md), or [CreateFolder Table](createfolder-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="eea32-143"><span id="Domain"></span><span id="domain"></span><span id="DOMAIN"></span>域</span><span class="sxs-lookup"><span data-stu-id="eea32-143"><span id="Domain"></span><span id="domain"></span><span id="DOMAIN"></span>Domain</span></span>
</dt> <dd>

<span data-ttu-id="eea32-144">識別要設定許可權之使用者網域的資料行。</span><span class="sxs-lookup"><span data-stu-id="eea32-144">The column that identifies the domain of the user for which permissions are to be set.</span></span> <span data-ttu-id="eea32-145">這是獨立電腦或功能變數名稱的名稱。</span><span class="sxs-lookup"><span data-stu-id="eea32-145">This is the name of a stand-alone machine or a domain name.</span></span> <span data-ttu-id="eea32-146">資料行資料類型已 [格式化](formatted.md)，您可以 \[ \] 在此欄位中使用字串% USERDOMAIN 來取得目前網域的 USERDOMAIN 環境變數值。</span><span class="sxs-lookup"><span data-stu-id="eea32-146">The column data type is [Formatted](formatted.md), and you may use the string \[%USERDOMAIN\] in this field to get the value of the USERDOMAIN environment variable for the current domain.</span></span> <span data-ttu-id="eea32-147">若要取得任何其他網域，則需要使用 [自訂動作](custom-actions.md)。</span><span class="sxs-lookup"><span data-stu-id="eea32-147">To get any other domain requires using [Custom Actions](custom-actions.md).</span></span> <span data-ttu-id="eea32-148">如需詳細資訊，請參閱自訂動作表。</span><span class="sxs-lookup"><span data-stu-id="eea32-148">For more information, see the Custom Action Table.</span></span>

</dd> <dt>

<span data-ttu-id="eea32-149"><span id="User"></span><span id="user"></span><span id="USER"></span>使用者</span><span class="sxs-lookup"><span data-stu-id="eea32-149"><span id="User"></span><span id="user"></span><span id="USER"></span>User</span></span>
</dt> <dd>

<span data-ttu-id="eea32-150">識別要設定許可權之使用者的當地語系化名稱的資料行。</span><span class="sxs-lookup"><span data-stu-id="eea32-150">The column that identifies the localized name of the user for which permissions are to be set.</span></span> <span data-ttu-id="eea32-151">此名稱必須位於電腦或網域上。</span><span class="sxs-lookup"><span data-stu-id="eea32-151">This name must be located on the machine or domain.</span></span> <span data-ttu-id="eea32-152">如果電腦或網域控制站無法辨識網域和使用者組合，或無法抓取 (SID) 使用者的安全識別碼，則安裝會失敗。</span><span class="sxs-lookup"><span data-stu-id="eea32-152">The installation fails if the machine or domain controller does not recognize the domain and user combination or if the user's security identifier (SID) cannot be retrieved.</span></span> <span data-ttu-id="eea32-153">可以為單一 LockObject 指定多個使用者。</span><span class="sxs-lookup"><span data-stu-id="eea32-153">Multiple users can be specified for a single LockObject.</span></span>

<span data-ttu-id="eea32-154">一般使用者名稱「Everyone」和「系統管理員」可能會以英文輸入，並對應到知名的 Sid。</span><span class="sxs-lookup"><span data-stu-id="eea32-154">The common user names "Everyone" and "Administrators" may be entered in English and are mapped to well-known SIDs.</span></span> <span data-ttu-id="eea32-155">LocalSystem 在透過 LockPermissions 資料表所建立的所有安全描述項中，都具有完整控制權。</span><span class="sxs-lookup"><span data-stu-id="eea32-155">LocalSystem is given full control in all security descriptors created through the LockPermissions Table.</span></span> <span data-ttu-id="eea32-156">您可以使用此欄位中的 [ [**ComputerName] 屬性**](computername.md)、[ [**LogonUser] 屬性**](logonuser.md) 或 [使用者名稱] [**屬性**](username.md) 來取得目前的使用者。</span><span class="sxs-lookup"><span data-stu-id="eea32-156">You can use the [**ComputerName Property**](computername.md), [**LogonUser Property**](logonuser.md) or [**USERNAME Property**](username.md) in this field to get the current user.</span></span> <span data-ttu-id="eea32-157">需要自訂動作，才能輸入任何其他使用者或群組的當地語系化名稱。</span><span class="sxs-lookup"><span data-stu-id="eea32-157">A custom action is required to enter the localized name of any other user or group.</span></span>

<span data-ttu-id="eea32-158">您可以使用具有相同 LockObject 和資料表專案的多筆記錄 (但) 不同的使用者專案，以指定多個使用者的存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="eea32-158">You can use multiple records with identical LockObject and Table entries (but different User entries) to specify access control lists for multiple users.</span></span>

</dd> <dt>

<span data-ttu-id="eea32-159"><span id="Permission"></span><span id="permission"></span><span id="PERMISSION"></span>許可</span><span class="sxs-lookup"><span data-stu-id="eea32-159"><span id="Permission"></span><span id="permission"></span><span id="PERMISSION"></span>Permission</span></span>
</dt> <dd>

<span data-ttu-id="eea32-160">識別系統許可權之整數描述的資料行。</span><span class="sxs-lookup"><span data-stu-id="eea32-160">The column that identifies the integer description of system privileges.</span></span> <span data-ttu-id="eea32-161">以下提供最常使用的值 (在 Winnt. h) 中有完整清單。</span><span class="sxs-lookup"><span data-stu-id="eea32-161">The following gives the most commonly used values (a complete list exists in Winnt.h).</span></span>



| <span data-ttu-id="eea32-162">Privilege</span><span class="sxs-lookup"><span data-stu-id="eea32-162">Privilege</span></span>                                                              | <span data-ttu-id="eea32-163">Description</span><span class="sxs-lookup"><span data-stu-id="eea32-163">Description</span></span>                     |
|------------------------------------------------------------------------|---------------------------------|
| <span data-ttu-id="eea32-164">一般 \_ 全部</span><span class="sxs-lookup"><span data-stu-id="eea32-164">GENERIC\_ALL</span></span><br/> <span data-ttu-id="eea32-165">0X10000000</span><span class="sxs-lookup"><span data-stu-id="eea32-165">0X10000000</span></span><br/> <span data-ttu-id="eea32-166">268435456</span><span class="sxs-lookup"><span data-stu-id="eea32-166">268435456</span></span><br/>     | <span data-ttu-id="eea32-167">讀取、寫入和執行存取權</span><span class="sxs-lookup"><span data-stu-id="eea32-167">Read, write, and execute access</span></span> |
| <span data-ttu-id="eea32-168">一般 \_ 執行</span><span class="sxs-lookup"><span data-stu-id="eea32-168">GENERIC\_EXECUTE</span></span><br/> <span data-ttu-id="eea32-169">0X20000000</span><span class="sxs-lookup"><span data-stu-id="eea32-169">0X20000000</span></span><br/> <span data-ttu-id="eea32-170">536870912</span><span class="sxs-lookup"><span data-stu-id="eea32-170">536870912</span></span><br/> | <span data-ttu-id="eea32-171">執行存取</span><span class="sxs-lookup"><span data-stu-id="eea32-171">Execute access</span></span>                  |
| <span data-ttu-id="eea32-172">一般 \_ 寫入</span><span class="sxs-lookup"><span data-stu-id="eea32-172">GENERIC\_WRITE</span></span><br/> <span data-ttu-id="eea32-173">0X40000000</span><span class="sxs-lookup"><span data-stu-id="eea32-173">0X40000000</span></span><br/> <span data-ttu-id="eea32-174">1073741824</span><span class="sxs-lookup"><span data-stu-id="eea32-174">1073741824</span></span><br/>  | <span data-ttu-id="eea32-175">寫入存取權</span><span class="sxs-lookup"><span data-stu-id="eea32-175">Write access</span></span>                    |



 

<span data-ttu-id="eea32-176">您無法 \_ 在許可權資料行中指定泛型 READ。</span><span class="sxs-lookup"><span data-stu-id="eea32-176">You cannot specify GENERIC\_READ in the Permission column.</span></span> <span data-ttu-id="eea32-177">嘗試這麼做將會失敗。</span><span class="sxs-lookup"><span data-stu-id="eea32-177">Attempting to do so will fail.</span></span> <span data-ttu-id="eea32-178">相反地，您必須指定一個值，例如讀取金鑰 \_ 或 \_ 讀取檔案一般 \_ 。</span><span class="sxs-lookup"><span data-stu-id="eea32-178">Instead, you must specify a value such as KEY\_READ or FILE\_GENERIC\_READ.</span></span>

<span data-ttu-id="eea32-179">在此資料行中輸入的 Null 已保留供日後使用。</span><span class="sxs-lookup"><span data-stu-id="eea32-179">Null entered in this column is reserved for future use.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eea32-180">備註</span><span class="sxs-lookup"><span data-stu-id="eea32-180">Remarks</span></span>

<span data-ttu-id="eea32-181">[*順序資料表*](s-gly.md)中的 [InstallFiles](installfiles-action.md)、 [WriteRegistryValues](writeregistryvalues-action.md)和 [CreateFolders](createfolders-action.md)動作會處理此資料表中的資訊。</span><span class="sxs-lookup"><span data-stu-id="eea32-181">The [InstallFiles](installfiles-action.md), [WriteRegistryValues](writeregistryvalues-action.md), and [CreateFolders](createfolders-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="eea32-182">如需使用 *順序資料表* 的詳細資訊，請參閱 [使用順序資料表](using-a-sequence-table.md)。</span><span class="sxs-lookup"><span data-stu-id="eea32-182">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

<span data-ttu-id="eea32-183">只有在已經存在於電腦或網域上的使用者，才能在 LockPermissions 資料表中設定許可權。</span><span class="sxs-lookup"><span data-stu-id="eea32-183">Permission can only be set in the LockPermissions Table for users that already exist on the computer or domain.</span></span> <span data-ttu-id="eea32-184">嘗試設定未知使用者的許可權，會導致安裝失敗，即使該使用者帳戶是在安裝期間由延遲的自訂動作所建立。</span><span class="sxs-lookup"><span data-stu-id="eea32-184">An attempt to set permissions for an unknown user causes the installation to fail, even if that user account is created during the installation by a deferred custom action.</span></span>

<span data-ttu-id="eea32-185">建議將系統管理員的本機群組包含在 (ACL) 的所有存取控制清單中。</span><span class="sxs-lookup"><span data-stu-id="eea32-185">It is recommended that the system administrator's local group be included in all access control lists (ACL).</span></span> <span data-ttu-id="eea32-186">這可確保系統管理員可以存取和維護物件。</span><span class="sxs-lookup"><span data-stu-id="eea32-186">This ensures that the system administrator can access and maintain objects.</span></span>

<span data-ttu-id="eea32-187">LockPermissions 資料表中所列的每個檔案、登錄機碼或目錄都會收到明確的安全描述項（不論是否取代現有的物件）。</span><span class="sxs-lookup"><span data-stu-id="eea32-187">Every file, registry key, or directory that is listed in the LockPermissions Table receives an explicit security descriptor, whether it replaces an existing object or not.</span></span> <span data-ttu-id="eea32-188">Windows Installer 會嘗試在已經存在於系統上的物件上保留安全性。</span><span class="sxs-lookup"><span data-stu-id="eea32-188">The Windows Installer attempts to preserve the security on objects that already exist on the system.</span></span> <span data-ttu-id="eea32-189">如果物件未列在 LockPermissions 資料表中，並取代現有的物件，則取代會取得它所取代之物件的安全性設定。</span><span class="sxs-lookup"><span data-stu-id="eea32-189">If an object is not listed in the LockPermissions Table, and replaces an existing object, the replacement gets the security settings of the object that it replaces.</span></span>

<span data-ttu-id="eea32-190">如果物件未列在 LockPermissions 資料表中，而且不會取代現有的物件，它就不會收到任何明確的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="eea32-190">If an object is not listed in the LockPermissions Table, and does not replace an existing object, it receives no explicit security descriptor.</span></span> <span data-ttu-id="eea32-191">新物件的存取是以其父系或容器物件的屬性為基礎。</span><span class="sxs-lookup"><span data-stu-id="eea32-191">The access to the new object is based on the attributes of its parent or container object.</span></span> <span data-ttu-id="eea32-192">如果物件未列在資料表中，並將物件取代為沒有明確安全描述項的物件，則會根據其父系或容器物件的屬性來存取新的物件。</span><span class="sxs-lookup"><span data-stu-id="eea32-192">If an object is not listed in the table, and replaces an object with no explicit security descriptor, the access to the new object is based on the attributes of its parent or container object.</span></span>

<span data-ttu-id="eea32-193">Windows Installer 將 [**UserSID**](usersid.md) 屬性設定為安全性識別元 (SID) 或執行安裝的使用者。</span><span class="sxs-lookup"><span data-stu-id="eea32-193">The Windows Installer sets the [**UserSID**](usersid.md) property to the security identifier (SID) or the user running the installation.</span></span>

## <a name="validation"></a><span data-ttu-id="eea32-194">驗證</span><span class="sxs-lookup"><span data-stu-id="eea32-194">Validation</span></span>

<dl>

[<span data-ttu-id="eea32-195">ICE03</span><span class="sxs-lookup"><span data-stu-id="eea32-195">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="eea32-196">ICE06</span><span class="sxs-lookup"><span data-stu-id="eea32-196">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="eea32-197">ICE46</span><span class="sxs-lookup"><span data-stu-id="eea32-197">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="eea32-198">ICE55</span><span class="sxs-lookup"><span data-stu-id="eea32-198">ICE55</span></span>](ice55.md)  
</dl>

 

 




