---
description: MsiLockPermissionsEx 資料表可以用來保護服務、檔案、登錄機碼和建立的資料夾。
ms.assetid: c642f02d-07fa-463f-8151-769c28a71a5c
title: MsiLockPermissionsEx 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63d7c63e27d7a9c390e6015eb0ebe5f663de5b4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997916"
---
# <a name="msilockpermissionsex-table"></a><span data-ttu-id="42659-103">MsiLockPermissionsEx 資料表</span><span class="sxs-lookup"><span data-stu-id="42659-103">MsiLockPermissionsEx Table</span></span>

<span data-ttu-id="42659-104">MsiLockPermissionsEx 資料表可以用來保護服務、檔案、登錄機碼和建立的資料夾。</span><span class="sxs-lookup"><span data-stu-id="42659-104">The MsiLockPermissionsEx Table can be used to secure services, files, registry keys, and created folders.</span></span>

<span data-ttu-id="42659-105">封裝不應同時包含 MsiLockPermissionsEx 資料表和 [LockPermissions 資料表](lockpermissions-table.md)。</span><span class="sxs-lookup"><span data-stu-id="42659-105">A package should not contain both the MsiLockPermissionsEx Table and the [LockPermissions Table](lockpermissions-table.md).</span></span>

<span data-ttu-id="42659-106">**[Windows Installer 4.5 或更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="42659-106">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="42659-107">針對要使用 Windows Installer 5.0 或更新版本安裝的套件，建議使用此資料表。</span><span class="sxs-lookup"><span data-stu-id="42659-107">This table is recommended for packages intended for installation with Windows Installer 5.0 or later.</span></span>

<span data-ttu-id="42659-108">MsiLockPermissionsEx 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="42659-108">The MsiLockPermissionsEx Table has the following columns.</span></span>



| <span data-ttu-id="42659-109">Column</span><span class="sxs-lookup"><span data-stu-id="42659-109">Column</span></span>               | <span data-ttu-id="42659-110">類型</span><span class="sxs-lookup"><span data-stu-id="42659-110">Type</span></span>                                       | <span data-ttu-id="42659-111">答案</span><span class="sxs-lookup"><span data-stu-id="42659-111">Key</span></span> | <span data-ttu-id="42659-112">Nullable</span><span class="sxs-lookup"><span data-stu-id="42659-112">Nullable</span></span> |
|----------------------|--------------------------------------------|-----|----------|
| <span data-ttu-id="42659-113">MsiLockPermissionsEx</span><span class="sxs-lookup"><span data-stu-id="42659-113">MsiLockPermissionsEx</span></span> | [<span data-ttu-id="42659-114">Text</span><span class="sxs-lookup"><span data-stu-id="42659-114">Text</span></span>](text.md)                           | <span data-ttu-id="42659-115">Y</span><span class="sxs-lookup"><span data-stu-id="42659-115">Y</span></span>   | <span data-ttu-id="42659-116">N</span><span class="sxs-lookup"><span data-stu-id="42659-116">N</span></span>        |
| <span data-ttu-id="42659-117">LockObject</span><span class="sxs-lookup"><span data-stu-id="42659-117">LockObject</span></span>           | [<span data-ttu-id="42659-118">識別碼</span><span class="sxs-lookup"><span data-stu-id="42659-118">Identifier</span></span>](identifier.md)               | <span data-ttu-id="42659-119">N</span><span class="sxs-lookup"><span data-stu-id="42659-119">N</span></span>   | <span data-ttu-id="42659-120">N</span><span class="sxs-lookup"><span data-stu-id="42659-120">N</span></span>        |
| <span data-ttu-id="42659-121">資料表</span><span class="sxs-lookup"><span data-stu-id="42659-121">Table</span></span>                | [<span data-ttu-id="42659-122">Text</span><span class="sxs-lookup"><span data-stu-id="42659-122">Text</span></span>](text.md)                           | <span data-ttu-id="42659-123">N</span><span class="sxs-lookup"><span data-stu-id="42659-123">N</span></span>   | <span data-ttu-id="42659-124">N</span><span class="sxs-lookup"><span data-stu-id="42659-124">N</span></span>        |
| <span data-ttu-id="42659-125">SDDLText</span><span class="sxs-lookup"><span data-stu-id="42659-125">SDDLText</span></span>             | [<span data-ttu-id="42659-126">FormattedSDDLText</span><span class="sxs-lookup"><span data-stu-id="42659-126">FormattedSDDLText</span></span>](formattedsddltext.md) | <span data-ttu-id="42659-127">N</span><span class="sxs-lookup"><span data-stu-id="42659-127">N</span></span>   | <span data-ttu-id="42659-128">N</span><span class="sxs-lookup"><span data-stu-id="42659-128">N</span></span>        |
| <span data-ttu-id="42659-129">條件</span><span class="sxs-lookup"><span data-stu-id="42659-129">Condition</span></span>            | [<span data-ttu-id="42659-130">Condition</span><span class="sxs-lookup"><span data-stu-id="42659-130">Condition</span></span>](condition.md)                 | <span data-ttu-id="42659-131">N</span><span class="sxs-lookup"><span data-stu-id="42659-131">N</span></span>   | <span data-ttu-id="42659-132">Y</span><span class="sxs-lookup"><span data-stu-id="42659-132">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="42659-133">資料行</span><span class="sxs-lookup"><span data-stu-id="42659-133">Columns</span></span>

<dl> <dt>

<span data-ttu-id="42659-134"><span id="MsiLockPermissionsEx"></span><span id="msilockpermissionsex"></span><span id="MSILOCKPERMISSIONSEX"></span>MsiLockPermissionsEx</span><span class="sxs-lookup"><span data-stu-id="42659-134"><span id="MsiLockPermissionsEx"></span><span id="msilockpermissionsex"></span><span id="MSILOCKPERMISSIONSEX"></span>MsiLockPermissionsEx</span></span>
</dt> <dd>

<span data-ttu-id="42659-135">這是此資料表的主要索引鍵。</span><span class="sxs-lookup"><span data-stu-id="42659-135">This is the primary key of this table.</span></span>

</dd> <dt>

<span data-ttu-id="42659-136"><span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject</span><span class="sxs-lookup"><span data-stu-id="42659-136"><span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject</span></span>
</dt> <dd>

<span data-ttu-id="42659-137">這個資料行和資料表資料行會指定要保護的檔案、目錄、登錄機碼或服務。</span><span class="sxs-lookup"><span data-stu-id="42659-137">This column and the Table column together specify the file, directory, registry key, or service that is to be secured.</span></span> <span data-ttu-id="42659-138">LockObject 資料行是一個外鍵，指向資料表資料行所指定之資料表的主鍵。</span><span class="sxs-lookup"><span data-stu-id="42659-138">The LockObject column is a foreign key that points to the primary key of the table specified by the Table column.</span></span>

</dd> <dt>

<span data-ttu-id="42659-139"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>表</span><span class="sxs-lookup"><span data-stu-id="42659-139"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="42659-140">這個資料行和 LockObject 資料行指定要保護的檔案、目錄、登錄機碼或服務。</span><span class="sxs-lookup"><span data-stu-id="42659-140">This column and the LockObject column specify the file, directory, registry key, or service that is to be secured.</span></span> <span data-ttu-id="42659-141">在 [資料表] 資料行中，輸入 File、Registry、CreateFolder 或 ServiceInstall，以指定檔案 [資料表](file-table.md)、登錄 [資料表](registry-table.md)、 [CreateFolder 資料表](createfolder-table.md)或 [ServiceInstall 資料表](serviceinstall-table.md)中所列的 LockObject。</span><span class="sxs-lookup"><span data-stu-id="42659-141">In the Table column, enter File, Registry, CreateFolder, or ServiceInstall to specify a LockObject listed in the [File Table](file-table.md), [Registry Table](registry-table.md), [CreateFolder Table](createfolder-table.md), or [ServiceInstall Table](serviceinstall-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="42659-142"><span id="SDDLText"></span><span id="sddltext"></span><span id="SDDLTEXT"></span>SDDLText</span><span class="sxs-lookup"><span data-stu-id="42659-142"><span id="SDDLText"></span><span id="sddltext"></span><span id="SDDLTEXT"></span>SDDLText</span></span>
</dt> <dd>

<span data-ttu-id="42659-143">輸入 SDDL 字串，表示要套用至所選物件的許可權。</span><span class="sxs-lookup"><span data-stu-id="42659-143">Enter the SDDL string to indicate permissions to apply to selected object.</span></span> <span data-ttu-id="42659-144">您必須在 [安全描述項字串格式](../secauthz/security-descriptor-string-format.md)中提供 SDDL。</span><span class="sxs-lookup"><span data-stu-id="42659-144">The SDDL must be provided in [Security Descriptor String Format](../secauthz/security-descriptor-string-format.md).</span></span>

<span data-ttu-id="42659-145">這不支援私用或公用屬性。</span><span class="sxs-lookup"><span data-stu-id="42659-145">This does not support private or public properties.</span></span>

</dd> <dt>

<span data-ttu-id="42659-146"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>條件</span><span class="sxs-lookup"><span data-stu-id="42659-146"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="42659-147">此資料行包含條件運算式，用來判斷是否要套用指定的許可權。</span><span class="sxs-lookup"><span data-stu-id="42659-147">This column contains a conditional expression used to determine whether to apply the specified permission.</span></span> <span data-ttu-id="42659-148">如果條件評估為 **FALSE**，則不會套用許可權。</span><span class="sxs-lookup"><span data-stu-id="42659-148">If the condition evaluates to **FALSE**, the permission is not applied.</span></span> <span data-ttu-id="42659-149">如果條件評估為 **TRUE**，則會套用許可權。</span><span class="sxs-lookup"><span data-stu-id="42659-149">If the condition evaluates to **TRUE**, the permission is applied.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="42659-150">備註</span><span class="sxs-lookup"><span data-stu-id="42659-150">Remarks</span></span>

<span data-ttu-id="42659-151">如需保護服務、檔案、登錄機碼和已建立資料夾的詳細資訊，請參閱 [保護資源](securing-resources-.md)。</span><span class="sxs-lookup"><span data-stu-id="42659-151">See [Securing Resources](securing-resources-.md)for more information about securing services, files, registry keys, and created folders.</span></span>

<span data-ttu-id="42659-152">使用 MsiLockPermissionsEx 資料表來保護安裝期間所建立之使用者帳戶的物件。</span><span class="sxs-lookup"><span data-stu-id="42659-152">Use the MsiLockPermissionsEx Table to secure objects for a user account that is being created during the installation.</span></span> <span data-ttu-id="42659-153">當安裝保護物件時，使用者帳戶必須已經存在。</span><span class="sxs-lookup"><span data-stu-id="42659-153">The user account must already exist when the installation secures the object.</span></span> <span data-ttu-id="42659-154">在安裝檔案、登錄機碼、資料夾或服務受保護之前，請先建立使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="42659-154">Create the user account before installing the file, registry key, folder or service being secured.</span></span>

<span data-ttu-id="42659-155">如果這個資料表中的 LockObject 和資料表配對有一個以上的條件運算式評估為 true，則安裝會失敗，且 Windows Installer 會傳回錯誤訊息1942。</span><span class="sxs-lookup"><span data-stu-id="42659-155">If a LockObject and Table pair in this table has more than one conditional expression that evaluates to true, the installation fails and Windows Installer returns an error message 1942.</span></span>

<span data-ttu-id="42659-156">如果 SDDLText 欄位中的 [FormattedSDDLText](formattedsddltext.md) 字串無法解析為有效的 SDDL 字串，則安裝會失敗，且 Windows Installer 會傳回錯誤訊息1943。</span><span class="sxs-lookup"><span data-stu-id="42659-156">If the [FormattedSDDLText](formattedsddltext.md) string in the SDDLText field cannot be resolved into a valid SDDL string, the installation fails and Windows Installer returns an error message 1943.</span></span>

<span data-ttu-id="42659-157">如果使用者沒有足夠的許可權可設定檔案或資料夾上 SDDLText 欄位所指定的安全描述項，則安裝會失敗，且 Windows Installer 會傳回錯誤訊息1926。</span><span class="sxs-lookup"><span data-stu-id="42659-157">If the user does not have sufficient privileges to set the security descriptor specified by the SDDLText field on a file or folder, the installation fails and Windows Installer returns an error message 1926.</span></span>

<span data-ttu-id="42659-158">如果使用者沒有足夠的許可權可設定登錄機碼上 SDDLText 欄位所指定的安全描述項，則安裝會失敗，且 Windows Installer 會傳回錯誤訊息1401。</span><span class="sxs-lookup"><span data-stu-id="42659-158">If the user does not have sufficient privileges to set the security descriptor specified by the SDDLText field on a registry key, the installation fails and Windows Installer returns an error message 1401.</span></span>

<span data-ttu-id="42659-159">如果使用者沒有足夠的許可權可設定服務上 SDDLText 欄位所指定的安全描述項，則安裝會失敗，且 Windows Installer 會傳回錯誤訊息1944。</span><span class="sxs-lookup"><span data-stu-id="42659-159">If the user does not have sufficient privileges to set the security descriptor specified by the SDDLText field on a service, the installation fails and Windows Installer returns an error message 1944.</span></span>

## <a name="validation"></a><span data-ttu-id="42659-160">驗證</span><span class="sxs-lookup"><span data-stu-id="42659-160">Validation</span></span>

<dl>

[<span data-ttu-id="42659-161">ICE104</span><span class="sxs-lookup"><span data-stu-id="42659-161">ICE104</span></span>](ice-104.md)  
[<span data-ttu-id="42659-162">ICE03</span><span class="sxs-lookup"><span data-stu-id="42659-162">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="42659-163">ICE06</span><span class="sxs-lookup"><span data-stu-id="42659-163">ICE06</span></span>](ice06.md)  
</dl>

 

 
