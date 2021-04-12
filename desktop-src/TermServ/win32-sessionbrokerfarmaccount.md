---
title: Win32_SessionBrokerFarmAccount 類別
description: Win32 \_ SessionBrokerFarmAccount 類別無法再供 Windows Server 2012 使用。 |Win32_SessionBrokerFarmAccount 類別
ms.assetid: a76ade0f-cd94-438c-bc07-30dc4b4ee6c8
ms.tgt_platform: multiple
keywords:
- Win32_SessionBrokerFarmAccount 類別遠端桌面服務
- Win32_SessionBrokerFarmAccount 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_SessionBrokerFarmAccount
- Win32_SessionBrokerFarmAccount.FarmName
- Win32_SessionBrokerFarmAccount.Manual
- Win32_SessionBrokerFarmAccount.AccountName
- Win32_SessionBrokerFarmAccount.AccountDomain
- Win32_SessionBrokerFarmAccount.AccountPassword
- Win32_SessionBrokerFarmAccount.AccountSPN1
- Win32_SessionBrokerFarmAccount.AccountSPN2
- Win32_SessionBrokerFarmAccount.ComputerDNSName
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a31f076ddc6f9361be12a57dc60ada24ed75e4bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103696517"
---
# <a name="win32_sessionbrokerfarmaccount-class"></a><span data-ttu-id="47c34-106">Win32 \_ SessionBrokerFarmAccount 類別</span><span class="sxs-lookup"><span data-stu-id="47c34-106">Win32\_SessionBrokerFarmAccount class</span></span>

<span data-ttu-id="47c34-107">\[**Win32 \_ SessionBrokerFarmAccount** 類別無法再供 Windows Server 2012 使用。\]</span><span class="sxs-lookup"><span data-stu-id="47c34-107">\[The **Win32\_SessionBrokerFarmAccount** class is no longer available for use as of Windows Server 2012.\]</span></span>

<span data-ttu-id="47c34-108">定義 session broker 伺服器陣列帳戶。</span><span class="sxs-lookup"><span data-stu-id="47c34-108">Defines a session broker farm account.</span></span>

