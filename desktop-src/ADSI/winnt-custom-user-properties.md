---
title: WinNT 自訂使用者屬性
description: WinNT 提供者可提供下列使用者類別的自訂屬性。 您可以透過 IADs 和 IADs 來存取它們。 Put 方法。 如需詳細資訊，請參閱使用者 \_ 資訊 \_ 3 結構。
ms.assetid: 3b122424-ff24-4de7-bdaf-693fb4529b09
ms.tgt_platform: multiple
keywords:
- WinNT 自訂使用者屬性 ADSI
- WinNT 提供者 ADSI、使用者物件、自訂屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95230de6f7bb5bd848d7a8a047c0ec1966e5a67e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103933615"
---
# <a name="winnt-custom-user-properties"></a><span data-ttu-id="c694e-107">WinNT 自訂使用者屬性</span><span class="sxs-lookup"><span data-stu-id="c694e-107">WinNT Custom User Properties</span></span>

<span data-ttu-id="c694e-108">WinNT 提供者可提供下列使用者類別的自訂屬性。</span><span class="sxs-lookup"><span data-stu-id="c694e-108">The WinNT provider makes available the following custom properties for the User class.</span></span> <span data-ttu-id="c694e-109">您可以透過 [**IADs**](/windows/desktop/api/Iads/nf-iads-iads-get) 和 IADs 來存取它們。 [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put) 方法。</span><span class="sxs-lookup"><span data-stu-id="c694e-109">They may be accessed through the [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) and [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) methods.</span></span> <span data-ttu-id="c694e-110">如需詳細資訊，請參閱 [**使用者 \_ 資訊 \_ 3**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_3) 結構。</span><span class="sxs-lookup"><span data-stu-id="c694e-110">For more information, see the [**USER\_INFO\_3**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_3) structure.</span></span>



