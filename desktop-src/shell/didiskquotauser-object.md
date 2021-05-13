---
description: 允許用戶端管理 NTFS 磁片區的全域磁片配額設定。 這個物件讓 DIDiskQuotaUser 介面的基本功能可供腳本和 Microsoft Visual Basic 應用程式使用。
title: DIDiskQuotaUser 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 0cdf3293-3dcf-44e7-a80d-4eacf9d09fbf
ms.openlocfilehash: b370056f40320561a38b1f77fbcf9a53ee35686a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843239"
---
# <a name="didiskquotauser-object"></a><span data-ttu-id="d7f82-104">DIDiskQuotaUser 物件</span><span class="sxs-lookup"><span data-stu-id="d7f82-104">DIDiskQuotaUser object</span></span>

<span data-ttu-id="d7f82-105">允許用戶端管理 NTFS 磁片區的全域磁片配額設定。</span><span class="sxs-lookup"><span data-stu-id="d7f82-105">Allows a client to manage an NTFS volume's global disk quota settings.</span></span> <span data-ttu-id="d7f82-106">這個物件讓 **DIDiskQuotaUser** 介面的基本功能可供腳本和 Microsoft Visual Basic 應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="d7f82-106">This object makes the essential functionality of the **DIDiskQuotaUser** interface available to scripting and Microsoft Visual Basic-based applications.</span></span>

## <a name="members"></a><span data-ttu-id="d7f82-107">成員</span><span class="sxs-lookup"><span data-stu-id="d7f82-107">Members</span></span>

<span data-ttu-id="d7f82-108">**DIDiskQuotaUser** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d7f82-108">The **DIDiskQuotaUser** object has these types of members:</span></span>

-   [<span data-ttu-id="d7f82-109">方法</span><span class="sxs-lookup"><span data-stu-id="d7f82-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="d7f82-110">屬性</span><span class="sxs-lookup"><span data-stu-id="d7f82-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d7f82-111">方法</span><span class="sxs-lookup"><span data-stu-id="d7f82-111">Methods</span></span>

<span data-ttu-id="d7f82-112">**DIDiskQuotaUser** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="d7f82-112">The **DIDiskQuotaUser** object has these methods.</span></span>



| <span data-ttu-id="d7f82-113">方法</span><span class="sxs-lookup"><span data-stu-id="d7f82-113">Method</span></span>                                           | <span data-ttu-id="d7f82-114">描述</span><span class="sxs-lookup"><span data-stu-id="d7f82-114">Description</span></span>                                             |
|:-------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="d7f82-115">**無效**</span><span class="sxs-lookup"><span data-stu-id="d7f82-115">**Invalidate**</span></span>](didiskquotauser-invalidate.md) | <span data-ttu-id="d7f82-116">清除物件的快取使用者資訊。</span><span class="sxs-lookup"><span data-stu-id="d7f82-116">Clears the object's cached user information.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d7f82-117">屬性</span><span class="sxs-lookup"><span data-stu-id="d7f82-117">Properties</span></span>

<span data-ttu-id="d7f82-118">**DIDiskQuotaUser** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d7f82-118">The **DIDiskQuotaUser** object has these properties.</span></span>



