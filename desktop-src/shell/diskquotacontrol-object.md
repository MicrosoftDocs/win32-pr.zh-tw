---
description: 可讓系統管理員管理磁片區的磁片配額屬性。
title: DiskQuotaControl 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 846297f2-b826-45de-8617-228790e87a63
ms.openlocfilehash: 5f7b1d700c73df56ce7aaef39e162517629f96f6
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841549"
---
# <a name="diskquotacontrol-object"></a><span data-ttu-id="3955c-103">DiskQuotaControl 物件</span><span class="sxs-lookup"><span data-stu-id="3955c-103">DiskQuotaControl object</span></span>

<span data-ttu-id="3955c-104">可讓系統管理員管理磁片區的磁片配額屬性。</span><span class="sxs-lookup"><span data-stu-id="3955c-104">Allows an administrator to manage a volume's disk quota properties.</span></span> <span data-ttu-id="3955c-105">NTFS 檔案系統可讓系統管理員藉由為每個使用者配置指定的磁碟空間數量或 *配額限制*，來管理共用磁片區上的磁片使用量。</span><span class="sxs-lookup"><span data-stu-id="3955c-105">The NTFS file system allows an administrator to manage disk usage on a shared volume by allocating a specified amount of disk space, or *quota limit*, to each user.</span></span> <span data-ttu-id="3955c-106">您可以使用此物件來設定將自動指派給所有新使用者的預設配額限制。</span><span class="sxs-lookup"><span data-stu-id="3955c-106">You can use this object to set the default quota limit that will be automatically assigned to all new users.</span></span>

## <a name="members"></a><span data-ttu-id="3955c-107">成員</span><span class="sxs-lookup"><span data-stu-id="3955c-107">Members</span></span>

<span data-ttu-id="3955c-108">**DiskQuotaControl** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3955c-108">The **DiskQuotaControl** object has these types of members:</span></span>

