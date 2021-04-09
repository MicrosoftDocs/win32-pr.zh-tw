---
title: SystemRestore 類別
description: 提供方法來停用和啟用監視、列出可用的還原點，以及在本機系統上起始還原。
ms.assetid: 87216a56-6d40-44ea-a1ab-d43590b639a4
keywords:
- SystemRestore 類別系統還原
- SystemRestore 類別系統還原，說明
topic_type:
- apiref
api_name:
- SystemRestore
- SystemRestore.Description
- SystemRestore.RestorePointType
- SystemRestore.EventType
- SystemRestore.SequenceNumber
- SystemRestore.CreationTime
api_location:
- Root\Default
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64d2b609a7a49a9b319c15745600aa54193350e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025219"
---
# <a name="systemrestore-class"></a><span data-ttu-id="0208c-105">SystemRestore 類別</span><span class="sxs-lookup"><span data-stu-id="0208c-105">SystemRestore class</span></span>

<span data-ttu-id="0208c-106">提供方法來停用和啟用監視、列出可用的還原點，以及在本機系統上起始還原。</span><span class="sxs-lookup"><span data-stu-id="0208c-106">Provides methods for disabling and enabling monitoring, listing available restore points, and initiating a restore on the local system.</span></span>

## <a name="syntax"></a><span data-ttu-id="0208c-107">語法</span><span class="sxs-lookup"><span data-stu-id="0208c-107">Syntax</span></span>

``` syntax
class SystemRestore
{
  String Description;
  uint32 RestorePointType;
  uint32 EventType;
  uint32 SequenceNumber;
  String CreationTime;
};
```

## <a name="members"></a><span data-ttu-id="0208c-108">成員</span><span class="sxs-lookup"><span data-stu-id="0208c-108">Members</span></span>

<span data-ttu-id="0208c-109">**SystemRestore** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0208c-109">The **SystemRestore** class has these types of members:</span></span>

-   [<span data-ttu-id="0208c-110">方法</span><span class="sxs-lookup"><span data-stu-id="0208c-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="0208c-111">屬性</span><span class="sxs-lookup"><span data-stu-id="0208c-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0208c-112">方法</span><span class="sxs-lookup"><span data-stu-id="0208c-112">Methods</span></span>

<span data-ttu-id="0208c-113">**SystemRestore** 類別有這些方法。</span><span class="sxs-lookup"><span data-stu-id="0208c-113">The **SystemRestore** class has these methods.</span></span>



| <span data-ttu-id="0208c-114">方法</span><span class="sxs-lookup"><span data-stu-id="0208c-114">Method</span></span>                                                             | <span data-ttu-id="0208c-115">描述</span><span class="sxs-lookup"><span data-stu-id="0208c-115">Description</span></span>                                                 |
|:-------------------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="0208c-116">**CreateRestorePoint**</span><span class="sxs-lookup"><span data-stu-id="0208c-116">**CreateRestorePoint**</span></span>](createrestorepoint-systemrestore.md)     | <span data-ttu-id="0208c-117">建立還原點。</span><span class="sxs-lookup"><span data-stu-id="0208c-117">Creates a restore point.</span></span><br/>                         |
| [<span data-ttu-id="0208c-118">**停用**</span><span class="sxs-lookup"><span data-stu-id="0208c-118">**Disable**</span></span>](disable-systemrestore.md)                           | <span data-ttu-id="0208c-119">停用特定磁片磁碟機上的監視。</span><span class="sxs-lookup"><span data-stu-id="0208c-119">Disables monitoring on a particular drive.</span></span><br/>       |
| [<span data-ttu-id="0208c-120">**啟用**</span><span class="sxs-lookup"><span data-stu-id="0208c-120">**Enable**</span></span>](enable-systemrestore.md)                             | <span data-ttu-id="0208c-121">在特定磁片磁碟機上啟用監視。</span><span class="sxs-lookup"><span data-stu-id="0208c-121">Enables monitoring on a particular drive.</span></span><br/>        |
| [<span data-ttu-id="0208c-122">**GetLastRestoreStatus**</span><span class="sxs-lookup"><span data-stu-id="0208c-122">**GetLastRestoreStatus**</span></span>](getlastrestorestatus-systemrestore.md) | <span data-ttu-id="0208c-123">捕獲上次系統還原的狀態。</span><span class="sxs-lookup"><span data-stu-id="0208c-123">Retrieves the status of the last system restore.</span></span><br/> |
| [<span data-ttu-id="0208c-124">**還原**</span><span class="sxs-lookup"><span data-stu-id="0208c-124">**Restore**</span></span>](restore-systemrestore.md)                           | <span data-ttu-id="0208c-125">起始系統還原。</span><span class="sxs-lookup"><span data-stu-id="0208c-125">Initiates a system restore.</span></span><br/>                      |



 

