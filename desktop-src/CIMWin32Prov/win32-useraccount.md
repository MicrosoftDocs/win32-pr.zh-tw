---
description: Win32 \_ UserAccount&\# 32;WMI 類別包含執行 Windows 之電腦系統上的使用者帳戶的相關資訊。
ms.assetid: 747b2ce2-ae38-47de-bf3a-97058df56a7a
ms.tgt_platform: multiple
title: Win32_UserAccount 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_UserAccount
- Win32_UserAccount.AccountType
- Win32_UserAccount.Caption
- Win32_UserAccount.Description
- Win32_UserAccount.Disabled
- Win32_UserAccount.Domain
- Win32_UserAccount.FullName
- Win32_UserAccount.InstallDate
- Win32_UserAccount.LocalAccount
- Win32_UserAccount.Lockout
- Win32_UserAccount.Name
- Win32_UserAccount.PasswordChangeable
- Win32_UserAccount.PasswordExpires
- Win32_UserAccount.PasswordRequired
- Win32_UserAccount.SID
- Win32_UserAccount.SIDType
- Win32_UserAccount.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: df907b1686677db8ea895d8788055567e24dc7be7ffe758bcfa82801591a0dfb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922748"
---
# <a name="win32_useraccount-class"></a>Win32 \_ UserAccount 類別

**Win32 \_ UserAccount** [WMI 類別](../wmisdk/retrieving-a-class.md)包含執行 Windows 之電腦系統上的使用者帳戶的相關資訊。