-   [<span data-ttu-id="3955c-109">事件</span><span class="sxs-lookup"><span data-stu-id="3955c-109">Events</span></span>](#events)
-   [<span data-ttu-id="3955c-110">方法</span><span class="sxs-lookup"><span data-stu-id="3955c-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="3955c-111">屬性</span><span class="sxs-lookup"><span data-stu-id="3955c-111">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="3955c-112">事件</span><span class="sxs-lookup"><span data-stu-id="3955c-112">Events</span></span>

<span data-ttu-id="3955c-113">**DiskQuotaControl** 物件具有這些事件。</span><span class="sxs-lookup"><span data-stu-id="3955c-113">The **DiskQuotaControl** object has these events.</span></span>



| <span data-ttu-id="3955c-114">事件</span><span class="sxs-lookup"><span data-stu-id="3955c-114">Event</span></span>                                                           | <span data-ttu-id="3955c-115">描述</span><span class="sxs-lookup"><span data-stu-id="3955c-115">Description</span></span>                                                                                                                   |
|:----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3955c-116">**OnUserNameChanged**</span><span class="sxs-lookup"><span data-stu-id="3955c-116">**OnUserNameChanged**</span></span>](diskquotacontrol-onusernamechanged.md) | <span data-ttu-id="3955c-117">當已解析 [**DIDiskQuotaUser**](didiskquotauser-object.md) 物件的名稱資訊時發生。</span><span class="sxs-lookup"><span data-stu-id="3955c-117">Occurs when the name information for a [**DIDiskQuotaUser**](didiskquotauser-object.md) object has been resolved.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="3955c-118">方法</span><span class="sxs-lookup"><span data-stu-id="3955c-118">Methods</span></span>

<span data-ttu-id="3955c-119">**DiskQuotaControl** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="3955c-119">The **DiskQuotaControl** object has these methods.</span></span>



| <span data-ttu-id="3955c-120">方法</span><span class="sxs-lookup"><span data-stu-id="3955c-120">Method</span></span>                                                                                    | <span data-ttu-id="3955c-121">描述</span><span class="sxs-lookup"><span data-stu-id="3955c-121">Description</span></span>                                                                                |
|:------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3955c-122">**AddUser**</span><span class="sxs-lookup"><span data-stu-id="3955c-122">**AddUser**</span></span>](diskquotacontrol-adduser.md)                                               | <span data-ttu-id="3955c-123">將非預設磁片配額指派給新的使用者。</span><span class="sxs-lookup"><span data-stu-id="3955c-123">Assigns a nondefault disk quota to a new user.</span></span><br/>                                  |
| [<span data-ttu-id="3955c-124">**DeleteUser**</span><span class="sxs-lookup"><span data-stu-id="3955c-124">**DeleteUser**</span></span>](diskquotacontrol-deleteuser.md)                                         | <span data-ttu-id="3955c-125">從磁片區刪除使用者。</span><span class="sxs-lookup"><span data-stu-id="3955c-125">Deletes a user from the volume.</span></span><br/>                                                 |
| [<span data-ttu-id="3955c-126">**FindUser**</span><span class="sxs-lookup"><span data-stu-id="3955c-126">**FindUser**</span></span>](diskquotacontrol-finduser.md)                                             | <span data-ttu-id="3955c-127">在磁片區的配額檔案中，依名稱尋找使用者的專案。</span><span class="sxs-lookup"><span data-stu-id="3955c-127">Finds a user's entry, by name, in the volume's quota file.</span></span><br/>                      |
| [<span data-ttu-id="3955c-128">**GiveUserNameResolutionPriority**</span><span class="sxs-lookup"><span data-stu-id="3955c-128">**GiveUserNameResolutionPriority**</span></span>](diskquotacontrol-giveusernameresolutionpriority.md) | <span data-ttu-id="3955c-129">將指定的使用者物件放在行中，以進行名稱解析。</span><span class="sxs-lookup"><span data-stu-id="3955c-129">Places the specified user object next in line for name resolution.</span></span><br/>              |
| [<span data-ttu-id="3955c-130">**初始化**</span><span class="sxs-lookup"><span data-stu-id="3955c-130">**Initialize**</span></span>](diskquotacontrol-initialize.md)                                         | <span data-ttu-id="3955c-131">開啟指定的磁片區，並初始化其配額控制物件。</span><span class="sxs-lookup"><span data-stu-id="3955c-131">Opens a specified volume and initializes its quota control object.</span></span><br/>              |
| [<span data-ttu-id="3955c-132">**InvalidateSidNameCache**</span><span class="sxs-lookup"><span data-stu-id="3955c-132">**InvalidateSidNameCache**</span></span>](diskquotacontrol-invalidatesidnamecache.md)                 | <span data-ttu-id="3955c-133">使安全性識別碼的使用者名稱快取失效。</span><span class="sxs-lookup"><span data-stu-id="3955c-133">Invalidates the security ID user name cache.</span></span><br/>                                    |
| [<span data-ttu-id="3955c-134">**ShutdownNameResolution**</span><span class="sxs-lookup"><span data-stu-id="3955c-134">**ShutdownNameResolution**</span></span>](diskquotacontrol-shutdownnameresolution.md)                 | <span data-ttu-id="3955c-135">關閉使用者名稱解析執行緒。</span><span class="sxs-lookup"><span data-stu-id="3955c-135">Shuts down the user name resolution thread.</span></span><br/>                                     |
| [<span data-ttu-id="3955c-136">**TranslateLogonNameToSID**</span><span class="sxs-lookup"><span data-stu-id="3955c-136">**TranslateLogonNameToSID**</span></span>](diskquotacontrol-translatelogonnametosid.md)               | <span data-ttu-id="3955c-137">以字串格式將登入名稱轉譯為對應的使用者安全識別碼。</span><span class="sxs-lookup"><span data-stu-id="3955c-137">Translates a logon name to the corresponding user security ID in string format.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3955c-138">屬性</span><span class="sxs-lookup"><span data-stu-id="3955c-138">Properties</span></span>

<span data-ttu-id="3955c-139">**DiskQuotaControl** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3955c-139">The **DiskQuotaControl** object has these properties.</span></span>



| <span data-ttu-id="3955c-140">屬性</span><span class="sxs-lookup"><span data-stu-id="3955c-140">Property</span></span>                                                                                   | <span data-ttu-id="3955c-141">存取類型</span><span class="sxs-lookup"><span data-stu-id="3955c-141">Access type</span></span>           | <span data-ttu-id="3955c-142">描述</span><span class="sxs-lookup"><span data-stu-id="3955c-142">Description</span></span>                                                                                                                                                   |
|:-------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3955c-143">**DefaultQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="3955c-143">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)<br/>                 | <span data-ttu-id="3955c-144">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3955c-144">Read/write</span></span><br/> | <span data-ttu-id="3955c-145">設定或取得預設配額限制。</span><span class="sxs-lookup"><span data-stu-id="3955c-145">Sets or gets the default quota limit.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="3955c-146">**DefaultQuotaLimitText**</span><span class="sxs-lookup"><span data-stu-id="3955c-146">**DefaultQuotaLimitText**</span></span>](diskquotacontrol-defaultquotalimittext.md)<br/>         | <span data-ttu-id="3955c-147">唯讀</span><span class="sxs-lookup"><span data-stu-id="3955c-147">Read-only</span></span><br/>  | <span data-ttu-id="3955c-148">取得做為文字字串的預設配額限制。</span><span class="sxs-lookup"><span data-stu-id="3955c-148">Gets the default quota limit as a text string.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="3955c-149">**DefaultQuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="3955c-149">**DefaultQuotaThreshold**</span></span>](diskquotacontrol-defaultquotathreshold.md)<br/>         | <span data-ttu-id="3955c-150">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3955c-150">Read/write</span></span><br/> | <span data-ttu-id="3955c-151">設定或取得預設配額閾值。</span><span class="sxs-lookup"><span data-stu-id="3955c-151">Sets or gets the default quota threshold.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="3955c-152">**DefaultQuotaThresholdText**</span><span class="sxs-lookup"><span data-stu-id="3955c-152">**DefaultQuotaThresholdText**</span></span>](diskquotacontrol-defaultquotathresholdtext.md)<br/> | <span data-ttu-id="3955c-153">唯讀</span><span class="sxs-lookup"><span data-stu-id="3955c-153">Read-only</span></span><br/>  | <span data-ttu-id="3955c-154">取得預設配額閾值做為文字字串。</span><span class="sxs-lookup"><span data-stu-id="3955c-154">Gets the default quota threshold as a text string.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="3955c-155">**LogQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="3955c-155">**LogQuotaLimit**</span></span>](diskquotacontrol-logquotalimit.md)<br/>                         | <span data-ttu-id="3955c-156">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3955c-156">Read/write</span></span><br/> | <span data-ttu-id="3955c-157">設定或取得布林值，這個值會指出當使用者超過其指派的配額限制時，是否要建立系統事件記錄檔專案。</span><span class="sxs-lookup"><span data-stu-id="3955c-157">Sets or gets a Boolean value that indicates whether a system event log entry will be made when a user exceeds his or her assigned quota limit.</span></span><br/>     |
| [<span data-ttu-id="3955c-158">**LogQuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="3955c-158">**LogQuotaThreshold**</span></span>](diskquotacontrol-logquotathreshold.md)<br/>                 | <span data-ttu-id="3955c-159">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3955c-159">Read/write</span></span><br/> | <span data-ttu-id="3955c-160">設定或取得布林值，這個值會指出當使用者超過其指派的配額閾值時，是否要建立系統事件記錄檔專案。</span><span class="sxs-lookup"><span data-stu-id="3955c-160">Sets or gets a Boolean value that indicates whether a system event log entry will be made when a user exceeds his or her assigned quota threshold.</span></span><br/> |
| [<span data-ttu-id="3955c-161">**QuotaFileIncomplete**</span><span class="sxs-lookup"><span data-stu-id="3955c-161">**QuotaFileIncomplete**</span></span>](diskquotacontrol-quotafileincomplete.md)<br/>             | <span data-ttu-id="3955c-162">唯讀</span><span class="sxs-lookup"><span data-stu-id="3955c-162">Read-only</span></span><br/>  | <span data-ttu-id="3955c-163">取得布林值，這個值會指出磁片區的配額檔案是否已完成。</span><span class="sxs-lookup"><span data-stu-id="3955c-163">Gets a Boolean value that indicates whether the quota file for the volume is complete.</span></span><br/>                                                             |
| [<span data-ttu-id="3955c-164">**QuotaFileRebuilding**</span><span class="sxs-lookup"><span data-stu-id="3955c-164">**QuotaFileRebuilding**</span></span>](diskquotacontrol-quotafilerebuilding.md)<br/>             | <span data-ttu-id="3955c-165">唯讀</span><span class="sxs-lookup"><span data-stu-id="3955c-165">Read-only</span></span><br/>  | <span data-ttu-id="3955c-166">取得布林值，指出目前是否正在重建磁片區的配額檔案。</span><span class="sxs-lookup"><span data-stu-id="3955c-166">Gets a Boolean value that indicates whether the quota file for the volume is currently being rebuilt.</span></span><br/>                                              |
| [<span data-ttu-id="3955c-167">**QuotaState**</span><span class="sxs-lookup"><span data-stu-id="3955c-167">**QuotaState**</span></span>](diskquotacontrol-quotastate.md)<br/>                               | <span data-ttu-id="3955c-168">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3955c-168">Read/write</span></span><br/> | <span data-ttu-id="3955c-169">設定或取得磁片區磁片配額的狀態。</span><span class="sxs-lookup"><span data-stu-id="3955c-169">Sets or gets the state of the volume's disk quotas.</span></span><br/>                                                                                                |
| [<span data-ttu-id="3955c-170">**UserNameResolution**</span><span class="sxs-lookup"><span data-stu-id="3955c-170">**UserNameResolution**</span></span>](diskquotacontrol-usernameresolution.md)<br/>               | <span data-ttu-id="3955c-171">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3955c-171">Read/write</span></span><br/> | <span data-ttu-id="3955c-172">設定或取得值，這個值會控制如何將使用者 SID 解析為使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="3955c-172">Sets or gets a value that controls how user SID are resolved to user names.</span></span><br/>                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="3955c-173">備註</span><span class="sxs-lookup"><span data-stu-id="3955c-173">Remarks</span></span>