| <span data-ttu-id="c694e-111">屬性</span><span class="sxs-lookup"><span data-stu-id="c694e-111">Property</span></span>            | <span data-ttu-id="c694e-112">類型</span><span class="sxs-lookup"><span data-stu-id="c694e-112">Type</span></span>         | <span data-ttu-id="c694e-113">Description</span><span class="sxs-lookup"><span data-stu-id="c694e-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c694e-114">**HomeDirDrive**</span><span class="sxs-lookup"><span data-stu-id="c694e-114">**HomeDirDrive**</span></span>    | <span data-ttu-id="c694e-115">String</span><span class="sxs-lookup"><span data-stu-id="c694e-115">String</span></span>       | <span data-ttu-id="c694e-116">使用者的主目錄磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="c694e-116">Home Directory Drive of the user.</span></span> <span data-ttu-id="c694e-117">這是指定主目錄路徑的 Unicode 字串指標。</span><span class="sxs-lookup"><span data-stu-id="c694e-117">This is a pointer to a Unicode string that specifies the path of the home directory.</span></span> <span data-ttu-id="c694e-118">字串可以是 **null**。</span><span class="sxs-lookup"><span data-stu-id="c694e-118">The string can be **null**.</span></span> <span data-ttu-id="c694e-119">請參閱本主題中的範例。</span><span class="sxs-lookup"><span data-stu-id="c694e-119">See example in this topic.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="c694e-120">**ObjectSID**</span><span class="sxs-lookup"><span data-stu-id="c694e-120">**ObjectSID**</span></span>       | <span data-ttu-id="c694e-121">八位字串</span><span class="sxs-lookup"><span data-stu-id="c694e-121">Octet String</span></span> | <span data-ttu-id="c694e-122">使用者的物件 SID。</span><span class="sxs-lookup"><span data-stu-id="c694e-122">Object SID of the user.</span></span> <span data-ttu-id="c694e-123">如需如何使用 WinNT 提供者來取得物件 SID 的範例，請參閱 [ (WinNT 提供者的物件 sid) ](object-sid.md)</span><span class="sxs-lookup"><span data-stu-id="c694e-123">For an example of how to retrieve the Object SID using the WinNT Provider, see [Object SID (WinNT Provider)](object-sid.md)</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="c694e-124">**參數**</span><span class="sxs-lookup"><span data-stu-id="c694e-124">**Parameters**</span></span>      | <span data-ttu-id="c694e-125">String</span><span class="sxs-lookup"><span data-stu-id="c694e-125">String</span></span>       | <span data-ttu-id="c694e-126">使用者的參數。</span><span class="sxs-lookup"><span data-stu-id="c694e-126">Parameters of the user.</span></span> <span data-ttu-id="c694e-127">指向保留給應用程式使用的 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="c694e-127">Points to a Unicode string that is set aside for use by applications.</span></span> <span data-ttu-id="c694e-128">這個字串可以是 null 字串，也可以在終止的 null 字元之前有任意數目的字元。</span><span class="sxs-lookup"><span data-stu-id="c694e-128">This string can be a null string, or it can have any number of characters before the terminating null character.</span></span> <span data-ttu-id="c694e-129">Microsoft 產品會使用這個成員來儲存使用者設定資料。</span><span class="sxs-lookup"><span data-stu-id="c694e-129">Microsoft products use this member to store user configuration data.</span></span> <span data-ttu-id="c694e-130">這個屬性只能由應用程式在安裝期間修改。</span><span class="sxs-lookup"><span data-stu-id="c694e-130">This property can only be modified by an application during installation.</span></span> |
| <span data-ttu-id="c694e-131">**PasswordAge**</span><span class="sxs-lookup"><span data-stu-id="c694e-131">**PasswordAge**</span></span>     | <span data-ttu-id="c694e-132">Time</span><span class="sxs-lookup"><span data-stu-id="c694e-132">Time</span></span>         | <span data-ttu-id="c694e-133">使用中密碼的時間長度。</span><span class="sxs-lookup"><span data-stu-id="c694e-133">Time duration of the password in use.</span></span> <span data-ttu-id="c694e-134">這個屬性工作表示自上次變更密碼以來經過的秒數。</span><span class="sxs-lookup"><span data-stu-id="c694e-134">This property indicates the number of seconds that have elapsed since the password was last changed.</span></span>                                                                                                                                                                                                                    |
| <span data-ttu-id="c694e-135">**PasswordExpired**</span><span class="sxs-lookup"><span data-stu-id="c694e-135">**PasswordExpired**</span></span> | <span data-ttu-id="c694e-136">整數</span><span class="sxs-lookup"><span data-stu-id="c694e-136">Integer</span></span>      | <span data-ttu-id="c694e-137">告知密碼到期的時間。</span><span class="sxs-lookup"><span data-stu-id="c694e-137">Tells when the password was expired.</span></span> <span data-ttu-id="c694e-138">當您使用 Get 時，它會傳回零，也就是密碼已過期，或非零。</span><span class="sxs-lookup"><span data-stu-id="c694e-138">When you use Get, it will return zero is the password has not expired, or nonzero if it has expired.</span></span> <span data-ttu-id="c694e-139">請參閱本主題中的範例。</span><span class="sxs-lookup"><span data-stu-id="c694e-139">See example in this topic.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="c694e-140">**PrimaryGroupID**</span><span class="sxs-lookup"><span data-stu-id="c694e-140">**PrimaryGroupID**</span></span>  | <span data-ttu-id="c694e-141">整數</span><span class="sxs-lookup"><span data-stu-id="c694e-141">Integer</span></span>      | <span data-ttu-id="c694e-142">使用者的主要群組識別碼，例如網域使用者群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="c694e-142">User's primary group ID, for example, domain user group ID.</span></span> <span data-ttu-id="c694e-143">請參閱本主題中的範例。</span><span class="sxs-lookup"><span data-stu-id="c694e-143">See example in this topic.</span></span>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="c694e-144">**UserFlags**</span><span class="sxs-lookup"><span data-stu-id="c694e-144">**UserFlags**</span></span>       | <span data-ttu-id="c694e-145">整數</span><span class="sxs-lookup"><span data-stu-id="c694e-145">Integer</span></span>      | <span data-ttu-id="c694e-146">在 [**ADS \_ 使用者 \_ 旗標 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum)中定義的使用者旗標。</span><span class="sxs-lookup"><span data-stu-id="c694e-146">User Flag defined in [**ADS\_USER\_FLAG\_ENUM**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum).</span></span> <span data-ttu-id="c694e-147">如需如何使用 UserFlags 的範例，請參閱 [密碼永遠不會過期 (WinNT 提供者) ](winnt-password-never-expires.md)</span><span class="sxs-lookup"><span data-stu-id="c694e-147">For an example of how to use UserFlags, see [Password Never Expires (WinNT Provider)](winnt-password-never-expires.md)</span></span>                                                                                                                                                             |



 

<span data-ttu-id="c694e-148">此範例顯示如何設定使用者的主要磁碟磁碟機目錄。</span><span class="sxs-lookup"><span data-stu-id="c694e-148">This example shows how to set a user's Home Drive Directory.</span></span>


```VB
Dim usr As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user") 
usr.HomeDirectory = "UserHomeDirHere"
usr.HomeDirDrive = "HomeDirDriveHere"
usr.SetInfo
```



<span data-ttu-id="c694e-149">此範例示範如何使用 PasswordExpired 來強制使用者在下次登入時變更密碼。</span><span class="sxs-lookup"><span data-stu-id="c694e-149">This example shows how to use PasswordExpired to force a user to change the password at the next logon.</span></span>


```VB
Dim usr As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user")
usr.Put "PasswordExpired", CLng(1)
usr.SetInfo 

'--- Clear this flag so that the user does not have to change the password at next logon.

usr.Put "PasswordExpired", CLng(0)
usr.SetInfo
```



<span data-ttu-id="c694e-150">此範例顯示如何取得使用者的主要群組。</span><span class="sxs-lookup"><span data-stu-id="c694e-150">This example shows how to get the user's primary group.</span></span>


```VB
Dim usr As Object
Dim grpPrimaryID As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user") 
grpPrimaryID = usr.Get("PrimaryGroupID")
```



 

 