### <a name="properties"></a><span data-ttu-id="0208c-126">屬性</span><span class="sxs-lookup"><span data-stu-id="0208c-126">Properties</span></span>

<span data-ttu-id="0208c-127">**SystemRestore** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0208c-127">The **SystemRestore** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0208c-128">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="0208c-128">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0208c-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0208c-129">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="0208c-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0208c-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0208c-131">發生狀態變更的時間。</span><span class="sxs-lookup"><span data-stu-id="0208c-131">The time at which the state change occurred.</span></span>

</dd> <dt>

<span data-ttu-id="0208c-132">**說明**</span><span class="sxs-lookup"><span data-stu-id="0208c-132">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0208c-133">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0208c-133">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="0208c-134">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0208c-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0208c-135">要顯示的描述，讓使用者可以輕鬆地識別還原點。</span><span class="sxs-lookup"><span data-stu-id="0208c-135">The description to be displayed so the user can easily identify a restore point.</span></span> <span data-ttu-id="0208c-136">ANSI 字串的最大長度為最大 \_ DESC。</span><span class="sxs-lookup"><span data-stu-id="0208c-136">The maximum length of an ANSI string is MAX\_DESC.</span></span> <span data-ttu-id="0208c-137">Unicode 字串的最大長度為最大 \_ DESC \_ W。</span><span class="sxs-lookup"><span data-stu-id="0208c-137">The maximum length of a Unicode string is MAX\_DESC\_W.</span></span> <span data-ttu-id="0208c-138">如需詳細資訊，請參閱 [還原點描述文字](restore-point-description-text.md)。</span><span class="sxs-lookup"><span data-stu-id="0208c-138">For more information, see [Restore Point Description Text](restore-point-description-text.md).</span></span>

</dd> <dt>

<span data-ttu-id="0208c-139">**EventType**</span><span class="sxs-lookup"><span data-stu-id="0208c-139">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0208c-140">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0208c-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0208c-141">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0208c-141">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0208c-142">事件的類型。</span><span class="sxs-lookup"><span data-stu-id="0208c-142">The type of event.</span></span> <span data-ttu-id="0208c-143">這個成員可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="0208c-143">This member can be one of the following values.</span></span>



