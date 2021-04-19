---
description: Win32 \_ SystemAccount&\# 8194;WMI 類別代表系統帳戶。
ms.assetid: 0f745d93-cbac-428e-bf27-56f6e97d529f
ms.tgt_platform: multiple
title: Win32_SystemAccount 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemAccount
- Win32_SystemAccount.Caption
- Win32_SystemAccount.Description
- Win32_SystemAccount.InstallDate
- Win32_SystemAccount.Status
- Win32_SystemAccount.LocalAccount
- Win32_SystemAccount.SID
- Win32_SystemAccount.SIDType
- Win32_SystemAccount.Domain
- Win32_SystemAccount.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1ef246a0ee372c5755aeb30980095e7f2f6ca1dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972571"
---
# <a name="win32_systemaccount-class"></a>Win32 \_ SystemAccount 類別

**Win32 \_ SystemAccount** [WMI 類別](../wmisdk/retrieving-a-class.md)代表系統帳戶。 系統帳戶是由作業系統和服務所使用。 Windows 中有許多服務和進程需要在內部登入，例如在 Windows 安裝期間。 系統帳戶是針對該目的所設計。

系統帳戶是未顯示在使用者管理員中的內部帳戶，無法新增至任何群組，也無法將使用者權限指派給該帳戶。 不過，系統帳戶會顯示在 [檔案管理員] 中的 NTFS 檔案系統磁片區，該磁片區位於 [安全性] 功能表的 [許可權] 區段中。 根據預設，系統帳戶會被授與 NTFS 檔案系統磁片區上所有檔案的完整控制權，這表示系統帳戶具有與系統管理員帳戶相同的功能許可權。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性和方法是以字母順序排列，而不是 MOF 順序。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CA-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemAccount : Win32_Account
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  boolean  LocalAccount;
  string   SID;
  uint8    SIDType;
  string   Domain;
  string   Name;
};
```

## <a name="members"></a>成員

**Win32 \_ SystemAccount** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ SystemAccount** 類別具有這些屬性。

<dl> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) ， [**DisplayName**](../wmisdk/standard-qualifiers.md) ( "Caption" ) 
</dt> </dl>

物件的簡短文字描述。

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

物件的文字描述。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**網域**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "Domain" ) ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Network Management 函數 \| domainname" ) 
</dt> </dl>

系統帳戶所屬之 Windows 網域的名稱。

範例： "NA-SALES"

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](../wmisdk/standard-qualifiers.md) (" 安裝日期 ") 
</dt> </dl>

指出物件的安裝時間。 缺少值並不表示物件未安裝。

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

若 **為 TRUE**，則會在本機電腦上定義帳戶。 若只要取出本機電腦上定義的帳戶，請設計包含 "LocalAccount =**TRUE**" 條件的查詢。

這個屬性是從 [**Win32 \_ 帳戶**](win32-account.md)繼承而來的。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "Name" ) ， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Network Management 結構 \| 名稱" ) 
</dt> </dl>

此類別的 **domain** 屬性所指定之網域上的 Windows 系統帳戶名稱。

</dd> <dt>

**SID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Fixed**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Security 識別碼 (sid) " ) 
</dt> </dl>

此帳戶 (SID) 的安全識別碼。 SID 是變數長度的字串值，用來識別信任者。 每個帳戶都有一個由授權單位所發行的唯一 SID (例如儲存在安全性資料庫中的 Windows 網域) 。 當使用者登入時，系統會從資料庫抓取使用者的 SID，並將其放在使用者的存取權杖中。 系統會在使用者的存取權杖中使用 SID，以在所有後續與 Windows 安全性的互動中識別使用者。 使用 SID 做為使用者或群組的唯一識別碼時，無法再次使用它來識別另一個使用者或群組。

這個屬性是從 [**Win32 \_ 帳戶**](win32-account.md)繼承而來的。

</dd> <dt>

**SIDType**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Fixed**](../wmisdk/standard-wmi-qualifiers.md)， [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| 存取控制列舉類型 \| SID \_ 名稱 \_ 使用" ) 
</dt> </dl>

列舉值，指定 (SID) 的安全識別碼類型。

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

表示物件目前狀態的字串。 您可以定義操作和非運作狀態。 操作狀態可以包含「確定」、「降級」和「Pred 失敗」。 「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。

非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。 「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。 並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。

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

**Win32 \_ SystemAccount** 類別衍生自 [**win32 \_ 帳戶**](win32-account.md)。

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

 

 