> [!Note]  
> 由於 **名稱** 和 **網域** 都是索引鍵屬性，因此在大型網路上列舉 **Win32 \_ UserAccount** 可能會對效能造成負面影響。 呼叫 **GetObject** 或查詢特定實例的影響較小。

 

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性和方法是以字母順序排列，而不是 MOF 順序。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CC-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_UserAccount : Win32_Account
{
  uint32   AccountType;
  string   Caption;
  string   Description;
  boolean  Disabled;
  string   Domain;
  string   FullName;
  datetime InstallDate;
  boolean  LocalAccount;
  boolean  Lockout;
  string   Name;
  boolean  PasswordChangeable;
  boolean  PasswordExpires;
  boolean  PasswordRequired;
  string   SID;
  uint8    SIDType;
  string   Status;
};
```

## <a name="members"></a>成員

**Win32 \_ UserAccount** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 \_ UserAccount** 類別具有這些方法。



| 方法                                                     | 描述                                             |
|:-----------------------------------------------------------|:--------------------------------------------------------|
| [**重新命名**](rename-method-in-class-win32-useraccount.md) | 允許重新命名使用者帳戶。<br/> |



 

### <a name="properties"></a>屬性

**Win32 \_ UserAccount** 類別具有這些屬性。

<dl> <dt>

**AccountType**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| usri2 \_ 旗標」 ) 
</dt> </dl>

描述 Windows 使用者帳戶特性的旗標。

<dt>

<span id="Temporary_duplicate_account"></span><span id="temporary_duplicate_account"></span><span id="TEMPORARY_DUPLICATE_ACCOUNT"></span>

<span id="Temporary_duplicate_account"></span><span id="temporary_duplicate_account"></span><span id="TEMPORARY_DUPLICATE_ACCOUNT"></span>**暫時重複的帳戶** (256) 


</dt> <dd>

**UF \_ 暫存 \_ 重複 \_ 帳戶**

在另一個網域中具有主要帳戶之使用者的本機使用者帳戶。 此帳戶僅提供此網域的使用者存取權，而不是信任此網域的任何網域。

</dd> <dt>

<span id="Normal_account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>

<span id="Normal_account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>**一般帳戶** (512) 


</dt> <dd>

**UF \_ 一般 \_ 帳戶**

代表一般使用者的預設帳戶類型。

</dd> <dt>

<span id="Interdomain_trust_account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>

<span id="Interdomain_trust_account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span> (2048) 的 **域間信任帳戶**


</dt> <dd>

**每個 UF \_ 域 \_ 信任 \_ 帳戶**

適用于信任其他網域之系統網域的帳戶。

</dd> <dt>

<span id="Workstation_trust_account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>

<span id="Workstation_trust_account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>**工作站信任帳戶** (4096) 


</dt> <dd>

**UF \_ 工作站 \_ 信任 \_ 帳戶**

電腦系統的電腦帳戶，執行的 Windows 是此網域的成員。

</dd> <dt>

<span id="Server_trust_account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>

<span id="Server_trust_account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>**伺服器信任帳戶** (8192) 


</dt> <dd>

**UF \_ 伺服器 \_ 信任 \_ 帳戶**

屬於此網域成員的系統備份網域控制站帳戶。

</dd> </dl>

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) 
</dt> </dl>

帳戶的網域和使用者名稱。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Description" ) 
</dt> </dl>

帳戶的描述。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**停用**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| 使用者 \_ 資訊 \| UF \_ ACCOUNTDISABLE」 ) 
</dt> </dl>

Windows 使用者帳戶已停用。

</dd> <dt>

**網域**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "Domain" ) ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Network Management 函數 \| domainname" ) 
</dt> </dl>

使用者帳戶所屬 Windows 網域的名稱，例如： "NA-SALES"。

</dd> <dt>

**FullName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Network Management 結構 \| [**USER \_ INFO \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2) \| **usri2 \_ full \_ name**" ) 
</dt> </dl>

本機使用者的完整名稱，例如：「Dan Wilson」。

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") 
</dt> </dl>

物件的安裝日期。 這個屬性不需要值來表示已安裝物件。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**LocalAccount**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：已 [**修正**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

若 **為 true**，則會在本機電腦上定義帳戶。

這個屬性是從 [**Win32 \_ 帳戶**](win32-account.md)繼承而來的。

</dd> <dt>

**鎖定**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)的 \| **UF \_ 鎖定**」 ) 
</dt> </dl>

若 **為 true**，則會將使用者帳戶鎖定 Windows 作業系統。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "Name" ) ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Network Management 結構 \| 名稱" ) 
</dt> </dl>

此類別的 **網域** 屬性指定之網域上 Windows 使用者帳戶的名稱。

範例： "danwilson"。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**PasswordChangeable**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)個 \| **UF \_ 密碼無法 \_ \_ 變更**」 ) 
</dt> </dl>

若 **為 true**，則可以變更此使用者帳戶的密碼。

</dd> <dt>

**PasswordExpires**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)的 \| **UF 未 \_ \_ 過期 \_**」 ) 
</dt> </dl>

若 **為 true**，則表示此使用者帳戶的密碼已過期。

</dd> <dt>

**PasswordRequired**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 2**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_2)個 \| **UF \_ 密碼 \_ NOTREQD**」 ) 
</dt> </dl>

若 **為 true**，則 Windows 使用者帳戶上需要有密碼。 如果 **為 false**，則此帳戶不需要密碼。

</dd> <dt>

**SID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Fixed**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Security 識別碼 (sid) " ) 
</dt> </dl>

此帳戶 (SID) 的安全識別碼。 SID 是變數長度的字串值，可用來識別信任者。 每個帳戶都有一個唯一的 SID，例如 Windows 網域的問題。 SID 會儲存在安全性資料庫中。 當使用者登入時，系統會從資料庫抓取使用者 sid、將 sid 放在使用者存取權杖中，然後使用使用者存取權杖中的 sid 來識別與 Windows 安全性的所有後續互動中的使用者。 每個 SID 都是使用者或群組的唯一識別碼，而且不同的使用者或群組不能有相同的 SID。

這個屬性是從 [**Win32 \_ 帳戶**](win32-account.md)繼承而來的。

</dd> <dt>

**SIDType**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Fixed**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 存取控制列舉類型 \| [**SID \_ 名稱 \_ 使用**](/windows/win32/api/winnt/ne-winnt-sid_name_use)" ) 
</dt> </dl>

指定 SID 類型的列舉值。

這個屬性是從 [**Win32 \_ 帳戶**](win32-account.md)繼承而來的。

<dt>

<span id="SidTypeUser"></span><span id="sidtypeuser"></span><span id="SIDTYPEUSER"></span>

**SidTypeUser** (1) 


</dt> <dd></dd> <dt>

<span id="SidTypeGroup"></span><span id="sidtypegroup"></span><span id="SIDTYPEGROUP"></span>

**SidTypeGroup** (2) 


</dt> <dd></dd> <dt>

<span id="SidTypeDomain"></span><span id="sidtypedomain"></span><span id="SIDTYPEDOMAIN"></span>

**SidTypeDomain** (3) 


</dt> <dd></dd> <dt>

<span id="SidTypeAlias"></span><span id="sidtypealias"></span><span id="SIDTYPEALIAS"></span>

**SidTypeAlias** (4) 


</dt> <dd></dd> <dt>

<span id="SidTypeWellKnownGroup"></span><span id="sidtypewellknowngroup"></span><span id="SIDTYPEWELLKNOWNGROUP"></span>

**SidTypeWellKnownGroup** (5) 


</dt> <dd></dd> <dt>

<span id="SidTypeDeletedAccount"></span><span id="sidtypedeletedaccount"></span><span id="SIDTYPEDELETEDACCOUNT"></span>

**SidTypeDeletedAccount** (6) 


</dt> <dd></dd> <dt>

<span id="SidTypeInvalid"></span><span id="sidtypeinvalid"></span><span id="SIDTYPEINVALID"></span>

**SidTypeInvalid** (7) 


</dt> <dd></dd> <dt>

<span id="SidTypeUnknown"></span><span id="sidtypeunknown"></span><span id="SIDTYPEUNKNOWN"></span>

**SidTypeUnknown** (8) 


</dt> <dd></dd> <dt>

<span id="SidTypeComputer"></span><span id="sidtypecomputer"></span><span id="SIDTYPECOMPUTER"></span>

**SidTypeComputer** (9) 


</dt> <dd></dd> </dl>

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (10) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Status" ) 
</dt> </dl>

物件的目前狀態。 您可以定義各種操作和 nonoperational 狀態。 作業狀態包括：「確定」、「降級」和「Pred 失敗」，這是一種元素，例如可正常運作的智慧型硬碟，但在不久的未來會預測失敗。 Nonoperational 狀態包括：「錯誤」、「開始」、「停止」和「服務」，這可在磁片的鏡像重新同步處理期間套用、重載使用者權限清單或其他系統管理工作。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

包括下列值：

<dt>

<span id="OK"></span><span id="ok"></span>

**確定** ( [確定] ) 


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**錯誤** ( 「錯誤」 ) 


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**降級** ( 「降級」 ) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 ( 「未知」 ) 


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred 失敗** ( 「Pred 失敗」 ) 


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**開始** ( 「開始」 ) 


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**停止** ( 「正在停止」 ) 


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**服務** ( 「服務」 ) 


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**壓力** ( 「壓力」 ) 


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ( "NonRecover" ) 


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**沒有連絡人** ( 「沒有連絡人」 ) 


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**遺失的 comm** ( 「遺失的通訊」 ) 


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ UserAccount** 類別衍生自 [**win32 \_ 帳戶**](win32-account.md)。

> [!Note]  
> 嘗試寫入唯讀屬性時，不會傳回錯誤，而且屬性的值會維持不變。

 

## <a name="examples"></a>範例

在 TechNet 資源庫上使用 WMI VBScript 程式碼範例 [列出本機使用者帳戶](https://Gallery.TechNet.Microsoft.Com/827623f5-eb55-4035-8f57-25c4afb444cd) ，會使用 **Win32 \_ UserAccount** 來傳回在電腦上找到的本機使用者帳戶的相關資訊。

將 [Sid 轉換為使用者帳戶，並將使用者帳戶轉換為 sid](https://Gallery.TechNet.Microsoft.Com/f1c83aed-fe60-48d5-90ab-22388fcbd54f)TechNet 資源庫上的 PowerShell 程式碼範例會使用 **Win32 \_ UserAccount** ，將 Sid 轉譯為使用者帳戶和/或使用者帳戶至 sid。

下列 VBScript 程式碼範例會示範如何在本機電腦上取得使用者的完整名稱。 全名是人類的語言名稱，例如，一個人可以有 "kensanchez" 的使用者名稱，而全名可能是 "Ken Sanchez"，所以您可以用真實的功能變數名稱和使用者名稱取代 "MyDomainName" 和 "MyUserName"。 針對有效率的查詢，您必須同時指定 [網域] 和 [使用者名稱] 屬性。

如果您是遠端電腦上的系統管理員，您可以指派 strComputer (的遠端電腦名稱稱，而不是 ".") ，然後使用下列腳本類型，從遠端電腦取得本機電腦上的使用者帳戶的完整名稱。


```VB
On Error Resume Next
strComputer = "."

Set objUserAccount = GetObject("winmgmts{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\cimv2:Win32_UserAccount.Domain='MyDomainName',Name='MyUserName' ")

If Err = 0 Then
    WScript.Echo objUserAccount.FullName
Else
    WScript.Echo "No object found" & Err.Number
End If
```




```CSharp
using System.Management;

{
     ManagementScope mgmtScope = new ManagementScope("\\\\.\\Root\\CIMv2");
     ObjectQuery oQuery = new ObjectQuery("SELECT * FROM Win32_UserAccount Where Name=\"myUserName\"");
     ManagementObjectSearcher mgmtSearch = new ManagementObjectSearcher(mgmtScope, oQuery);
     ManagementObjectCollection objCollection = mgmtSearch.Get();
     foreach (ManagementObject mgmtObject in objCollection)
     {
          Console.WriteLine("Full Name : {0}", mgmtObject["FullName"]);
     }
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ 帳戶**](win32-account.md)
</dt> <dt>

[作業系統類別](./operating-system-classes.md)
</dt> </dl>

 

 