| <span data-ttu-id="d7f82-119">屬性</span><span class="sxs-lookup"><span data-stu-id="d7f82-119">Property</span></span>                                                                        | <span data-ttu-id="d7f82-120">存取類型</span><span class="sxs-lookup"><span data-stu-id="d7f82-120">Access type</span></span>           | <span data-ttu-id="d7f82-121">描述</span><span class="sxs-lookup"><span data-stu-id="d7f82-121">Description</span></span>                                                                                          |
|:--------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d7f82-122">**AccountContainerName**</span><span class="sxs-lookup"><span data-stu-id="d7f82-122">**AccountContainerName**</span></span>](didiskquotauser-accountcontainername.md)<br/> | <span data-ttu-id="d7f82-123">唯讀</span><span class="sxs-lookup"><span data-stu-id="d7f82-123">Read-only</span></span><br/>  | <span data-ttu-id="d7f82-124">取得使用者帳戶容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="d7f82-124">Gets the name of the user's account container.</span></span><br/>                                            |
| [<span data-ttu-id="d7f82-125">**AccountStatus**</span><span class="sxs-lookup"><span data-stu-id="d7f82-125">**AccountStatus**</span></span>](didiskquotauser-accountstatus.md)<br/>               | <span data-ttu-id="d7f82-126">唯讀</span><span class="sxs-lookup"><span data-stu-id="d7f82-126">Read-only</span></span><br/>  | <span data-ttu-id="d7f82-127">取得使用者帳戶的狀態。</span><span class="sxs-lookup"><span data-stu-id="d7f82-127">Gets the status of the user's account.</span></span><br/>                                                    |
| [<span data-ttu-id="d7f82-128">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="d7f82-128">**DisplayName**</span></span>](didiskquotauser-displayname.md)<br/>                   | <span data-ttu-id="d7f82-129">唯讀</span><span class="sxs-lookup"><span data-stu-id="d7f82-129">Read-only</span></span><br/>  | <span data-ttu-id="d7f82-130">取得使用者的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="d7f82-130">Gets the user's display name.</span></span><br/>                                                             |
| [<span data-ttu-id="d7f82-131">**識別碼**</span><span class="sxs-lookup"><span data-stu-id="d7f82-131">**ID**</span></span>](didiskquotauser-id.md)<br/>                                     | <span data-ttu-id="d7f82-132">唯讀</span><span class="sxs-lookup"><span data-stu-id="d7f82-132">Read-only</span></span><br/>  | <span data-ttu-id="d7f82-133">取得可唯一識別使用者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d7f82-133">Gets an ID that uniquely identifies the user.</span></span><br/>                                             |
| [<span data-ttu-id="d7f82-134">**LogonName**</span><span class="sxs-lookup"><span data-stu-id="d7f82-134">**LogonName**</span></span>](didiskquotauser-logonname.md)<br/>                       | <span data-ttu-id="d7f82-135">唯讀</span><span class="sxs-lookup"><span data-stu-id="d7f82-135">Read-only</span></span><br/>  | <span data-ttu-id="d7f82-136">取得使用者的登入帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="d7f82-136">Gets the user's logon account name.</span></span><br/>                                                       |
| [<span data-ttu-id="d7f82-137">**QuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="d7f82-137">**QuotaLimit**</span></span>](didiskquotauser-quotalimit.md)<br/>                     | <span data-ttu-id="d7f82-138">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d7f82-138">Read/write</span></span><br/> | <span data-ttu-id="d7f82-139">設定或取得使用者目前的 [**配額限制**](diskquotacontrol-object.md)。</span><span class="sxs-lookup"><span data-stu-id="d7f82-139">Sets or gets the user's current [**quota limit**](diskquotacontrol-object.md).</span></span><br/>           |
| [<span data-ttu-id="d7f82-140">**QuotaLimitText**</span><span class="sxs-lookup"><span data-stu-id="d7f82-140">**QuotaLimitText**</span></span>](didiskquotauser-quotalimittext.md)<br/>             | <span data-ttu-id="d7f82-141">唯讀</span><span class="sxs-lookup"><span data-stu-id="d7f82-141">Read-only</span></span><br/>  | <span data-ttu-id="d7f82-142">取得使用者目前的 [**配額限制**](diskquotacontrol-object.md) ，作為文字字串。</span><span class="sxs-lookup"><span data-stu-id="d7f82-142">Gets the user's current [**quota limit**](diskquotacontrol-object.md) as a text string.</span></span> <br/> |
| [<span data-ttu-id="d7f82-143">**QuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="d7f82-143">**QuotaThreshold**</span></span>](didiskquotauser-quotathreshold.md)<br/>             | <span data-ttu-id="d7f82-144">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d7f82-144">Read/write</span></span><br/> | <span data-ttu-id="d7f82-145">設定或取得使用者的警告臨界值（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="d7f82-145">Sets or gets the user's warning threshold, in bytes.</span></span><br/>                                      |
| [<span data-ttu-id="d7f82-146">**QuotaThresholdText**</span><span class="sxs-lookup"><span data-stu-id="d7f82-146">**QuotaThresholdText**</span></span>](didiskquotauser-quotathresholdtext.md)<br/>     | <span data-ttu-id="d7f82-147">唯讀</span><span class="sxs-lookup"><span data-stu-id="d7f82-147">Read-only</span></span><br/>  | <span data-ttu-id="d7f82-148">取得使用者的警告臨界值做為文字字串。</span><span class="sxs-lookup"><span data-stu-id="d7f82-148">Gets the user's warning threshold as a text string.</span></span><br/>                                       |
| [<span data-ttu-id="d7f82-149">**QuotaUsed**</span><span class="sxs-lookup"><span data-stu-id="d7f82-149">**QuotaUsed**</span></span>](didiskquotauser-quotaused.md)<br/>                       | <span data-ttu-id="d7f82-150">唯讀</span><span class="sxs-lookup"><span data-stu-id="d7f82-150">Read-only</span></span><br/>  | <span data-ttu-id="d7f82-151">取得使用者目前的磁片使用量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="d7f82-151">Gets the user's current disk usage, in bytes.</span></span><br/>                                             |
| [<span data-ttu-id="d7f82-152">**QuotaUsedText**</span><span class="sxs-lookup"><span data-stu-id="d7f82-152">**QuotaUsedText**</span></span>](didiskquotauser-quotausedtext.md)<br/>               | <span data-ttu-id="d7f82-153">唯讀</span><span class="sxs-lookup"><span data-stu-id="d7f82-153">Read-only</span></span><br/>  | <span data-ttu-id="d7f82-154">以文字字串形式取得使用者的目前磁片使用量。</span><span class="sxs-lookup"><span data-stu-id="d7f82-154">Gets the user's current disk usage as a text string.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="d7f82-155">備註</span><span class="sxs-lookup"><span data-stu-id="d7f82-155">Remarks</span></span>

