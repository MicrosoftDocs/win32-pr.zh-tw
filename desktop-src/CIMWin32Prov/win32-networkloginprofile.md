---
description: Win32 \_ NetworkLoginProfile&\# 8194;WMI 類別代表執行 Windows 之電腦系統上特定使用者的網路登入資訊。
ms.assetid: e5a8e934-d5a7-43fa-b140-c3cca972590f
ms.tgt_platform: multiple
title: Win32_NetworkLoginProfile 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkLoginProfile
- Win32_NetworkLoginProfile.Caption
- Win32_NetworkLoginProfile.Description
- Win32_NetworkLoginProfile.SettingID
- Win32_NetworkLoginProfile.AccountExpires
- Win32_NetworkLoginProfile.AuthorizationFlags
- Win32_NetworkLoginProfile.BadPasswordCount
- Win32_NetworkLoginProfile.CodePage
- Win32_NetworkLoginProfile.Comment
- Win32_NetworkLoginProfile.CountryCode
- Win32_NetworkLoginProfile.Flags
- Win32_NetworkLoginProfile.FullName
- Win32_NetworkLoginProfile.HomeDirectory
- Win32_NetworkLoginProfile.HomeDirectoryDrive
- Win32_NetworkLoginProfile.LastLogoff
- Win32_NetworkLoginProfile.LastLogon
- Win32_NetworkLoginProfile.LogonHours
- Win32_NetworkLoginProfile.LogonServer
- Win32_NetworkLoginProfile.MaximumStorage
- Win32_NetworkLoginProfile.Name
- Win32_NetworkLoginProfile.NumberOfLogons
- Win32_NetworkLoginProfile.Parameters
- Win32_NetworkLoginProfile.PasswordAge
- Win32_NetworkLoginProfile.PasswordExpires
- Win32_NetworkLoginProfile.PrimaryGroupId
- Win32_NetworkLoginProfile.Privileges
- Win32_NetworkLoginProfile.Profile
- Win32_NetworkLoginProfile.ScriptPath
- Win32_NetworkLoginProfile.UnitsPerWeek
- Win32_NetworkLoginProfile.UserComment
- Win32_NetworkLoginProfile.UserId
- Win32_NetworkLoginProfile.UserType
- Win32_NetworkLoginProfile.Workstations
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4fb71b27093cb1011b9aebaadf0a6760124b64f9e13ae7b5ef46f5ffc478cce4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972647"
---
# <a name="win32_networkloginprofile-class"></a>Win32 \_ NetworkLoginProfile 類別

