---
title: Win32_RDMSDeploymentSettings 類別
description: 管理虛擬桌面集合的部署設定。
ms.assetid: c33563d5-a388-46d3-b23a-797aab9d472a
ms.tgt_platform: multiple
keywords:
- Win32_RDMSDeploymentSettings 類別遠端桌面服務
- Win32_RDMSDeploymentSettings 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6be75f74a71a82800bc6fdd7ba0c4bae5a85021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508472"
---
# <a name="win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="dea6d-105">Win32 \_ RDMSDeploymentSettings 類別</span><span class="sxs-lookup"><span data-stu-id="dea6d-105">Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="dea6d-106">管理虛擬桌面集合的部署設定。</span><span class="sxs-lookup"><span data-stu-id="dea6d-106">Manages deployment settings for a virtual desktop collection.</span></span>

<span data-ttu-id="dea6d-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="dea6d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dea6d-108">語法</span><span class="sxs-lookup"><span data-stu-id="dea6d-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSDeploymentSettings
{
};
```

## <a name="members"></a><span data-ttu-id="dea6d-109">成員</span><span class="sxs-lookup"><span data-stu-id="dea6d-109">Members</span></span>

<span data-ttu-id="dea6d-110">**Win32 \_ RDMSDeploymentSettings** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="dea6d-110">The **Win32\_RDMSDeploymentSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="dea6d-111">方法</span><span class="sxs-lookup"><span data-stu-id="dea6d-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="dea6d-112">方法</span><span class="sxs-lookup"><span data-stu-id="dea6d-112">Methods</span></span>

<span data-ttu-id="dea6d-113">**Win32 \_ RDMSDeploymentSettings** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="dea6d-113">The **Win32\_RDMSDeploymentSettings** class has these methods.</span></span>



| <span data-ttu-id="dea6d-114">方法</span><span class="sxs-lookup"><span data-stu-id="dea6d-114">Method</span></span>                                                                                                  | <span data-ttu-id="dea6d-115">描述</span><span class="sxs-lookup"><span data-stu-id="dea6d-115">Description</span></span>                                                                                                                       |
|:--------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dea6d-116">**GetBaseVHDPath**</span><span class="sxs-lookup"><span data-stu-id="dea6d-116">**GetBaseVHDPath**</span></span>](getbasevhdpath-win32-rdmsdeploymentsettings.md)                                   | <span data-ttu-id="dea6d-117">抓取虛擬桌面集合 Vhd 部署所在目錄的基底路徑。</span><span class="sxs-lookup"><span data-stu-id="dea6d-117">Retrieves the base path to the directory to which VHDs of the virtual desktop collection are deployed.</span></span><br/>                 |
| [<span data-ttu-id="dea6d-118">**GetConnectionString**</span><span class="sxs-lookup"><span data-stu-id="dea6d-118">**GetConnectionString**</span></span>](win32-rdmsdeploymentsettings-getconnectionstring.md)                         | <span data-ttu-id="dea6d-119">抓取部署層級的資料庫連接字串。</span><span class="sxs-lookup"><span data-stu-id="dea6d-119">Retrieves the deployment-level database connection string.</span></span><br/>                                                             |
| [<span data-ttu-id="dea6d-120">**GetDiffVHDPath**</span><span class="sxs-lookup"><span data-stu-id="dea6d-120">**GetDiffVHDPath**</span></span>](getdiffvhdpath-win32-rdmsdeploymentsettings.md)                                   | <span data-ttu-id="dea6d-121">抓取為虛擬桌面集合部署差異磁片的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="dea6d-121">Retrieves the directory path to which the differencing disks are deployed for a virtual desktop collection.</span></span><br/>            |
| [<span data-ttu-id="dea6d-122">**GetExportPath**</span><span class="sxs-lookup"><span data-stu-id="dea6d-122">**GetExportPath**</span></span>](getexportpath-win32-rdmsdeploymentsettings.md)                                     | <span data-ttu-id="dea6d-123">抓取虛擬機器集合的虛擬機器部署所在的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="dea6d-123">Retrieves the directory path to which virtual machines are deployed for a virtual desktop collection.</span></span><br/>                  |
| [<span data-ttu-id="dea6d-124">**GetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="dea6d-124">**GetInt32Property**</span></span>](getint32property-win32-rdmsdeploymentsettings.md)                               | <span data-ttu-id="dea6d-125">抓取虛擬桌面集合部署設定的整數屬性。</span><span class="sxs-lookup"><span data-stu-id="dea6d-125">Retrieves an integer property for the deployment settings of a virtual desktop collection.</span></span><br/>                             |
| [<span data-ttu-id="dea6d-126">**GetSecondaryConnectionString**</span><span class="sxs-lookup"><span data-stu-id="dea6d-126">**GetSecondaryConnectionString**</span></span>](win32-rdmsdeploymentsettings-getsecondaryconnectionstring.md)       | <span data-ttu-id="dea6d-127">抓取部署層級資料庫的次要連接字串，可用來支援密碼到期。</span><span class="sxs-lookup"><span data-stu-id="dea6d-127">Retrieves the deployment-level database secondary connection string, which may be used to support password expiration.</span></span><br/> |
| [<span data-ttu-id="dea6d-128">**GetSMBPath**</span><span class="sxs-lookup"><span data-stu-id="dea6d-128">**GetSMBPath**</span></span>](getsmbpath-win32-rdmsdeploymentsettings.md)                                           | <span data-ttu-id="dea6d-129">抓取虛擬桌面集合的虛擬機器部署所在 SMB 共用的 UNC 路徑。</span><span class="sxs-lookup"><span data-stu-id="dea6d-129">Retrieves the UNC path to the SMB share to which virtual machines of the virtual desktop collection are deployed.</span></span><br/>      |
| [<span data-ttu-id="dea6d-130">**GetStringArrayDeploymentSetting**</span><span class="sxs-lookup"><span data-stu-id="dea6d-130">**GetStringArrayDeploymentSetting**</span></span>](getstringarraydeploymentsetting-win32-rdmsdeploymentsettings.md) | <span data-ttu-id="dea6d-131">抓取虛擬桌面集合的部署設定。</span><span class="sxs-lookup"><span data-stu-id="dea6d-131">Retrieves the deployment settings for a virtual desktop collection.</span></span><br/>                                                    |
| [<span data-ttu-id="dea6d-132">**GetStringProperty**</span><span class="sxs-lookup"><span data-stu-id="dea6d-132">**GetStringProperty**</span></span>](getstringproperty-win32-rdmsdeploymentsettings.md)                             | <span data-ttu-id="dea6d-133">抓取虛擬桌面集合之部署設定的字串屬性。</span><span class="sxs-lookup"><span data-stu-id="dea6d-133">Retrieves a string property for the deployment settings of a virtual desktop collection.</span></span><br/>                               |
| [<span data-ttu-id="dea6d-134">**RemoveDeploymentSetting**</span><span class="sxs-lookup"><span data-stu-id="dea6d-134">**RemoveDeploymentSetting**</span></span>](removedeploymentsetting-win32-rdmsdeploymentsettings.md)                 | <span data-ttu-id="dea6d-135">刪除虛擬桌面集合的部署設定。</span><span class="sxs-lookup"><span data-stu-id="dea6d-135">Deletes the deployment settings for a virtual desktop collection.</span></span><br/>                                                      |
| [<span data-ttu-id="dea6d-136">**SetBaseVHDPath**</span><span class="sxs-lookup"><span data-stu-id="dea6d-136">**SetBaseVHDPath**</span></span>](setbasevhdpath-win32-rdmsdeploymentsettings.md)                                   | <span data-ttu-id="dea6d-137">抓取虛擬桌面集合 Vhd 部署所在目錄的基底路徑。</span><span class="sxs-lookup"><span data-stu-id="dea6d-137">Retrieves the base path to the directory to which VHDs of the virtual desktop collection are deployed.</span></span><br/>                 |
| [<span data-ttu-id="dea6d-138">**SetConnectionString**</span><span class="sxs-lookup"><span data-stu-id="dea6d-138">**SetConnectionString**</span></span>](win32-rdmsdeploymentsettings-setconnectionstring.md)                         | <span data-ttu-id="dea6d-139">設定部署層級的資料庫連接字串。</span><span class="sxs-lookup"><span data-stu-id="dea6d-139">Sets the deployment-level database connection string.</span></span><br/>                                                                  |
| [<span data-ttu-id="dea6d-140">**SetDiffVHDPath**</span><span class="sxs-lookup"><span data-stu-id="dea6d-140">**SetDiffVHDPath**</span></span>](setdiffvhdpath-win32-rdmsdeploymentsettings.md)                                   | <span data-ttu-id="dea6d-141">更新為虛擬桌面集合部署差異磁片的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="dea6d-141">Updates the directory path to which the differencing disks are deployed for a virtual desktop collection.</span></span><br/>              |
| [<span data-ttu-id="dea6d-142">**SetExportPath**</span><span class="sxs-lookup"><span data-stu-id="dea6d-142">**SetExportPath**</span></span>](setexportpath-win32-rdmsdeploymentsettings.md)                                     | <span data-ttu-id="dea6d-143">更新虛擬機器集合的虛擬機器部署所在的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="dea6d-143">Updates the directory path to which virtual machines are deployed for a virtual desktop collection.</span></span><br/>                    |
| [<span data-ttu-id="dea6d-144">**SetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="dea6d-144">**SetInt32Property**</span></span>](setint32property-win32-rdmsdeploymentsettings.md)                               | <span data-ttu-id="dea6d-145">針對虛擬桌面集合的部署設定，更新整數屬性。</span><span class="sxs-lookup"><span data-stu-id="dea6d-145">Updates an integer property for the deployment settings of a virtual desktop collection.</span></span><br/>                               |
| [<span data-ttu-id="dea6d-146">**SetSecondaryConnectionString**</span><span class="sxs-lookup"><span data-stu-id="dea6d-146">**SetSecondaryConnectionString**</span></span>](win32-rdmsdeploymentsettings-setsecondaryconnectionstring.md)       | <span data-ttu-id="dea6d-147">設定部署層級資料庫次要連接字串。</span><span class="sxs-lookup"><span data-stu-id="dea6d-147">Sets the deployment-level database secondary connection string.</span></span><br/>                                                        |
| [<span data-ttu-id="dea6d-148">**SetSMBPath**</span><span class="sxs-lookup"><span data-stu-id="dea6d-148">**SetSMBPath**</span></span>](setsmbpath-win32-rdmsdeploymentsettings.md)                                           | <span data-ttu-id="dea6d-149">將 UNC 路徑更新為虛擬桌面集合的虛擬機器部署所在的 SMB 共用。</span><span class="sxs-lookup"><span data-stu-id="dea6d-149">Updates the UNC path to the SMB share to which virtual machines of the virtual desktop collection are deployed.</span></span><br/>        |
| [<span data-ttu-id="dea6d-150">**SetStringArrayDeploymentSetting**</span><span class="sxs-lookup"><span data-stu-id="dea6d-150">**SetStringArrayDeploymentSetting**</span></span>](setstringarraydeploymentsetting-win32-rdmsdeploymentsettings.md) | <span data-ttu-id="dea6d-151">更新虛擬桌面集合的部署設定。</span><span class="sxs-lookup"><span data-stu-id="dea6d-151">Updates the deployment settings for a virtual desktop collection.</span></span><br/>                                                      |
| [<span data-ttu-id="dea6d-152">**SetStringProperty**</span><span class="sxs-lookup"><span data-stu-id="dea6d-152">**SetStringProperty**</span></span>](setstringproperty-win32-rdmsdeploymentsettings.md)                             | <span data-ttu-id="dea6d-153">更新虛擬桌面集合之部署設定的字串屬性。</span><span class="sxs-lookup"><span data-stu-id="dea6d-153">Updates a string property for the deployment settings of a virtual desktop collection.</span></span><br/>                                 |



 

## <a name="requirements"></a><span data-ttu-id="dea6d-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="dea6d-154">Requirements</span></span>



| <span data-ttu-id="dea6d-155">需求</span><span class="sxs-lookup"><span data-stu-id="dea6d-155">Requirement</span></span> | <span data-ttu-id="dea6d-156">值</span><span class="sxs-lookup"><span data-stu-id="dea6d-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="dea6d-157">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dea6d-157">Minimum supported client</span></span><br/> | <span data-ttu-id="dea6d-158">都不支援</span><span class="sxs-lookup"><span data-stu-id="dea6d-158">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="dea6d-159">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dea6d-159">Minimum supported server</span></span><br/> | <span data-ttu-id="dea6d-160">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dea6d-160">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="dea6d-161">命名空間</span><span class="sxs-lookup"><span data-stu-id="dea6d-161">Namespace</span></span><br/>                | <span data-ttu-id="dea6d-162">根 \\ cimv2 \\ rdm</span><span class="sxs-lookup"><span data-stu-id="dea6d-162">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="dea6d-163">MOF</span><span class="sxs-lookup"><span data-stu-id="dea6d-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dea6d-164"><dt>RDManagement mof</dt></span><span class="sxs-lookup"><span data-stu-id="dea6d-164"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="dea6d-165">DLL</span><span class="sxs-lookup"><span data-stu-id="dea6d-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dea6d-166"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dea6d-166"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="dea6d-167">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dea6d-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dea6d-168">遠端桌面管理服務提供者</span><span class="sxs-lookup"><span data-stu-id="dea6d-168">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

 