<span data-ttu-id="d7f82-156">[**DiskQuotaControl**](diskquotacontrol-object.md)物件所管理之磁片區上的每個使用者都有與其相關聯的 **DIDiskQuotaUser** 物件。</span><span class="sxs-lookup"><span data-stu-id="d7f82-156">Each user on the volume that is managed by the [**DiskQuotaControl**](diskquotacontrol-object.md) object has a **DIDiskQuotaUser** object associated with it.</span></span> <span data-ttu-id="d7f82-157">此物件可讓用戶端管理個別使用者的設定。</span><span class="sxs-lookup"><span data-stu-id="d7f82-157">This object allows a client to manage an individual user's settings.</span></span> <span data-ttu-id="d7f82-158">有幾種方式可以取得使用者的 **DIDiskQuotaUser** 物件：</span><span class="sxs-lookup"><span data-stu-id="d7f82-158">There are several ways to obtain a user's **DIDiskQuotaUser** object:</span></span>

-   <span data-ttu-id="d7f82-159">具有磁片區配額之所有使用者的 **DIDiskQuotaUser** 物件會公開為集合，而且可以列舉。</span><span class="sxs-lookup"><span data-stu-id="d7f82-159">The **DIDiskQuotaUser** objects for all users with quotas on the volume are exposed as a collection and can be enumerated.</span></span> <span data-ttu-id="d7f82-160">有關如何列舉 **DIDiskQuotaUser** 物件的討論，請參閱下面。</span><span class="sxs-lookup"><span data-stu-id="d7f82-160">A discussion of how to enumerate **DIDiskQuotaUser** objects is found below.</span></span>
-   <span data-ttu-id="d7f82-161">當您加入新的使用者時， [**AddUser**](diskquotacontrol-adduser.md) 方法會傳回使用者的 **DIDiskQuotaUser** 物件。</span><span class="sxs-lookup"><span data-stu-id="d7f82-161">When you add a new user, the [**AddUser**](diskquotacontrol-adduser.md) method returns the user's **DIDiskQuotaUser** object.</span></span>
-   <span data-ttu-id="d7f82-162">如果您有使用者的名稱， [**FindUser**](diskquotacontrol-finduser.md) 方法會傳回使用者的 **DIDiskQuotaUser** 物件。</span><span class="sxs-lookup"><span data-stu-id="d7f82-162">If you have the user's name, the [**FindUser**](diskquotacontrol-finduser.md) method returns the user's **DIDiskQuotaUser** object.</span></span>

### <a name="enumerating-disk-quota-users"></a><span data-ttu-id="d7f82-163">列舉磁片配額使用者</span><span class="sxs-lookup"><span data-stu-id="d7f82-163">Enumerating Disk Quota Users</span></span>

<span data-ttu-id="d7f82-164">具有磁片區配額之所有使用者的 **DIDiskQuotaUser** 物件會公開為集合。</span><span class="sxs-lookup"><span data-stu-id="d7f82-164">The **DIDiskQuotaUser** objects for all users with a quota on the volume are exposed as a collection.</span></span> <span data-ttu-id="d7f82-165">[**DiskQuotaControl**](diskquotacontrol-object.md)物件會匯出標準的枚舉器方法，可讓您列舉 **DIDiskQuotaUser** 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="d7f82-165">The [**DiskQuotaControl**](diskquotacontrol-object.md) object exports a standard enumerator method that allows you to enumerate the collection of **DIDiskQuotaUser** objects.</span></span> <span data-ttu-id="d7f82-166">下列程式說明如何使用 Microsoft JScript 執行列舉， (與 ECMA 262 語言規格) 相容。</span><span class="sxs-lookup"><span data-stu-id="d7f82-166">The following procedure illustrates how to perform the enumeration with Microsoft JScript (compatible with ECMA 262 language specification).</span></span> <span data-ttu-id="d7f82-167">您可以使用類似的程式與 Visual Basic 或 Microsoft Visual Basic Scripting Edition (VBScript) 。</span><span class="sxs-lookup"><span data-stu-id="d7f82-167">You can use a similar procedure with Visual Basic or Microsoft Visual Basic Scripting Edition (VBScript).</span></span>

