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
# <a name="didiskquotauser-object"></a>DIDiskQuotaUser 物件

允許用戶端管理 NTFS 磁片區的全域磁片配額設定。 這個物件讓 **DIDiskQuotaUser** 介面的基本功能可供腳本和 Microsoft Visual Basic 應用程式使用。

## <a name="members"></a>成員

**DIDiskQuotaUser** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**DIDiskQuotaUser** 物件有這些方法。



| 方法                                           | 描述                                             |
|:-------------------------------------------------|:--------------------------------------------------------|
| [**無效**](didiskquotauser-invalidate.md) | 清除物件的快取使用者資訊。<br/> |



 

### <a name="properties"></a>屬性

**DIDiskQuotaUser** 物件具有這些屬性。



| 屬性                                                                        | 存取類型           | 描述                                                                                          |
|:--------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------|
| [**AccountContainerName**](didiskquotauser-accountcontainername.md)<br/> | 唯讀<br/>  | 取得使用者帳戶容器的名稱。<br/>                                            |
| [**AccountStatus**](didiskquotauser-accountstatus.md)<br/>               | 唯讀<br/>  | 取得使用者帳戶的狀態。<br/>                                                    |
| [**DisplayName**](didiskquotauser-displayname.md)<br/>                   | 唯讀<br/>  | 取得使用者的顯示名稱。<br/>                                                             |
| [**識別碼**](didiskquotauser-id.md)<br/>                                     | 唯讀<br/>  | 取得可唯一識別使用者的識別碼。<br/>                                             |
| [**LogonName**](didiskquotauser-logonname.md)<br/>                       | 唯讀<br/>  | 取得使用者的登入帳戶名稱。<br/>                                                       |
| [**QuotaLimit**](didiskquotauser-quotalimit.md)<br/>                     | 讀取/寫入<br/> | 設定或取得使用者目前的 [**配額限制**](diskquotacontrol-object.md)。<br/>           |
| [**QuotaLimitText**](didiskquotauser-quotalimittext.md)<br/>             | 唯讀<br/>  | 取得使用者目前的 [**配額限制**](diskquotacontrol-object.md) ，作為文字字串。 <br/> |
| [**QuotaThreshold**](didiskquotauser-quotathreshold.md)<br/>             | 讀取/寫入<br/> | 設定或取得使用者的警告臨界值（以位元組為單位）。<br/>                                      |
| [**QuotaThresholdText**](didiskquotauser-quotathresholdtext.md)<br/>     | 唯讀<br/>  | 取得使用者的警告臨界值做為文字字串。<br/>                                       |
| [**QuotaUsed**](didiskquotauser-quotaused.md)<br/>                       | 唯讀<br/>  | 取得使用者目前的磁片使用量（以位元組為單位）。<br/>                                             |
| [**QuotaUsedText**](didiskquotauser-quotausedtext.md)<br/>               | 唯讀<br/>  | 以文字字串形式取得使用者的目前磁片使用量。<br/>                                      |



 

## <a name="remarks"></a>備註

[**DiskQuotaControl**](diskquotacontrol-object.md)物件所管理之磁片區上的每個使用者都有與其相關聯的 **DIDiskQuotaUser** 物件。 此物件可讓用戶端管理個別使用者的設定。 有幾種方式可以取得使用者的 **DIDiskQuotaUser** 物件：

-   具有磁片區配額之所有使用者的 **DIDiskQuotaUser** 物件會公開為集合，而且可以列舉。 有關如何列舉 **DIDiskQuotaUser** 物件的討論，請參閱下面。
-   當您加入新的使用者時， [**AddUser**](diskquotacontrol-adduser.md) 方法會傳回使用者的 **DIDiskQuotaUser** 物件。
-   如果您有使用者的名稱， [**FindUser**](diskquotacontrol-finduser.md) 方法會傳回使用者的 **DIDiskQuotaUser** 物件。

### <a name="enumerating-disk-quota-users"></a>列舉磁片配額使用者

具有磁片區配額之所有使用者的 **DIDiskQuotaUser** 物件會公開為集合。 [**DiskQuotaControl**](diskquotacontrol-object.md)物件會匯出標準的枚舉器方法，可讓您列舉 **DIDiskQuotaUser** 物件的集合。 下列程式說明如何使用 Microsoft JScript 執行列舉， (與 ECMA 262 語言規格) 相容。 您可以使用類似的程式與 Visual Basic 或 Microsoft Visual Basic Scripting Edition (VBScript) 。

1.  建立新的 [**DiskQuotaControl**](diskquotacontrol-object.md) 物件。
2.  使用 [**initialize**](diskquotacontrol-initialize.md)將它初始化。
3.  建立新的 JScript **列舉** 值物件。
4.  使用 **for** 迴圈來列舉 **DIDiskQuotaUser** 物件。 不需要設定起始值。 列舉值物件的 **moveNext** 方法會通知 **專案** 方法傳回下一個 **DIDiskQuotaUser** 物件。 當您到達清單結尾時， **atEnd** 方法會傳回 **false** 。
5.  如有需要，請使用列舉值之 **item** 方法所傳回的 **DIDiskQuotaUser** 物件，以抓取或設定一或多個相關聯的使用者磁片配額屬性。

下列程式碼片段說明如何使用 JScript 列舉 **DIDiskQuotaUser** 物件。 傳遞至 **EnumUsers** 函數的 **磁片區卷 \_ 標** 引數是包含磁片區標籤（例如 "C："）的字串值 \\ \\ 。


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



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (5.0 版或更新版本) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Shell 物件**](shell.md)
</dt> </dl>

 

 




