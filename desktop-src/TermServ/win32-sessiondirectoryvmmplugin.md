---
title: Win32_SessionDirectoryVMMPlugin 類別
description: 代表已向會話代理人註冊 (VMM) 外掛程式的 virtual machine manager。
ms.assetid: b5c5deb1-6c1b-4547-a24a-db3ce6654144
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectoryVMMPlugin 類別遠端桌面服務
- Win32_SessionDirectoryVMMPlugin 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin
- Win32_SessionDirectoryVMMPlugin.sName
- Win32_SessionDirectoryVMMPlugin.sProvider
- Win32_SessionDirectoryVMMPlugin.sClassID
- Win32_SessionDirectoryVMMPlugin.sServiceLocation
- Win32_SessionDirectoryVMMPlugin.Priority
- Win32_SessionDirectoryVMMPlugin.Enabled
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c5fc6b899eaa264357527eb107e11ad5a40ad67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934057"
---
# <a name="win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="61ee8-105">Win32 \_ SessionDirectoryVMMPlugin 類別</span><span class="sxs-lookup"><span data-stu-id="61ee8-105">Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="61ee8-106">代表已向會話代理人註冊 (VMM) 外掛程式的 virtual machine manager。</span><span class="sxs-lookup"><span data-stu-id="61ee8-106">Represents a virtual machine manager (VMM) plug-in registered with a session broker.</span></span>