| <span data-ttu-id="0208c-144">值</span><span class="sxs-lookup"><span data-stu-id="0208c-144">Value</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="0208c-145">意義</span><span class="sxs-lookup"><span data-stu-id="0208c-145">Meaning</span></span>                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BEGIN_NESTED_SYSTEM_CHANGE"></span><span id="begin_nested_system_change"></span><dl> <span data-ttu-id="0208c-146"><dt>**開始 \_嵌套 \_ 系統 \_ 變更**</dt> <dt>102</dt></span><span class="sxs-lookup"><span data-stu-id="0208c-146"><dt>**BEGIN\_NESTED\_SYSTEM\_CHANGE**</dt> <dt>102</dt></span></span> </dl> | <span data-ttu-id="0208c-147">系統變更已開始。</span><span class="sxs-lookup"><span data-stu-id="0208c-147">A system change has begun.</span></span> <span data-ttu-id="0208c-148">後續的嵌套呼叫不會建立新的還原點。</span><span class="sxs-lookup"><span data-stu-id="0208c-148">A subsequent nested call does not create a new restore point.</span></span> <br/> <span data-ttu-id="0208c-149">後續呼叫必須使用 END \_ NESTED \_ 系統 \_ 變更，而不是終端 \_ 系統 \_ 變更。</span><span class="sxs-lookup"><span data-stu-id="0208c-149">Subsequent calls must use END\_NESTED\_SYSTEM\_CHANGE, not END\_SYSTEM\_CHANGE.</span></span><br/> |
| <span id="BEGIN_SYSTEM_CHANGE"></span><span id="begin_system_change"></span><dl> <span data-ttu-id="0208c-150"><dt>**開始 \_系統 \_ 變更**</dt> <dt>100</dt></span><span class="sxs-lookup"><span data-stu-id="0208c-150"><dt>**BEGIN\_SYSTEM\_CHANGE**</dt> <dt>100</dt></span></span> </dl>                       | <span data-ttu-id="0208c-151">系統變更已開始。</span><span class="sxs-lookup"><span data-stu-id="0208c-151">A system change has begun.</span></span><br/>                                                                                                                                                           |
| <span id="END_NESTED_SYSTEM_CHANGE"></span><span id="end_nested_system_change"></span><dl> <span data-ttu-id="0208c-152"><dt>**結束 \_嵌套 \_ 系統 \_ 變更**</dt> <dt>103</dt></span><span class="sxs-lookup"><span data-stu-id="0208c-152"><dt>**END\_NESTED\_SYSTEM\_CHANGE**</dt> <dt>103</dt></span></span> </dl>       | <span data-ttu-id="0208c-153">系統變更已結束。</span><span class="sxs-lookup"><span data-stu-id="0208c-153">A system change has ended.</span></span><br/>                                                                                                                                                           |
| <span id="END_SYSTEM_CHANGE"></span><span id="end_system_change"></span><dl> <span data-ttu-id="0208c-154"><dt>**結束 \_系統 \_ 變更**</dt> <dt>101</dt></span><span class="sxs-lookup"><span data-stu-id="0208c-154"><dt>**END\_SYSTEM\_CHANGE**</dt> <dt>101</dt></span></span> </dl>                             | <span data-ttu-id="0208c-155">系統變更已結束。</span><span class="sxs-lookup"><span data-stu-id="0208c-155">A system change has ended.</span></span><br/>                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="0208c-156">**RestorePointType**</span><span class="sxs-lookup"><span data-stu-id="0208c-156">**RestorePointType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0208c-157">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0208c-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0208c-158">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0208c-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0208c-159">還原點的類型。</span><span class="sxs-lookup"><span data-stu-id="0208c-159">The type of restore point.</span></span> <span data-ttu-id="0208c-160">這個成員可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="0208c-160">This member can be one of the following values.</span></span>



| <span data-ttu-id="0208c-161">值</span><span class="sxs-lookup"><span data-stu-id="0208c-161">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="0208c-162">意義</span><span class="sxs-lookup"><span data-stu-id="0208c-162">Meaning</span></span>                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPLICATION_INSTALL"></span><span id="application_install"></span><dl> <span data-ttu-id="0208c-163"><dt>**應用程式 \_安裝**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0208c-163"><dt>**APPLICATION\_INSTALL**</dt> <dt>0</dt></span></span> </dl>         | <span data-ttu-id="0208c-164">已安裝應用程式。</span><span class="sxs-lookup"><span data-stu-id="0208c-164">An application has been installed.</span></span><br/>                                                                                                                 |
| <span id="APPLICATION_UNINSTALL"></span><span id="application_uninstall"></span><dl> <span data-ttu-id="0208c-165"><dt>**應用程式 \_卸載**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0208c-165"><dt>**APPLICATION\_UNINSTALL**</dt> <dt>1</dt></span></span> </dl>   | <span data-ttu-id="0208c-166">已卸載應用程式。</span><span class="sxs-lookup"><span data-stu-id="0208c-166">An application has been uninstalled.</span></span><br/>                                                                                                               |
| <span id="CANCELLED_OPERATION"></span><span id="cancelled_operation"></span><dl> <span data-ttu-id="0208c-167">已 <dt>**取消 \_操作**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="0208c-167"><dt>**CANCELLED\_OPERATION**</dt> <dt>13</dt></span></span> </dl>        | <span data-ttu-id="0208c-168">應用程式必須刪除它所建立的還原點。</span><span class="sxs-lookup"><span data-stu-id="0208c-168">An application needs to delete the restore point it created.</span></span> <span data-ttu-id="0208c-169">例如，當使用者取消安裝時，應用程式會使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="0208c-169">For example, an application would use this flag when a user cancels an installation.</span></span> <br/> |
| <span id="DEVICE_DRIVER_INSTALL"></span><span id="device_driver_install"></span><dl> <span data-ttu-id="0208c-170"><dt>**裝置 \_驅動程式 \_ 安裝**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="0208c-170"><dt>**DEVICE\_DRIVER\_INSTALL**</dt> <dt>10</dt></span></span> </dl> | <span data-ttu-id="0208c-171">已安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="0208c-171">A device driver has been installed.</span></span><br/>                                                                                                                |
| <span id="MODIFY_SETTINGS"></span><span id="modify_settings"></span><dl> <span data-ttu-id="0208c-172"><dt>**修改 \_設定**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="0208c-172"><dt>**MODIFY\_SETTINGS**</dt> <dt>12</dt></span></span> </dl>                    | <span data-ttu-id="0208c-173">應用程式已新增或移除功能。</span><span class="sxs-lookup"><span data-stu-id="0208c-173">An application has had features added or removed.</span></span><br/>                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="0208c-174">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="0208c-174">**SequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0208c-175">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0208c-175">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0208c-176">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0208c-176">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0208c-177">限定詞：索引 **鍵**</span><span class="sxs-lookup"><span data-stu-id="0208c-177">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="0208c-178">還原點的序號。</span><span class="sxs-lookup"><span data-stu-id="0208c-178">The sequence number of the restore point.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0208c-179">備註</span><span class="sxs-lookup"><span data-stu-id="0208c-179">Remarks</span></span>