<span data-ttu-id="47c34-109">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="47c34-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="47c34-110">語法</span><span class="sxs-lookup"><span data-stu-id="47c34-110">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONBROKERFARMACCOUNT_Prov"), AMENDMENT]
class Win32_SessionBrokerFarmAccount
{
  string  FarmName;
  boolean Manual;
  string  AccountName;
  string  AccountDomain;
  string  AccountPassword;
  string  AccountSPN1;
  string  AccountSPN2;
  string  ComputerDNSName;
};
```

## <a name="members"></a><span data-ttu-id="47c34-111">成員</span><span class="sxs-lookup"><span data-stu-id="47c34-111">Members</span></span>

<span data-ttu-id="47c34-112">**Win32 \_ SessionBrokerFarmAccount** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="47c34-112">The **Win32\_SessionBrokerFarmAccount** class has these types of members:</span></span>

-   [<span data-ttu-id="47c34-113">方法</span><span class="sxs-lookup"><span data-stu-id="47c34-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="47c34-114">屬性</span><span class="sxs-lookup"><span data-stu-id="47c34-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="47c34-115">方法</span><span class="sxs-lookup"><span data-stu-id="47c34-115">Methods</span></span>

<span data-ttu-id="47c34-116">**Win32 \_ SessionBrokerFarmAccount** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="47c34-116">The **Win32\_SessionBrokerFarmAccount** class has these methods.</span></span>



| <span data-ttu-id="47c34-117">方法</span><span class="sxs-lookup"><span data-stu-id="47c34-117">Method</span></span>                                                      | <span data-ttu-id="47c34-118">描述</span><span class="sxs-lookup"><span data-stu-id="47c34-118">Description</span></span>                          |
|:------------------------------------------------------------|:-------------------------------------|
| [<span data-ttu-id="47c34-119">**DeleteEx**</span><span class="sxs-lookup"><span data-stu-id="47c34-119">**DeleteEx**</span></span>](deleteex-win32-sessionbrokerfarmaccount.md) | <span data-ttu-id="47c34-120">刪除伺服器陣列帳戶。</span><span class="sxs-lookup"><span data-stu-id="47c34-120">Deletes the farm account.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="47c34-121">屬性</span><span class="sxs-lookup"><span data-stu-id="47c34-121">Properties</span></span>

<span data-ttu-id="47c34-122">**Win32 \_ SessionBrokerFarmAccount** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="47c34-122">The **Win32\_SessionBrokerFarmAccount** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="47c34-123">**AccountDomain**</span><span class="sxs-lookup"><span data-stu-id="47c34-123">**AccountDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47c34-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="47c34-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47c34-125">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="47c34-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="47c34-126">伺服器陣列帳戶所屬網域的名稱。</span><span class="sxs-lookup"><span data-stu-id="47c34-126">The name of the domain the farm account belongs to.</span></span>

</dd> <dt>

<span data-ttu-id="47c34-127">**AccountName**</span><span class="sxs-lookup"><span data-stu-id="47c34-127">**AccountName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47c34-128">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="47c34-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47c34-129">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="47c34-129">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="47c34-130">伺服器陣列帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="47c34-130">The name of the farm account.</span></span>

</dd> <dt>

<span data-ttu-id="47c34-131">**AccountPassword**</span><span class="sxs-lookup"><span data-stu-id="47c34-131">**AccountPassword**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47c34-132">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="47c34-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47c34-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="47c34-133">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="47c34-134">伺服器陣列帳戶的密碼。</span><span class="sxs-lookup"><span data-stu-id="47c34-134">The password of the farm account.</span></span>

</dd> <dt>

<span data-ttu-id="47c34-135">**AccountSPN1**</span><span class="sxs-lookup"><span data-stu-id="47c34-135">**AccountSPN1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47c34-136">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="47c34-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47c34-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="47c34-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="47c34-138">第一個服務主體名稱 (SPN) 與伺服器陣列帳戶相關聯。</span><span class="sxs-lookup"><span data-stu-id="47c34-138">The first service principal name (SPN) associated with the farm account.</span></span>

</dd> <dt>

<span data-ttu-id="47c34-139">**AccountSPN2**</span><span class="sxs-lookup"><span data-stu-id="47c34-139">**AccountSPN2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47c34-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="47c34-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47c34-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="47c34-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="47c34-142">與伺服器陣列帳戶相關聯的第二個 SPN。</span><span class="sxs-lookup"><span data-stu-id="47c34-142">The second SPN associated with the farm account.</span></span>

</dd> <dt>

<span data-ttu-id="47c34-143">**ComputerDNSName**</span><span class="sxs-lookup"><span data-stu-id="47c34-143">**ComputerDNSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47c34-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="47c34-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47c34-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="47c34-145">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="47c34-146">與伺服器陣列帳戶相關聯之電腦的 DNS 名稱。</span><span class="sxs-lookup"><span data-stu-id="47c34-146">The DNS name of the computer associated with the farm account.</span></span>

</dd> <dt>

<span data-ttu-id="47c34-147">**FarmName**</span><span class="sxs-lookup"><span data-stu-id="47c34-147">**FarmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47c34-148">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="47c34-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47c34-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="47c34-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47c34-150">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="47c34-150">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="47c34-151">會話代理程式伺服器陣列的名稱。</span><span class="sxs-lookup"><span data-stu-id="47c34-151">The name of the session broker farm.</span></span>

</dd> <dt>

<span data-ttu-id="47c34-152">**手動**</span><span class="sxs-lookup"><span data-stu-id="47c34-152">**Manual**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47c34-153">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="47c34-153">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="47c34-154">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="47c34-154">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="47c34-155">指出是否以手動方式更新帳戶的密碼。</span><span class="sxs-lookup"><span data-stu-id="47c34-155">Indicates if the password for the account is updated manually.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="47c34-156">規格需求</span><span class="sxs-lookup"><span data-stu-id="47c34-156">Requirements</span></span>



| <span data-ttu-id="47c34-157">需求</span><span class="sxs-lookup"><span data-stu-id="47c34-157">Requirement</span></span> | <span data-ttu-id="47c34-158">值</span><span class="sxs-lookup"><span data-stu-id="47c34-158">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="47c34-159">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="47c34-159">Minimum supported client</span></span><br/> | <span data-ttu-id="47c34-160">都不支援</span><span class="sxs-lookup"><span data-stu-id="47c34-160">None supported</span></span><br/>                                                              |
| <span data-ttu-id="47c34-161">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="47c34-161">Minimum supported server</span></span><br/> | <span data-ttu-id="47c34-162">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="47c34-162">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="47c34-163">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="47c34-163">End of client support</span></span><br/>    | <span data-ttu-id="47c34-164">都不支援</span><span class="sxs-lookup"><span data-stu-id="47c34-164">None supported</span></span><br/>                                                              |
| <span data-ttu-id="47c34-165">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="47c34-165">End of server support</span></span><br/>    | <span data-ttu-id="47c34-166">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="47c34-166">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="47c34-167">命名空間</span><span class="sxs-lookup"><span data-stu-id="47c34-167">Namespace</span></span><br/>                | <span data-ttu-id="47c34-168">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="47c34-168">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="47c34-169">MOF</span><span class="sxs-lookup"><span data-stu-id="47c34-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="47c34-170"><dt>TssdWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="47c34-170"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="47c34-171">DLL</span><span class="sxs-lookup"><span data-stu-id="47c34-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47c34-172"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47c34-172"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

