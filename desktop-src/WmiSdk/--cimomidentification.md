---
description: 描述 WMI 的本機安裝。
ms.assetid: 907b65b2-a853-40f4-8b36-5a05a2b1cf85
ms.tgt_platform: multiple
title: __CIMOMIdentification 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __CIMOMIdentification
- Root.__CIMOMIdentification.SetupDateTime
- Root.__CIMOMIdentification.VersionCurrentlyRunning
- Root.__CIMOMIdentification.VersionUsedToCreateDB
- Root.__CIMOMIdentification.WorkingDirectory
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: a8590a2a83cdbc9bd06575cf17ddbe65138a4a31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977990"
---
# <a name="__cimomidentification-class"></a><span data-ttu-id="8f91c-103">\_\_CIMOMIdentification 類別</span><span class="sxs-lookup"><span data-stu-id="8f91c-103">\_\_CIMOMIdentification class</span></span>

<span data-ttu-id="8f91c-104">**\_ \_ CIMOMIdentification** 系統類別描述 WMI 的本機安裝。</span><span class="sxs-lookup"><span data-stu-id="8f91c-104">The **\_\_CIMOMIdentification** system class describes the local installation of WMI.</span></span> <span data-ttu-id="8f91c-105">這是單一類別，只有一個實例。</span><span class="sxs-lookup"><span data-stu-id="8f91c-105">This is a singleton class; there is only one instance.</span></span> <span data-ttu-id="8f91c-106">**\_ \_ CIMOMIdentification** 類別僅適用于 **根目錄** 和 **根 \\ 預設** 命名空間。</span><span class="sxs-lookup"><span data-stu-id="8f91c-106">The **\_\_CIMOMIdentification** class is available only in the **Root** and **Root\\Default** namespaces.</span></span> <span data-ttu-id="8f91c-107">使用者查詢實例以取得 WMI 安裝的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8f91c-107">Users query for the instance to obtain information about the WMI installation.</span></span>

<span data-ttu-id="8f91c-108">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="8f91c-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8f91c-109">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="8f91c-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f91c-110">語法</span><span class="sxs-lookup"><span data-stu-id="8f91c-110">Syntax</span></span>

``` syntax
[singleton]
class __CIMOMIdentification : __SystemClass
{
  string SetupDateTime;
  string VersionCurrentlyRunning;
  string VersionUsedToCreateDB;
  string WorkingDirectory;
};
```

## <a name="members"></a><span data-ttu-id="8f91c-111">成員</span><span class="sxs-lookup"><span data-stu-id="8f91c-111">Members</span></span>

<span data-ttu-id="8f91c-112">**\_ \_ CIMOMIdentification** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8f91c-112">The **\_\_CIMOMIdentification** class has these types of members:</span></span>