<span data-ttu-id="0208c-180">您可以使用 [**SWbemServices InstancesOf**](/windows/desktop/WmiSdk/swbemservices-instancesof) 方法取得還原點的清單，以取得 **SystemRestore** 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="0208c-180">You can obtain a list of restore points by using the [**SWbemServices.InstancesOf**](/windows/desktop/WmiSdk/swbemservices-instancesof) method to retrieve a collection of **SystemRestore** objects.</span></span> <span data-ttu-id="0208c-181">您可以使用類別屬性來識別還原點。</span><span class="sxs-lookup"><span data-stu-id="0208c-181">You can use the class properties to identify the restore point.</span></span>

## <a name="examples"></a><span data-ttu-id="0208c-182">範例</span><span class="sxs-lookup"><span data-stu-id="0208c-182">Examples</span></span>

<span data-ttu-id="0208c-183">下列範例腳本會列舉目前的還原點。</span><span class="sxs-lookup"><span data-stu-id="0208c-183">The following sample script enumerates the current restore points.</span></span>


```VB
'SystemRestore Class
'Provides methods for disabling and enabling monitoring, 
'listing available restore points, and initiating a 
'restore on the local system.

Set RPSet = GetObject("winmgmts:root/default").InstancesOf ("SystemRestore")
for each RP in RPSet
    wscript.Echo "Dir: RP" & RP.SequenceNumber & ", Name: " & RP.Description & ", Type: ", RP.RestorePointType & ", Time: " & RP.CreationTime
next
```



## <a name="requirements"></a><span data-ttu-id="0208c-184">規格需求</span><span class="sxs-lookup"><span data-stu-id="0208c-184">Requirements</span></span>



| <span data-ttu-id="0208c-185">需求</span><span class="sxs-lookup"><span data-stu-id="0208c-185">Requirement</span></span> | <span data-ttu-id="0208c-186">值</span><span class="sxs-lookup"><span data-stu-id="0208c-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="0208c-187">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0208c-187">Minimum supported client</span></span><br/> | <span data-ttu-id="0208c-188">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0208c-188">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="0208c-189">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0208c-189">Minimum supported server</span></span><br/> | <span data-ttu-id="0208c-190">都不支援</span><span class="sxs-lookup"><span data-stu-id="0208c-190">None supported</span></span><br/>                                                         |
| <span data-ttu-id="0208c-191">命名空間</span><span class="sxs-lookup"><span data-stu-id="0208c-191">Namespace</span></span><br/>                | <span data-ttu-id="0208c-192">根 \\ 預設值</span><span class="sxs-lookup"><span data-stu-id="0208c-192">Root\\Default</span></span><br/>                                                          |
| <span data-ttu-id="0208c-193">MOF</span><span class="sxs-lookup"><span data-stu-id="0208c-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0208c-194"><dt>Sr-iov</dt></span><span class="sxs-lookup"><span data-stu-id="0208c-194"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0208c-195">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0208c-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0208c-196">Windows Management Instrumentation</span><span class="sxs-lookup"><span data-stu-id="0208c-196">Windows Management Instrumentation</span></span>](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