1.  <span data-ttu-id="d7f82-168">建立新的 [**DiskQuotaControl**](diskquotacontrol-object.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="d7f82-168">Create a new [**DiskQuotaControl**](diskquotacontrol-object.md) object.</span></span>
2.  <span data-ttu-id="d7f82-169">使用 [**initialize**](diskquotacontrol-initialize.md)將它初始化。</span><span class="sxs-lookup"><span data-stu-id="d7f82-169">Initialize it with [**Initialize**](diskquotacontrol-initialize.md).</span></span>
3.  <span data-ttu-id="d7f82-170">建立新的 JScript **列舉** 值物件。</span><span class="sxs-lookup"><span data-stu-id="d7f82-170">Create a new JScript **Enumerator** object.</span></span>
4.  <span data-ttu-id="d7f82-171">使用 **for** 迴圈來列舉 **DIDiskQuotaUser** 物件。</span><span class="sxs-lookup"><span data-stu-id="d7f82-171">Use a **for** loop to enumerate the **DIDiskQuotaUser** objects.</span></span> <span data-ttu-id="d7f82-172">不需要設定起始值。</span><span class="sxs-lookup"><span data-stu-id="d7f82-172">There is no need to set a starting value.</span></span> <span data-ttu-id="d7f82-173">列舉值物件的 **moveNext** 方法會通知 **專案** 方法傳回下一個 **DIDiskQuotaUser** 物件。</span><span class="sxs-lookup"><span data-stu-id="d7f82-173">The enumerator object's **moveNext** method notifies the **item** method to return the next **DIDiskQuotaUser** object.</span></span> <span data-ttu-id="d7f82-174">當您到達清單結尾時， **atEnd** 方法會傳回 **false** 。</span><span class="sxs-lookup"><span data-stu-id="d7f82-174">The **atEnd** method returns **false** when you reach the end of the list.</span></span>
5.  <span data-ttu-id="d7f82-175">如有需要，請使用列舉值之 **item** 方法所傳回的 **DIDiskQuotaUser** 物件，以抓取或設定一或多個相關聯的使用者磁片配額屬性。</span><span class="sxs-lookup"><span data-stu-id="d7f82-175">As needed, use the **DIDiskQuotaUser** object returned by the enumerator's **item** method to retrieve or set one or more of the associated user's disk quota properties.</span></span>

<span data-ttu-id="d7f82-176">下列程式碼片段說明如何使用 JScript 列舉 **DIDiskQuotaUser** 物件。</span><span class="sxs-lookup"><span data-stu-id="d7f82-176">The following code fragment illustrates how to enumerate **DIDiskQuotaUser** objects with JScript.</span></span> <span data-ttu-id="d7f82-177">傳遞至 **EnumUsers** 函數的 **磁片區卷 \_ 標** 引數是包含磁片區標籤（例如 "C："）的字串值 \\ \\ 。</span><span class="sxs-lookup"><span data-stu-id="d7f82-177">The **Volume\_Label** argument that is passed to the **EnumUsers** function is a string value containing a volume label such as "C:\\\\".</span></span>


```
function EnumUsers(Volume_Label)
{
    var Volume;
    var QuotaUsers;
    var QuotaUser;

    Volume = new ActiveXObject("Microsoft.DiskQuota.1");
    Volume.Initialize(Volume_Label, 1);

    QuotaUsers = new Enumerator(Volume);
    for (;!Users.atEnd(); Users.moveNext())
    {
       QuotaUser = QuotaUsers.item();

     //Use the QuotaUser object to retrieve or set one or more
     //of the user's disk quota properties
     ...
    }
}
```



## <a name="requirements"></a><span data-ttu-id="d7f82-178">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7f82-178">Requirements</span></span>



| <span data-ttu-id="d7f82-179">需求</span><span class="sxs-lookup"><span data-stu-id="d7f82-179">Requirement</span></span> | <span data-ttu-id="d7f82-180">值</span><span class="sxs-lookup"><span data-stu-id="d7f82-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7f82-181">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d7f82-181">Minimum supported client</span></span><br/> | <span data-ttu-id="d7f82-182">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7f82-182">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d7f82-183">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d7f82-183">Minimum supported server</span></span><br/> | <span data-ttu-id="d7f82-184">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7f82-184">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="d7f82-185">DLL</span><span class="sxs-lookup"><span data-stu-id="d7f82-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7f82-186"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="d7f82-186"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7f82-187">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d7f82-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7f82-188">**Shell 物件**</span><span class="sxs-lookup"><span data-stu-id="d7f82-188">**Shell Object**</span></span>](shell.md)
</dt> </dl>

 

 