-   [<span data-ttu-id="8f91c-113">屬性</span><span class="sxs-lookup"><span data-stu-id="8f91c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8f91c-114">屬性</span><span class="sxs-lookup"><span data-stu-id="8f91c-114">Properties</span></span>

<span data-ttu-id="8f91c-115">**\_ \_ CIMOMIdentification** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8f91c-115">The **\_\_CIMOMIdentification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8f91c-116">**SetupDateTime**</span><span class="sxs-lookup"><span data-stu-id="8f91c-116">**SetupDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f91c-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8f91c-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f91c-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f91c-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f91c-119">安裝的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="8f91c-119">Date and time of installation.</span></span> <span data-ttu-id="8f91c-120">第一次安裝作業系統之後，這個屬性是空的。</span><span class="sxs-lookup"><span data-stu-id="8f91c-120">This property is empty after the operating system is installed for the first time.</span></span>

<span data-ttu-id="8f91c-121">如果 WMI 存放庫已刪除，然後再次建立，則此屬性會包含重新建立存放庫的日期和時間。</span><span class="sxs-lookup"><span data-stu-id="8f91c-121">If the WMI repository has been deleted and then created again, this property contains the date and time that the repository is created again.</span></span>

</dd> <dt>

<span data-ttu-id="8f91c-122">**VersionCurrentlyRunning**</span><span class="sxs-lookup"><span data-stu-id="8f91c-122">**VersionCurrentlyRunning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f91c-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8f91c-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f91c-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f91c-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f91c-125">指出實際映射的版本，其中包含建立通用訊息模型 (CIM) 儲存機制的 WMI 服務。</span><span class="sxs-lookup"><span data-stu-id="8f91c-125">Indicates the version of the actual image containing the WMI service that created the Common Information Model (CIM) repository.</span></span> <span data-ttu-id="8f91c-126">由於存放庫格式可能會在 WMI 版本之間變更，因此，此屬性可讓未來的 WMI 升級判斷是否必須升級資料庫。</span><span class="sxs-lookup"><span data-stu-id="8f91c-126">Because the repository format may change between versions of WMI, this property allows future WMI upgrades to determine whether the database must be upgraded.</span></span> <span data-ttu-id="8f91c-127">其格式為：</span><span class="sxs-lookup"><span data-stu-id="8f91c-127">The format is:</span></span>

<span data-ttu-id="8f91c-128">"1.00.183.0000"</span><span class="sxs-lookup"><span data-stu-id="8f91c-128">"1.00.183.0000"</span></span>

<span data-ttu-id="8f91c-129">其中第一個數位是主要版本，接下來的兩個數字是次要版本，而接下來的三個數字則是組建編號。</span><span class="sxs-lookup"><span data-stu-id="8f91c-129">where the first digit is the major version, the next two digits are minor versions, and the next three digits are the build number.</span></span> <span data-ttu-id="8f91c-130">不使用剩餘的數位。</span><span class="sxs-lookup"><span data-stu-id="8f91c-130">The remaining digits are not used.</span></span>

</dd> <dt>

<span data-ttu-id="8f91c-131">**VersionUsedToCreateDB**</span><span class="sxs-lookup"><span data-stu-id="8f91c-131">**VersionUsedToCreateDB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f91c-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8f91c-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f91c-133">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f91c-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f91c-134">指出實際映射的版本，其中包含建立 CIM 儲存機制的 WMI 服務。</span><span class="sxs-lookup"><span data-stu-id="8f91c-134">Indicates the version of the actual image containing the WMI service that created the CIM repository.</span></span> <span data-ttu-id="8f91c-135">由於存放庫格式可能會在 WMI 版本之間變更，因此，此屬性可讓未來的 WMI 升級判斷是否必須升級資料庫。</span><span class="sxs-lookup"><span data-stu-id="8f91c-135">Because the repository format may change between versions of WMI, this property allows future WMI upgrades to determine whether the database must be upgraded.</span></span> <span data-ttu-id="8f91c-136">其格式為：</span><span class="sxs-lookup"><span data-stu-id="8f91c-136">The format is:</span></span>

<span data-ttu-id="8f91c-137">"1.00.183.0000"</span><span class="sxs-lookup"><span data-stu-id="8f91c-137">"1.00.183.0000"</span></span>

<span data-ttu-id="8f91c-138">其中第一個數位是主要版本，接下來的兩個數字是次要版本，而接下來的三個數字則是組建編號。</span><span class="sxs-lookup"><span data-stu-id="8f91c-138">where the first digit is the major version, the next two digits are minor versions, and the next three digits are the build number.</span></span> <span data-ttu-id="8f91c-139">不使用剩餘的數位。</span><span class="sxs-lookup"><span data-stu-id="8f91c-139">The remaining digits are not used.</span></span>

</dd> <dt>

<span data-ttu-id="8f91c-140">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="8f91c-140">**WorkingDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8f91c-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="8f91c-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8f91c-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="8f91c-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8f91c-143">安裝目錄。</span><span class="sxs-lookup"><span data-stu-id="8f91c-143">Installation directory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f91c-144">備註</span><span class="sxs-lookup"><span data-stu-id="8f91c-144">Remarks</span></span>

<span data-ttu-id="8f91c-145">**\_ \_ CIMOMIdentification** 類別衍生自 [**\_ \_ SystemClass**](--systemclass.md)，但沒有屬性。</span><span class="sxs-lookup"><span data-stu-id="8f91c-145">The **\_\_CIMOMIdentification** class is derived from [**\_\_SystemClass**](--systemclass.md), which has no properties.</span></span>

## <a name="examples"></a><span data-ttu-id="8f91c-146">範例</span><span class="sxs-lookup"><span data-stu-id="8f91c-146">Examples</span></span>

<span data-ttu-id="8f91c-147">下列 VBScript 程式碼範例說明如何顯示 CIM 物件模型識別資訊，並取自 \\ \\ Program Files \\ Microsoft sdk \\ Windows \\ 7.0 \\ 範例 \\ sysmgmt \\ wmi \\ 腳本的範例目錄。</span><span class="sxs-lookup"><span data-stu-id="8f91c-147">The following VBScript code sample describes how to display CIM object model identification information, and was taken from the sample directory at \\\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\sysmgmt\\wmi\\scripting.</span></span>


```VB
on error resume next 
set cimomid = GetObject("winmgmts:root\default:__cimomidentification=@")

if err <> 0 then
 WScript.Echo ErrNumber, Err.Source, Err.Description
else
 WScript.Echo cimomid.path_.displayname
 WScript.Echo cimomid.versionusedtocreatedb
end if
```



<span data-ttu-id="8f91c-148">下列 Perl 程式碼範例說明如何顯示 CIM 物件模型識別資訊，並取自 \\ \\ 程式檔 \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ \\ sysmgmt \\ wmi \\ 腳本範例目錄。</span><span class="sxs-lookup"><span data-stu-id="8f91c-148">The following Perl code sample describes how to display CIM object model identification information, and was taken from the sample directory at \\\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\sysmgmt\\wmi\\scripting.</span></span>


```Perl
use strict;
use Win32::OLE;

my ($Cimomid, $locator, $services);

eval { $Cimomid = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\default")->
 Get("__CIMOMIdentification=@"); };

unless ($@)
{
 print "\n", $Cimomid->Path_()->{displayname}, "\n";
 print $Cimomid->{versionusedtocreatedb}, "\n";
}
else
{ 
 print STDERR "\n", Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="8f91c-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f91c-149">Requirements</span></span>



| <span data-ttu-id="8f91c-150">需求</span><span class="sxs-lookup"><span data-stu-id="8f91c-150">Requirement</span></span> | <span data-ttu-id="8f91c-151">值</span><span class="sxs-lookup"><span data-stu-id="8f91c-151">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="8f91c-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8f91c-152">Minimum supported client</span></span><br/> | <span data-ttu-id="8f91c-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f91c-153">Windows Vista</span></span><br/>       |
| <span data-ttu-id="8f91c-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8f91c-154">Minimum supported server</span></span><br/> | <span data-ttu-id="8f91c-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f91c-155">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="8f91c-156">命名空間</span><span class="sxs-lookup"><span data-stu-id="8f91c-156">Namespace</span></span><br/>                | <span data-ttu-id="8f91c-157">Root</span><span class="sxs-lookup"><span data-stu-id="8f91c-157">Root</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="8f91c-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f91c-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f91c-159">**\_\_SystemClass**</span><span class="sxs-lookup"><span data-stu-id="8f91c-159">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="8f91c-160">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="8f91c-160">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