<span data-ttu-id="3955c-174">系統管理員可以使用 **DiskQuotaControl** 物件來執行一些工作，包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="3955c-174">An administrator can use the **DiskQuotaControl** object to do a number of tasks, including the following:</span></span>

-   <span data-ttu-id="3955c-175">啟用和停用磁片區的磁片配額系統。</span><span class="sxs-lookup"><span data-stu-id="3955c-175">Enabling and disabling the volume's disk quota system.</span></span>
-   <span data-ttu-id="3955c-176">取得磁片區上配額系統的狀態。</span><span class="sxs-lookup"><span data-stu-id="3955c-176">Obtaining the status of the quota system on the volume.</span></span>
-   <span data-ttu-id="3955c-177">拒絕超過配額限制的使用者磁碟空間。</span><span class="sxs-lookup"><span data-stu-id="3955c-177">Denying disk space to users exceeding their quota limit.</span></span>
-   <span data-ttu-id="3955c-178">指定預設的警告臨界值，以及將指派給新使用者的配額限制值。</span><span class="sxs-lookup"><span data-stu-id="3955c-178">Specifying the default warning threshold and quota limit values that will be assigned to new users.</span></span>
-   <span data-ttu-id="3955c-179">新增和移除使用者。</span><span class="sxs-lookup"><span data-stu-id="3955c-179">Adding and removing users.</span></span>

