---
title: Win32_SessionBrokerServiceProperties 類別
description: 定義 session broker 服務的查詢。
ms.assetid: fe7a0317-8b52-4685-9d0d-2f81058b4561
ms.tgt_platform: multiple
keywords:
- Win32_SessionBrokerServiceProperties 類別遠端桌面服務
- Win32_SessionBrokerServiceProperties 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties
- Win32_SessionBrokerServiceProperties.SBNetworkName
- Win32_SessionBrokerServiceProperties.SBDbConnectionString
- Win32_SessionBrokerServiceProperties.SBDbSecondaryConnectionString
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 507c4211b9506e0635966e9541167d24495735ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509376"
---
# <a name="win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="35f1e-105">Win32 \_ SessionBrokerServiceProperties 類別</span><span class="sxs-lookup"><span data-stu-id="35f1e-105">Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="35f1e-106">定義 session broker 服務的查詢。</span><span class="sxs-lookup"><span data-stu-id="35f1e-106">Defines the query for a session broker service.</span></span>

<span data-ttu-id="35f1e-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="35f1e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="35f1e-108">語法</span><span class="sxs-lookup"><span data-stu-id="35f1e-108">Syntax</span></span>

``` syntax
[dynamic, singleton, provider("Win32_WIN32_SESSIONBROKERSERVICEPROPERTIES_Prov"), AMENDMENT]
class Win32_SessionBrokerServiceProperties
{
  string SBNetworkName;
  string SBDbConnectionString;
  string SBDbSecondaryConnectionString;
};
```

## <a name="members"></a><span data-ttu-id="35f1e-109">成員</span><span class="sxs-lookup"><span data-stu-id="35f1e-109">Members</span></span>

<span data-ttu-id="35f1e-110">**Win32 \_ SessionBrokerServiceProperties** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="35f1e-110">The **Win32\_SessionBrokerServiceProperties** class has these types of members:</span></span>

-   [<span data-ttu-id="35f1e-111">方法</span><span class="sxs-lookup"><span data-stu-id="35f1e-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="35f1e-112">屬性</span><span class="sxs-lookup"><span data-stu-id="35f1e-112">Properties</span></span>](/windows)

### <a name="methods"></a><span data-ttu-id="35f1e-113">方法</span><span class="sxs-lookup"><span data-stu-id="35f1e-113">Methods</span></span>

<span data-ttu-id="35f1e-114">**Win32 \_ SessionBrokerServiceProperties** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="35f1e-114">The **Win32\_SessionBrokerServiceProperties** class has these methods.</span></span>



| <span data-ttu-id="35f1e-115">方法</span><span class="sxs-lookup"><span data-stu-id="35f1e-115">Method</span></span>                                                                                                | <span data-ttu-id="35f1e-116">描述</span><span class="sxs-lookup"><span data-stu-id="35f1e-116">Description</span></span>                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="35f1e-117">**DeleteSBDbConnectionString**</span><span class="sxs-lookup"><span data-stu-id="35f1e-117">**DeleteSBDbConnectionString**</span></span>](win32-sessionbrokerserviceproperties-deletesbdbconnectionstring.md) | <span data-ttu-id="35f1e-118">從登錄中刪除主要和次要)  (的資料庫連接字串。</span><span class="sxs-lookup"><span data-stu-id="35f1e-118">Deletes DB connection strings (primary and secondary) from the registry.</span></span><br/> <span data-ttu-id="35f1e-119">**Windows server 2012 r2、Windows server 2012 和 Windows server 2008 R2：** 在 Windows Server 2016 之前無法使用此方法</span><span class="sxs-lookup"><span data-stu-id="35f1e-119">**Windows Server 2012 R2, Windows Server 2012 and Windows Server 2008 R2:** This method is not available prior to Windows Server 2016</span></span><br/> |
| [<span data-ttu-id="35f1e-120">**InstallBrokerDatabase**</span><span class="sxs-lookup"><span data-stu-id="35f1e-120">**InstallBrokerDatabase**</span></span>](win32-sessionbrokerserviceproperties-installbrokerdatabase.md)           | <span data-ttu-id="35f1e-121">在中央 SQL Server 上安裝 RD 連線代理人 DB</span><span class="sxs-lookup"><span data-stu-id="35f1e-121">Installs RD Connection Broker DB on central SQL Server</span></span><br/>                                                                                                                                                                    |
| [<span data-ttu-id="35f1e-122">**IsDbReachable**</span><span class="sxs-lookup"><span data-stu-id="35f1e-122">**IsDbReachable**</span></span>](win32-sessionbrokerserviceproperties-isdbreachable.md)                           | <span data-ttu-id="35f1e-123">檢查資料庫是否可連線</span><span class="sxs-lookup"><span data-stu-id="35f1e-123">Checks if DB is reachable</span></span><br/>                                                                                                                                                                                                 |
| [<span data-ttu-id="35f1e-124">**SetBrokerHAMode**</span><span class="sxs-lookup"><span data-stu-id="35f1e-124">**SetBrokerHAMode**</span></span>](win32-sessionbrokerserviceproperties-setbrokerhamode.md)                       | <span data-ttu-id="35f1e-125">將資料從本機 WID 資料庫移轉至新的 SQL Server 資料庫。</span><span class="sxs-lookup"><span data-stu-id="35f1e-125">Migrates data from local WID DB to the new SQL Server based DB.</span></span> <span data-ttu-id="35f1e-126">它也會將訊息代理程式伺服器設定為使用中央 SQL Server</span><span class="sxs-lookup"><span data-stu-id="35f1e-126">It also configures the broker server to use the central SQL Server</span></span><br/>                                                                                        |
| [<span data-ttu-id="35f1e-127">**SetBrokerNonHAMode**</span><span class="sxs-lookup"><span data-stu-id="35f1e-127">**SetBrokerNonHAMode**</span></span>](win32-sessionbrokerserviceproperties-setbrokernonhamode.md)                 | <span data-ttu-id="35f1e-128">將資料從中央 SQL Server 遷移至本機 DB。</span><span class="sxs-lookup"><span data-stu-id="35f1e-128">Migrates data from central SQL Server to local DB.</span></span> <span data-ttu-id="35f1e-129">它也會將訊息代理程式伺服器設定為使用本機資料庫。</span><span class="sxs-lookup"><span data-stu-id="35f1e-129">It also configures the broker server to use the local DB.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="35f1e-130">**SetSBDbConnectionStrings**</span><span class="sxs-lookup"><span data-stu-id="35f1e-130">**SetSBDbConnectionStrings**</span></span>](win32-sessionbrokerserviceproperties-setsbdbconnectionstrings.md)     | <span data-ttu-id="35f1e-131">將資料庫連接字串儲存 (主要和次要) 登錄中。</span><span class="sxs-lookup"><span data-stu-id="35f1e-131">Saves DB connection strings (primary and secondary) in the registry.</span></span><br/> <span data-ttu-id="35f1e-132">**Windows server 2012 r2、Windows server 2012 和 Windows server 2008 R2：** 在 Windows Server 2016 之前無法使用此方法</span><span class="sxs-lookup"><span data-stu-id="35f1e-132">**Windows Server 2012 R2, Windows Server 2012 and Windows Server 2008 R2:** This method is not available prior to Windows Server 2016</span></span><br/>     |



 