**Win32 \_ NetworkLoginProfile** [WMI 類別](../wmisdk/retrieving-a-class.md)代表執行 Windows 之電腦系統上特定使用者的網路登入資訊。 這包括但不限於密碼狀態、存取權限、磁片配額和登入目錄路徑。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C4E7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkLoginProfile : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  datetime AccountExpires;
  uint32   AuthorizationFlags;
  uint32   BadPasswordCount;
  uint32   CodePage;
  string   Comment;
  uint32   CountryCode;
  uint32   Flags;
  string   FullName;
  string   HomeDirectory;
  string   HomeDirectoryDrive;
  datetime LastLogoff;
  datetime LastLogon;
  string   LogonHours;
  string   LogonServer;
  uint64   MaximumStorage;
  string   Name;
  uint32   NumberOfLogons;
  string   Parameters;
  datetime PasswordAge;
  datetime PasswordExpires;
  uint32   PrimaryGroupId;
  uint32   Privileges;
  string   Profile;
  string   ScriptPath;
  uint32   UnitsPerWeek;
  string   UserComment;
  uint32   UserId;
  string   UserType;
  string   Workstations;
};
```

## <a name="members"></a>成員

**Win32 \_ NetworkLoginProfile** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ NetworkLoginProfile** 類別具有這些屬性。

<dl> <dt>

**AccountExpires**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ 帳戶 \_ 到期」 ) 
</dt> </dl>

帳戶將到期。 此值的計算方式是從00:00:00 年1月 1970 1 日起經過的秒數開始計算，並以下列格式設定： yyyymmddhhmmss.ffffff. mmmmmm sutc。

範例： 20521201000230.000000 000

</dd> <dt>

**AuthorizationFlags**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ auth \_ 旗標」 ) 、 [**BitValues**](../wmisdk/standard-qualifiers.md) ( 「印表機」、「通訊」、「伺服器」、「帳戶」 ) 
</dt> </dl>

一組旗標，指定使用者有權使用或修改的資源。

<dt>

1 (0x1) 
</dt> <dd>

印表機

</dd> <dt>

2 (0x2) 
</dt> <dd>

溝通

</dd> <dt>

4 (0x4) 
</dt> <dd>

伺服器

</dd> <dt>

8 (0x8) 
</dt> <dd>

帳戶

</dd> </dl>

</dd> <dt>

**BadPasswordCount**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Network Management 函數 \| NetUserEnum" ) 
</dt> </dl>

登入執行 Windows 的電腦系統時，使用者輸入錯誤密碼的次數。

範例：0

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (64) 
</dt> </dl>

目前物件的簡短文字描述。

這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。

</dd> <dt>

**CodePage**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ 代碼 \_ 頁」 ) 
</dt> </dl>

使用者選擇之語言的字碼頁。 字碼頁是使用的字元集。

</dd> <dt>

**註解**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ 批註」 ) 
</dt> </dl>

此登入設定檔的批註或描述。

</dd> <dt>

**CountryCode**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ country \_ code」 ) 
</dt> </dl>

使用者選擇之語言的國家/地區代碼。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

目前物件的文字描述。

這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。

</dd> <dt>

**旗標**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ 旗標」 ) ， [**BitMap**](../wmisdk/standard-qualifiers.md) ( "0"，"1"、"3"、"4"、"5"、"6"、"7"、"8"、"9"、"11"、"12"、"13"、"16"、"17"、"18"、"19"、"20"、"21"、"22"、"23" ) ， [**BitValues**](../wmisdk/standard-qualifiers.md) ( "Script"，"帳戶已停用"，"Home Dir Required"，"鎖定"，"不需要密碼"，"Paswword"，"無法變更"，「允許的加密測試密碼」，"Temp 重複的帳戶"，"Normal account"，"域信任帳戶"、「工作站信任帳戶」、「伺服器信任帳戶」、「不要過期密碼」、「MNS 登入帳戶」、「需要智慧卡」、「受信任的委派」、「未委派」、「僅使用 DES 金鑰」、「不需要 Preauthorization」、「密碼已過期」 ) 
</dt> </dl>

此網路設定檔可用的屬性。

可以設定的屬性包括：

<dt>

1 (0x1) 
</dt> <dd>

指令碼

執行的登入腳本。 必須為 LAN Manager 2.0 設定這個值。

</dd> <dt>

2 (0x2) 
</dt> <dd>

帳戶已停用

使用者的帳戶已停用。

</dd> <dt>

8 (0x8) 
</dt> <dd>

需要主目錄

需要主目錄。

</dd> <dt>

16 (0x10) 
</dt> <dd>

鎖定

帳戶目前已鎖定。若為 [**NetUserSetInfo**](/windows/win32/api/lmaccess/nf-lmaccess-netusersetinfo)，可以清除此值以解除鎖定先前鎖定的帳戶。 此值不能用來鎖定先前已解除鎖定的帳戶。

</dd> <dt>

32 (0x20) 
</dt> <dd>

不需要密碼

不需要密碼。

</dd> <dt>

64 (0x40) 
</dt> <dd>

密碼無法變更

使用者無法變更密碼。

</dd> <dt>

128 (0x80) 
</dt> <dd>

允許加密的測試密碼

</dd> <dt>

256 (0x100)
</dt> <dd>

暫存重複帳戶

其主要帳戶位於另一個網域的使用者帳戶。 此帳戶可讓使用者存取此網域，但不提供任何信任此網域的網域。 使用者管理員會將此帳戶類型稱為本機使用者帳戶。

</dd> <dt>

512 (0x200) 
</dt> <dd>

一般帳戶

代表一般使用者的預設帳戶類型。

</dd> <dt>

2048 (0x800) 
</dt> <dd>

限域信任帳戶

針對信任其他網域的網域允許信任帳戶。

</dd> <dt>

4096 (0x1000) 
</dt> <dd>

工作站信任帳戶

屬於此網域成員之 Windows 工作站或伺服器的電腦帳戶。

</dd> <dt>

8192 (0x2000) 
</dt> <dd>

伺服器信任帳戶

屬於此網域成員的備份網域控制站的電腦帳戶。

</dd> <dt>

65536 (0x10000) 
</dt> <dd>

不要過期密碼

</dd> <dt>

131072 (0x20000) 
</dt> <dd>

MNS 登入帳戶

多數節點集 (MNS) 登入帳戶類型，代表一則 MNS 使用者。

</dd> <dt>

262144 (0x40000) 
</dt> <dd>

需要智慧卡

</dd> <dt>

524288 (0x80000) 
</dt> <dd>

受信任以進行委派

</dd> <dt>

1048576 (0x100000) 
</dt> <dd>

未委派

</dd> <dt>

2097152 (0x200000) 
</dt> <dd>

僅使用 DES 金鑰

</dd> <dt>

4194304 (0x400000) 
</dt> <dd>

不需要 Preauthorization

</dd> <dt>

8388608 (0x800000) 
</dt> <dd>

密碼已過期

指出密碼已過期。

</dd> </dl>

下列屬性描述帳戶類型。 只能設定一個值：

-   UF \_ 一般 \_ 帳戶
-   UF \_ 暫存 \_ 重複 \_ 帳戶
-   UF \_ 工作站 \_ 信任 \_ 帳戶
-   UF \_ 伺服器 \_ 信任 \_ 帳戶
-   每個 UF \_ 域 \_ 信任 \_ 帳戶

</dd> <dt>

**FullName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Network Management 結構 \| [**USER \_ INFO \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ full \_ name" ) 
</dt> </dl>

屬於網路登入設定檔之使用者的完整名稱。 如果使用者選擇不將完整名稱與使用者名稱建立關聯，這個字串可以是空的。

</dd> <dt>

**HomeDirectory**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ home \_ dir」 ) 
</dt> </dl>

使用者主目錄的路徑。 如果使用者選擇不指定主目錄，此字串可能是空的。

範例： " \\ HOMEDIR"

</dd> <dt>

**HomeDirectoryDrive**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ home \_ dir \_ 磁片磁碟機」 ) 
</dt> </dl>

指派給使用者的主目錄以供登入之用的磁碟機號。

範例： "C："

</dd> <dt>

**LastLogoff**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ 上次 \_ 登出」 ) 
</dt> </dl>

使用者上次登出系統。 此值的計算是00:00:00 自1970年1月1日起經過的秒數。 值為 " \* \* \* \* \* \* \* \* \* \* \* \* \* \* . \* \* \* \* \* \* + \* \* \* " 表示最後一次登出時間是未知的。 此值的格式為 yyyymmddhhmmss.ffffff. mmmmmm sutc。 如需將此屬性轉譯為本地時間的詳細資訊，請參閱 [WMI 工作：日期和時間](../wmisdk/wmi-tasks--dates-and-times.md)。

範例： 19521201000230.000000 000

</dd> <dt>

**LastLogon**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ 上次 \_ 登入」 ) 
</dt> </dl>

使用者上次登入系統的時間。 此值的計算是00:00:00 自1970年1月1日起經過的秒數。 此值的格式為 yyyymmddhhmmss.ffffff. mmmmmm sutc。 如需將此屬性轉譯為本地時間的詳細資訊，請參閱 [WMI 工作：日期和時間](../wmisdk/wmi-tasks--dates-and-times.md)。

範例： 19521201000230.000000 000

</dd> <dt>

**LogonHours**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (147) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ 登入時數」 \_ ) 
</dt> </dl>

使用者可以登入的時間。 每個位代表 **UnitsPerWeek** 屬性指定的時間單位。 比方說，如果時間單位是每小時，第一個位 (位0，word 0) 是星期日、0:00 到0:59、第二個位 (bit 1、word 0) 是星期日、1:00 至1:59 等等。 如果這個成員設定為 **Null**，則沒有時間限制。 時間會設定為 GMT，且必須針對其他時區進行調整 (例如，在 PST) 的 GMT 減去8小時。

</dd> <dt>

**LogonServer**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ 登入 \_ 伺服器」 ) 
</dt> </dl>

傳送登入要求的伺服器名稱。 伺服器名稱的前面應該要有兩個反斜線 (\\ \\) 。 具有星號 (的伺服器名稱 \\ \\ \*) 表示登入要求可以由任何登入伺服器處理。 Null 字串表示將要求傳送至網域控制站。

範例： " \\ \\ MyServer"

</dd> <dt>

**MaximumStorage**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ 儲存體上限」 \_ ) ，[**單位**](../wmisdk/standard-qualifiers.md) ( 「位元組」 ) 
</dt> </dl>

可供使用者使用的最大磁碟空間量。 如果 MaximumStorage 設定為 \_ \_ [無限制使用者 MAXSTORAGE]，則允許使用者使用所有可用的磁碟空間。

範例：10000000

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| Network Management 結構 \| [**USER \_ INFO \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ name" ) 
</dt> </dl>

特定網域或電腦上的使用者帳戶。 名稱中的字元數不能超過 UNLEN 的值。

範例： "n \\ johndoe"

</dd> <dt>

**NumberOfLogons**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ num 登入」 \_ ) 
</dt> </dl>

使用者嘗試登入此帳戶的成功次數。 0xFFFFFFFF 的值表示值不明。 這個屬性會在網域中 (BDC) 的每個備份網域控制站上分開維護。 若要取得精確的值，應該只使用來自所有 Bdc 的最大值。

範例: 4

</dd> <dt>

**參數**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ parms」 ) 
</dt> </dl>

留有空間供應用程式使用。 這個字串可以是 null，也可以在終止的 null 字元之前有任意數目的字元。 Microsoft 產品會使用這個成員來儲存使用者設定資訊。 請勿修改此資訊，因為此值是應用程式特有的。

</dd> <dt>

**PasswordAge**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ 密碼 \_ 使用期限」 ) 
</dt> </dl>

密碼生效的時間長度。 此值是從上次變更密碼以來經過的秒數來測量。

範例： 00001201000230.000000 000

</dd> <dt>

**PasswordExpires**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ MODALS \_ 資訊 \_ 0**](/windows/win32/api/lmaccess/ns-lmaccess-user_modals_info_0) \| usrmod0 \_ 最大 \_ 密碼 \_ 存留期」 ) 
</dt> </dl>

密碼過期的日期和時間。 此值的設定格式如下： yyyymmddhhmmss.ffffff. mmmmmm sutc

範例： 19521201000230.000000 000

</dd> <dt>

**PrimaryGroupId**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ 主要 \_ 群組 \_ 識別碼」 ) 
</dt> </dl>

此使用者的主要全域群組 (RID) 的相對識別碼。 此識別碼會驗證使用者設定檔所屬的主要群組。

</dd> <dt>

**特權**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 的特權」 \_ ) 
</dt> </dl>

指派給 **usri3 \_ name** 屬性的許可權層級。

<dt>

<span id="Guest"></span><span id="guest"></span><span id="GUEST"></span>

**來賓** (0) 


</dt> <dd></dd> <dt>

<span id="User"></span><span id="user"></span><span id="USER"></span>

**使用者** (1) 


</dt> <dd></dd> <dt>

<span id="Administrator"></span><span id="administrator"></span><span id="ADMINISTRATOR"></span>

**系統管理員** (2) 


</dt> <dd></dd> </dl>

</dd> <dt>

**設定檔**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ 設定檔」 ) 
</dt> </dl>

使用者設定檔的路徑。 這個值可以是 null 字串、區域絕對路徑或 UNC 路徑。 使用者設定檔包含可針對每個使用者自訂的設定，例如桌面色彩。

範例： "C： \\ Windows"

</dd> <dt>

**ScriptPath**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ 腳本 \_ 路徑」 ) 
</dt> </dl>

使用者登入腳本的目錄路徑。 登入腳本會在每次使用者登入系統時，自動執行一組命令。

範例： "C： \\ win \\ profiles \\ ThomasSteven"

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](../wmisdk/standard-qualifiers.md) (256) 
</dt> </dl>

已知目前物件的識別碼。

這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。

</dd> <dt>

**UnitsPerWeek**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| \_ 每週的 usri3 單位」 \_ \_ ) 
</dt> </dl>

一周所分割的時間單位數。 它會搭配 **LogonHours** 屬性使用，以限制使用者對電腦的存取權。

範例：每週 168 (小時) 

</dd> <dt>

**UserComment**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ usr \_ 批註」 ) 
</dt> </dl>

此設定檔的使用者定義批註或描述。

</dd> <dt>

**UserId**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ 使用者 \_ 識別碼」 ) 
</dt> </dl>

使用者的 RID。 此識別碼會驗證使用者是否存在，而且對此網域而言是唯一的。

</dd> <dt>

**UserType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ 旗標」 ) 
</dt> </dl>

使用者具有許可權的帳戶類型。

值如下：

-   「一般帳戶」
-   「重複的帳戶」
-   「工作站信任帳戶」
-   「伺服器信任帳戶」
-   「限域信任帳戶」
-   不明

<dt>

<span id="Normal_Account"></span><span id="normal_account"></span><span id="NORMAL_ACCOUNT"></span>

**一般帳戶** ( 「一般帳戶」 ) 


</dt> <dd></dd> <dt>

<span id="Duplicate_Account"></span><span id="duplicate_account"></span><span id="DUPLICATE_ACCOUNT"></span>

**重複的帳戶** ( 「重複的帳戶」 ) 


</dt> <dd></dd> <dt>

<span id="Workstation_Trust_Account"></span><span id="workstation_trust_account"></span><span id="WORKSTATION_TRUST_ACCOUNT"></span>

**工作站信任帳戶** ( 「工作站信任帳戶」 ) 


</dt> <dd></dd> <dt>

<span id="Server_Trust_Account"></span><span id="server_trust_account"></span><span id="SERVER_TRUST_ACCOUNT"></span>

**伺服器信任帳戶** ( [伺服器信任帳戶] ) 


</dt> <dd></dd> <dt>

<span id="Interdomain_Trust_Account"></span><span id="interdomain_trust_account"></span><span id="INTERDOMAIN_TRUST_ACCOUNT"></span>

「域間信任帳戶 **」 ( 「域間信任帳戶**」 ) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 ( 「未知」 ) 


</dt> <dd></dd> </dl>

</dd> <dt>

**工作站**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( 「Win32API \| 網路管理結構 \| [**使用者 \_ 資訊 \_ 3**](/windows/win32/api/lmaccess/ns-lmaccess-user_info_3) \| usri3 \_ 工作站」 ) 
</dt> </dl>

使用者可以登入的工作站名稱。 最多可指定八個工作站;這些名稱必須以逗號分隔 (，) 。 Null 字串表示沒有限制。 若要停用此帳戶的所有工作站登入，請 \_ 在此類別的 [ **旗標** ] 屬性中設定 [UF] ACCOUNTDISABLE。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ NetworkLoginProfile** 類別衍生自 [**CIM \_ 設定**](cim-setting.md)。

使用這個類別的呼叫進程必須在登錄所在的電腦上具有 **SE \_ RESTORE \_ NAME** 許可權。 如需詳細資訊，請參閱 [執行特殊許可權作業](../wmisdk/executing-privileged-operations.md)。

## <a name="examples"></a>範例

[列出網路登入設定檔](https://Gallery.TechNet.Microsoft.Com/4b84fb8a-964e-4811-98d2-de1009685a14)PowerShell 範例會傳回電腦上所有使用者的網路登入資訊。

下列 VBScript 範例會傳回網路登入資訊。


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery _ 
    ("Select * from Win32_NetworkLoginProfile") 
 
For Each objItem in colItems 
    dtmWMIDate = objItem.AccountExpires 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Account Expires: " & strReturn 
    Wscript.Echo "Authorization Flags: " & objItem.AuthorizationFlags 
    Wscript.Echo "Bad Password Count: " & objItem.BadPasswordCount 
    Wscript.Echo "Caption: " & objItem.Caption 
    Wscript.Echo "CodePage: " & objItem.CodePage 
    Wscript.Echo "Comment: " & objItem.Comment 
    Wscript.Echo "Country Code: " & objItem.CountryCode 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Flags: " & objItem.Flags 
    Wscript.Echo "Full Name: " & objItem.FullName 
    Wscript.Echo "Home Directory: " & objItem.HomeDirectory 
    Wscript.Echo "Home Directory Drive: " & objItem.HomeDirectoryDrive 
    dtmWMIDate = objItem.LastLogoff 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Last Logoff: " & strReturn 
    dtmWMIDate = objItem.LastLogon 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Last Logon: " & strReturn 
    Wscript.Echo "Logon Hours: " & objItem.LogonHours 
    Wscript.Echo "Logon Server: " & objItem.LogonServer 
    Wscript.Echo "Maximum Storage: " & objItem.MaximumStorage 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "Number Of Logons: " & objItem.NumberOfLogons 
    Wscript.Echo "Password Age: " & objItem.PasswordAge 
    dtmWMIDate = objItem.PasswordExpires 
    strReturn = WMIDateStringToDate(dtmWMIDate) 
    Wscript.Echo "Password Expires: " & strReturn 
    Wscript.Echo "Primary Group ID: " & objItem.PrimaryGroupId 
    Wscript.Echo "Privileges: " & objItem.Privileges 
    Wscript.Echo "Profile: " & objItem.Profile 
    Wscript.Echo "Script Path: " & objItem.ScriptPath 
    Wscript.Echo "Setting ID: " & objItem.SettingID 
    Wscript.Echo "Units Per Week: " & objItem.UnitsPerWeek 
    Wscript.Echo "User Comment: " & objItem.UserComment 
    Wscript.Echo "User Id: " & objItem.UserId 
    Wscript.Echo "User Type: " & objItem.UserType 
    Wscript.Echo "Workstations: " & objItem.Workstations 
    Wscript.Echo 
Next 
  
Function WMIDateStringToDate(dtmWMIDate) 
    If Not IsNull(dtmWMIDate) Then 
    WMIDateStringToDate = CDate(Mid(dtmWMIDate, 5, 2) & "/" & _ 
         Mid(dtmWMIDate, 7, 2) & "/" & Left(dtmWMIDate, 4) _ 
             & " " & Mid (dtmWMIDate, 9, 2) & ":" & _ 
                 Mid(dtmWMIDate, 11, 2) & ":" & Mid(dtmWMIDate, 13, 2)) 
    End If 
End Function 
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

[**CIM \_ 設定**](cim-setting.md)
</dt> <dt>

[作業系統類別](./operating-system-classes.md)
</dt> </dl>

 

 