<span data-ttu-id="3955c-180">**DiskQuotaControl** 物件可讓您設定磁片區的全域預設值，例如配額限制。</span><span class="sxs-lookup"><span data-stu-id="3955c-180">The **DiskQuotaControl** object allows you to set global default values for the volume for properties such as quota limits.</span></span> <span data-ttu-id="3955c-181">不過，每個使用者都是由可用來指定個別配額設定的 [**DIDiskQuotaUser**](didiskquotauser-object.md) 物件表示。</span><span class="sxs-lookup"><span data-stu-id="3955c-181">However, each user is represented by a [**DIDiskQuotaUser**](didiskquotauser-object.md) object that can be used to specify individual quota settings.</span></span>

<span data-ttu-id="3955c-182">有幾種方式可以取得使用者的 [**DIDiskQuotaUser**](didiskquotauser-object.md) 物件：</span><span class="sxs-lookup"><span data-stu-id="3955c-182">There are several ways to obtain a user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object:</span></span>

-   <span data-ttu-id="3955c-183">具有磁片區配額之所有使用者的 [**DIDiskQuotaUser**](didiskquotauser-object.md) 物件會公開為集合，而且可以列舉。</span><span class="sxs-lookup"><span data-stu-id="3955c-183">The [**DIDiskQuotaUser**](didiskquotauser-object.md) objects for all users with quotas on the volume are exposed as a collection, and can be enumerated.</span></span> <span data-ttu-id="3955c-184">如需有關如何列舉 **DIDiskQuotaUser** 物件的討論，請參閱 **DIDiskQuotaUser** 的「備註」一節中的「**列舉磁片配額使用者**」。</span><span class="sxs-lookup"><span data-stu-id="3955c-184">For a discussion of how to enumerate **DIDiskQuotaUser** objects, see **Enumerating Disk Quota Users** in the Remarks section of **DIDiskQuotaUser**.</span></span>
-   <span data-ttu-id="3955c-185">當您加入新的使用者時， [**AddUser**](diskquotacontrol-adduser.md) 方法會傳回使用者的 [**DIDiskQuotaUser**](didiskquotauser-object.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="3955c-185">When you add a new user, the [**AddUser**](diskquotacontrol-adduser.md) method returns the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>
-   <span data-ttu-id="3955c-186">如果您有使用者的名稱， [**FindUser**](diskquotacontrol-finduser.md) 方法會傳回使用者的 [**DIDiskQuotaUser**](didiskquotauser-object.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="3955c-186">If you have the user's name, the [**FindUser**](diskquotacontrol-finduser.md) method returns the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>

<span data-ttu-id="3955c-187">這個物件讓 IDiskQuotaControl 介面的基本功能可供腳本和 Microsoft Visual Basic 應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="3955c-187">This object makes the essential functionality of the IDiskQuotaControl interface available to scripting and Microsoft Visual Basic-based applications.</span></span>

## <a name="requirements"></a><span data-ttu-id="3955c-188">規格需求</span><span class="sxs-lookup"><span data-stu-id="3955c-188">Requirements</span></span>



| <span data-ttu-id="3955c-189">需求</span><span class="sxs-lookup"><span data-stu-id="3955c-189">Requirement</span></span> | <span data-ttu-id="3955c-190">值</span><span class="sxs-lookup"><span data-stu-id="3955c-190">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3955c-191">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3955c-191">Minimum supported client</span></span><br/> | <span data-ttu-id="3955c-192">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3955c-192">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3955c-193">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3955c-193">Minimum supported server</span></span><br/> | <span data-ttu-id="3955c-194">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3955c-194">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="3955c-195">DLL</span><span class="sxs-lookup"><span data-stu-id="3955c-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3955c-196"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="3955c-196"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3955c-197">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3955c-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3955c-198">**Shell 物件**</span><span class="sxs-lookup"><span data-stu-id="3955c-198">**Shell Object**</span></span>](shell.md)
</dt> </dl>

 

 




