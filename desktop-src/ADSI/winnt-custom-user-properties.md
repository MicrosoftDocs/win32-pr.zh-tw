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
# <a name="winnt-custom-user-properties"></a>WinNT 自訂使用者屬性

WinNT 提供者可提供下列使用者類別的自訂屬性。 您可以透過 [**IADs**](/windows/desktop/api/Iads/nf-iads-iads-get) 和 IADs 來存取它們。 [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put) 方法。 如需詳細資訊，請參閱 [**使用者 \_ 資訊 \_ 3**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_3) 結構。



| 屬性            | 類型         | Description                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HomeDirDrive**    | String       | 使用者的主目錄磁片磁碟機。 這是指定主目錄路徑的 Unicode 字串指標。 字串可以是 **null**。 請參閱本主題中的範例。                                                                                                                                                                                 |
| **ObjectSID**       | 八位字串 | 使用者的物件 SID。 如需如何使用 WinNT 提供者來取得物件 SID 的範例，請參閱 [ (WinNT 提供者的物件 sid) ](object-sid.md)                                                                                                                                                                                                          |
| **參數**      | String       | 使用者的參數。 指向保留給應用程式使用的 Unicode 字串。 這個字串可以是 null 字串，也可以在終止的 null 字元之前有任意數目的字元。 Microsoft 產品會使用這個成員來儲存使用者設定資料。 這個屬性只能由應用程式在安裝期間修改。 |
| **PasswordAge**     | Time         | 使用中密碼的時間長度。 這個屬性工作表示自上次變更密碼以來經過的秒數。                                                                                                                                                                                                                    |
| **PasswordExpired** | 整數      | 告知密碼到期的時間。 當您使用 Get 時，它會傳回零，也就是密碼已過期，或非零。 請參閱本主題中的範例。                                                                                                                                                                                          |
| **PrimaryGroupID**  | 整數      | 使用者的主要群組識別碼，例如網域使用者群組識別碼。 請參閱本主題中的範例。                                                                                                                                                                                                                                                                        |
| **UserFlags**       | 整數      | 在 [**ADS \_ 使用者 \_ 旗標 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum)中定義的使用者旗標。 如需如何使用 UserFlags 的範例，請參閱 [密碼永遠不會過期 (WinNT 提供者) ](winnt-password-never-expires.md)                                                                                                                                                             |



 

此範例顯示如何設定使用者的主要磁碟磁碟機目錄。


```VB
Dim usr As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user") 
usr.HomeDirectory = "UserHomeDirHere"
usr.HomeDirDrive = "HomeDirDriveHere"
usr.SetInfo
```



此範例示範如何使用 PasswordExpired 來強制使用者在下次登入時變更密碼。


```VB
Dim usr As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user")
usr.Put "PasswordExpired", CLng(1)
usr.SetInfo 

'--- Clear this flag so that the user does not have to change the password at next logon.

usr.Put "PasswordExpired", CLng(0)
usr.SetInfo
```



此範例顯示如何取得使用者的主要群組。


```VB
Dim usr As Object
Dim grpPrimaryID As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user") 
grpPrimaryID = usr.Get("PrimaryGroupID")
```



 

 