<span data-ttu-id="61ee8-107">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="61ee8-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="61ee8-108">語法</span><span class="sxs-lookup"><span data-stu-id="61ee8-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYVMMPLUGIN_Prov"), AMENDMENT]
class Win32_SessionDirectoryVMMPlugin
{
  string  sName;
  string  sProvider;
  string  sClassID;
  string  sServiceLocation;
  sint32  Priority = 0;
  boolean Enabled = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="61ee8-109">成員</span><span class="sxs-lookup"><span data-stu-id="61ee8-109">Members</span></span>

<span data-ttu-id="61ee8-110">**Win32 \_ SessionDirectoryVMMPlugin** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="61ee8-110">The **Win32\_SessionDirectoryVMMPlugin** class has these types of members:</span></span>

-   [<span data-ttu-id="61ee8-111">方法</span><span class="sxs-lookup"><span data-stu-id="61ee8-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="61ee8-112">屬性</span><span class="sxs-lookup"><span data-stu-id="61ee8-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="61ee8-113">方法</span><span class="sxs-lookup"><span data-stu-id="61ee8-113">Methods</span></span>

<span data-ttu-id="61ee8-114">**Win32 \_ SessionDirectoryVMMPlugin** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="61ee8-114">The **Win32\_SessionDirectoryVMMPlugin** class has these methods.</span></span>



| <span data-ttu-id="61ee8-115">方法</span><span class="sxs-lookup"><span data-stu-id="61ee8-115">Method</span></span>                                                                             | <span data-ttu-id="61ee8-116">描述</span><span class="sxs-lookup"><span data-stu-id="61ee8-116">Description</span></span>                                                   |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="61ee8-117">**GetCurrentVMMPlugin**</span><span class="sxs-lookup"><span data-stu-id="61ee8-117">**GetCurrentVMMPlugin**</span></span>](getcurrentvmmplugin-win32-sessiondirectoryvmmplugin.md) | <span data-ttu-id="61ee8-118">取得已啟用的最高優先順序外掛程式。</span><span class="sxs-lookup"><span data-stu-id="61ee8-118">Gets the highest priority plug-in that is enabled.</span></span><br/> |
| [<span data-ttu-id="61ee8-119">**RegisterVMMPlugin**</span><span class="sxs-lookup"><span data-stu-id="61ee8-119">**RegisterVMMPlugin**</span></span>](registervmmplugin-win32-sessiondirectoryvmmplugin.md)     | <span data-ttu-id="61ee8-120">註冊新的 VMM 外掛程式。</span><span class="sxs-lookup"><span data-stu-id="61ee8-120">Registers a new VMM plug-in.</span></span><br/>                       |
| [<span data-ttu-id="61ee8-121">**SetEnabled**</span><span class="sxs-lookup"><span data-stu-id="61ee8-121">**SetEnabled**</span></span>](setenabled-win32-sessiondirectoryvmmplugin.md)                   | <span data-ttu-id="61ee8-122">啟用或停用外掛程式。</span><span class="sxs-lookup"><span data-stu-id="61ee8-122">Enables or disables the plug-in.</span></span><br/>                   |
| [<span data-ttu-id="61ee8-123">**SetName**</span><span class="sxs-lookup"><span data-stu-id="61ee8-123">**SetName**</span></span>](setname-win32-sessiondirectoryvmmplugin.md)                         | <span data-ttu-id="61ee8-124">設定外掛程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="61ee8-124">Sets the name of the plug-in.</span></span><br/>                      |
| [<span data-ttu-id="61ee8-125">**SetPriority**</span><span class="sxs-lookup"><span data-stu-id="61ee8-125">**SetPriority**</span></span>](setpriority-win32-sessiondirectoryvmmplugin.md)                 | <span data-ttu-id="61ee8-126">設定外掛程式的優先順序。</span><span class="sxs-lookup"><span data-stu-id="61ee8-126">Sets the priority of the plug-in.</span></span><br/>                  |
| [<span data-ttu-id="61ee8-127">**SetProvider**</span><span class="sxs-lookup"><span data-stu-id="61ee8-127">**SetProvider**</span></span>](setprovider-win32-sessiondirectoryvmmplugin.md)                 | <span data-ttu-id="61ee8-128">設定外掛程式的提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="61ee8-128">Sets the provider name of the plug-in.</span></span><br/>             |
| [<span data-ttu-id="61ee8-129">**SetServiceLocation**</span><span class="sxs-lookup"><span data-stu-id="61ee8-129">**SetServiceLocation**</span></span>](setservicelocation-win32-sessiondirectoryvmmplugin.md)   | <span data-ttu-id="61ee8-130">設定外掛程式的服務位置。</span><span class="sxs-lookup"><span data-stu-id="61ee8-130">Sets the service location of the plug-in.</span></span><br/>          |
| [<span data-ttu-id="61ee8-131">**UnregisterVMMPlugin**</span><span class="sxs-lookup"><span data-stu-id="61ee8-131">**UnregisterVMMPlugin**</span></span>](unregistervmmplugin-win32-sessiondirectoryvmmplugin.md) | <span data-ttu-id="61ee8-132">取消註冊外掛程式。</span><span class="sxs-lookup"><span data-stu-id="61ee8-132">Unregisters the plug-in.</span></span><br/>                           |



 

### <a name="properties"></a><span data-ttu-id="61ee8-133">屬性</span><span class="sxs-lookup"><span data-stu-id="61ee8-133">Properties</span></span>

<span data-ttu-id="61ee8-134">**Win32 \_ SessionDirectoryVMMPlugin** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="61ee8-134">The **Win32\_SessionDirectoryVMMPlugin** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="61ee8-135">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="61ee8-135">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61ee8-136">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="61ee8-136">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="61ee8-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="61ee8-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61ee8-138">指出外掛程式是否已啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="61ee8-138">Indicates whether the plug-in is enabled or disabled.</span></span> <span data-ttu-id="61ee8-139">如果外掛程式已啟用則 **為 True** ，否則為 **false** 。</span><span class="sxs-lookup"><span data-stu-id="61ee8-139">**True** if the plug-in is enabled or **false** otherwise.</span></span> <span data-ttu-id="61ee8-140">預設會停用外掛程式。</span><span class="sxs-lookup"><span data-stu-id="61ee8-140">The plug-in is disabled by default.</span></span>

</dd> <dt>

<span data-ttu-id="61ee8-141">**優先順序**</span><span class="sxs-lookup"><span data-stu-id="61ee8-141">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61ee8-142">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="61ee8-142">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="61ee8-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="61ee8-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61ee8-144">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="61ee8-144">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="61ee8-145">外掛程式的優先順序。</span><span class="sxs-lookup"><span data-stu-id="61ee8-145">The priority of the plug-in.</span></span> <span data-ttu-id="61ee8-146">值愈高，外掛程式的優先順序愈高。</span><span class="sxs-lookup"><span data-stu-id="61ee8-146">The higher the value, the higher the priority of the plug-in.</span></span> <span data-ttu-id="61ee8-147">優先權預設為零。</span><span class="sxs-lookup"><span data-stu-id="61ee8-147">The priority is zero by default.</span></span>

</dd> <dt>

<span data-ttu-id="61ee8-148">**sClassID**</span><span class="sxs-lookup"><span data-stu-id="61ee8-148">**sClassID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61ee8-149">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="61ee8-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61ee8-150">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="61ee8-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61ee8-151">外掛程式的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="61ee8-151">The class identifier of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="61ee8-152">**sName**</span><span class="sxs-lookup"><span data-stu-id="61ee8-152">**sName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61ee8-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="61ee8-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61ee8-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="61ee8-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61ee8-155">外掛程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="61ee8-155">The name of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="61ee8-156">**sProvider**</span><span class="sxs-lookup"><span data-stu-id="61ee8-156">**sProvider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61ee8-157">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="61ee8-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61ee8-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="61ee8-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61ee8-159">外掛程式提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="61ee8-159">The name of the plug-in provider.</span></span>

</dd> <dt>

<span data-ttu-id="61ee8-160">**sServiceLocation**</span><span class="sxs-lookup"><span data-stu-id="61ee8-160">**sServiceLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61ee8-161">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="61ee8-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="61ee8-162">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="61ee8-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="61ee8-163">外掛程式應聯絡的服務位置。</span><span class="sxs-lookup"><span data-stu-id="61ee8-163">The service location that the plug-in should contact.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="61ee8-164">規格需求</span><span class="sxs-lookup"><span data-stu-id="61ee8-164">Requirements</span></span>



| <span data-ttu-id="61ee8-165">需求</span><span class="sxs-lookup"><span data-stu-id="61ee8-165">Requirement</span></span> | <span data-ttu-id="61ee8-166">值</span><span class="sxs-lookup"><span data-stu-id="61ee8-166">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="61ee8-167">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="61ee8-167">Minimum supported client</span></span><br/> | <span data-ttu-id="61ee8-168">都不支援</span><span class="sxs-lookup"><span data-stu-id="61ee8-168">None supported</span></span><br/>                                                              |
| <span data-ttu-id="61ee8-169">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="61ee8-169">Minimum supported server</span></span><br/> | <span data-ttu-id="61ee8-170">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="61ee8-170">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="61ee8-171">命名空間</span><span class="sxs-lookup"><span data-stu-id="61ee8-171">Namespace</span></span><br/>                | <span data-ttu-id="61ee8-172">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="61ee8-172">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="61ee8-173">MOF</span><span class="sxs-lookup"><span data-stu-id="61ee8-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61ee8-174"><dt>TssdWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="61ee8-174"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="61ee8-175">DLL</span><span class="sxs-lookup"><span data-stu-id="61ee8-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61ee8-176"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61ee8-176"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