### <a name="properties"></a><span data-ttu-id="35f1e-133">屬性</span><span class="sxs-lookup"><span data-stu-id="35f1e-133">Properties</span></span>

<span data-ttu-id="35f1e-134">**Win32 \_ SessionBrokerServiceProperties** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="35f1e-134">The **Win32\_SessionBrokerServiceProperties** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="35f1e-135">**SBDbConnectionString**</span><span class="sxs-lookup"><span data-stu-id="35f1e-135">**SBDbConnectionString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35f1e-136">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="35f1e-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35f1e-137">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="35f1e-137">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="35f1e-138">Session Broker 服務所使用的資料庫連接字串。</span><span class="sxs-lookup"><span data-stu-id="35f1e-138">Database connection string used by Session Broker service.</span></span>

<span data-ttu-id="35f1e-139">**Windows Server 2008 R2：** 此屬性在 Windows Server 2012 之前無法使用</span><span class="sxs-lookup"><span data-stu-id="35f1e-139">**Windows Server 2008 R2:** This property is not available prior to Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="35f1e-140">**SBDbSecondaryConnectionString**</span><span class="sxs-lookup"><span data-stu-id="35f1e-140">**SBDbSecondaryConnectionString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35f1e-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="35f1e-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35f1e-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="35f1e-142">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="35f1e-143">選擇性。</span><span class="sxs-lookup"><span data-stu-id="35f1e-143">Optional.</span></span> <span data-ttu-id="35f1e-144">Session Broker 服務用來支援密碼到期的次要資料庫連接字串。</span><span class="sxs-lookup"><span data-stu-id="35f1e-144">Secondary database connection string, used by Session Broker service to support password expiration.</span></span>

<span data-ttu-id="35f1e-145">**Windows server 2012 r2、Windows server 2012 和 Windows server 2008 R2：** 此屬性在 Windows Server 2016 之前無法使用</span><span class="sxs-lookup"><span data-stu-id="35f1e-145">**Windows Server 2012 R2, Windows Server 2012 and Windows Server 2008 R2:** This property is not available prior to Windows Server 2016</span></span>

</dd> <dt>

<span data-ttu-id="35f1e-146">**SBNetworkName**</span><span class="sxs-lookup"><span data-stu-id="35f1e-146">**SBNetworkName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35f1e-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="35f1e-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35f1e-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="35f1e-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35f1e-149">Session broker 服務所使用的網路名稱。</span><span class="sxs-lookup"><span data-stu-id="35f1e-149">The network name used by the session broker service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="35f1e-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="35f1e-150">Requirements</span></span>



| <span data-ttu-id="35f1e-151">需求</span><span class="sxs-lookup"><span data-stu-id="35f1e-151">Requirement</span></span> | <span data-ttu-id="35f1e-152">值</span><span class="sxs-lookup"><span data-stu-id="35f1e-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="35f1e-153">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="35f1e-153">Minimum supported client</span></span><br/> | <span data-ttu-id="35f1e-154">都不支援</span><span class="sxs-lookup"><span data-stu-id="35f1e-154">None supported</span></span><br/>                                                              |
| <span data-ttu-id="35f1e-155">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="35f1e-155">Minimum supported server</span></span><br/> | <span data-ttu-id="35f1e-156">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="35f1e-156">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="35f1e-157">命名空間</span><span class="sxs-lookup"><span data-stu-id="35f1e-157">Namespace</span></span><br/>                | <span data-ttu-id="35f1e-158">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="35f1e-158">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="35f1e-159">MOF</span><span class="sxs-lookup"><span data-stu-id="35f1e-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35f1e-160"><dt>TssdWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="35f1e-160"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="35f1e-161">DLL</span><span class="sxs-lookup"><span data-stu-id="35f1e-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35f1e-162"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35f1e-162"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

