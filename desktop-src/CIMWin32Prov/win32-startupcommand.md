---
description: Win32 \_ StartupCommand&\# 8194;WMI 類別代表當使用者登入電腦系統時自動執行的命令。
ms.assetid: 7184ade8-fcc9-47b3-af04-8054b2fca937
ms.tgt_platform: multiple
title: Win32_StartupCommand 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_StartupCommand
- Win32_StartupCommand.Caption
- Win32_StartupCommand.Description
- Win32_StartupCommand.SettingID
- Win32_StartupCommand.Command
- Win32_StartupCommand.Location
- Win32_StartupCommand.Name
- Win32_StartupCommand.User
- Win32_StartupCommand.UserSID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1c38ec84b9df38687a32211f3294258fd58efb96
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847522"
---
# <a name="win32_startupcommand-class"></a>Win32 \_ StartupCommand 類別

**Win32 \_ StartupCommand** [WMI 類別](../wmisdk/retrieving-a-class.md)代表當使用者登入電腦系統時自動執行的命令。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性和方法是以字母順序排列，而不是 MOF 順序。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C50A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_StartupCommand : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  string Command;
  string Location;
  string Name;
  string User;
  string UserSID;
};
```

## <a name="members"></a>成員

**Win32 \_ StartupCommand** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ StartupCommand** 類別具有這些屬性。

<dl> <dt>

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

**命令**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| SOFTWARE \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \\ \\ Run" ) 
</dt> </dl>

啟動命令所執行的命令。

WMI 從登錄機碼取得這項資料

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **執行**

範例： "C： \\ Windows \\notepad.exe myfile.txt"

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

**位置**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32Registry \| \\ \\ SOFTWARE \\ \\ MICROSOFT \\ \\ windows \\ \\ CURRENTVERSION \\ \\ windows" ) 
</dt> </dl>

啟動命令位於磁片檔案系統上的路徑。

例如： HKLM \\ SOFTWARE \\ Microsoft \\ Windows \\ CurrentVersion \\ Run

<dt>

<span id="Startup"></span><span id="startup"></span><span id="STARTUP"></span>

**啟動** ( 「啟動」 ) 


</dt> <dd></dd> <dt>

<span id="Common_Startup"></span><span id="common_startup"></span><span id="COMMON_STARTUP"></span>

**一般** 啟動 ( 「一般啟動」 ) 


</dt> <dd></dd> <dt>

<span id="HKLM__SOFTWARE__Microsoft__Windows__CurrentVersion__Run"></span><span id="hklm__software__microsoft__windows__currentversion__run"></span><span id="HKLM__SOFTWARE__MICROSOFT__WINDOWS__CURRENTVERSION__RUN"></span>

**\\ HKLM \\軟體 \\ \\ microsoft \\ \\ windows \\ \\ CurrentVersion \\ \\ run** ( "HKLM \\ \\ SOFTWARE \\ \\ Microsoft \\ \\ windows \\ \\ CurrentVersion \\ \\ run" ) 


</dt> <dd></dd> <dt>

<span id="HKLM__SOFTWARE__Microsoft__Windows__CurrentVersion__RunServices"></span><span id="hklm__software__microsoft__windows__currentversion__runservices"></span><span id="HKLM__SOFTWARE__MICROSOFT__WINDOWS__CURRENTVERSION__RUNSERVICES"></span>

**\\ HKLM \\SOFTWARE \\ \\ microsoft \\ \\ windows \\ \\ CurrentVersion \\ \\ RunServices** ( "HKLM \\ \\ SOFTWARE \\ \\ microsoft \\ \\ windows \\ \\ CurrentVersion \\ \\ RunServices" ) 


</dt> <dd></dd> </dl>

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "Win32API \| File 結構 \| [**WIN32 \_ FIND \_ DATA**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) \| cFileName" ) 
</dt> </dl>

啟動命令的檔案名。

範例： "FindFast"

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

**使用者**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**key**](../wmisdk/key-qualifier.md)、 [**MAPPINGSTRINGS**](../wmisdk/standard-qualifiers.md) ( "WMI" ) 
</dt> </dl>

將執行這個啟動命令的使用者名稱。

範例： "mydomain \\ myname"

</dd> <dt>

**UserSID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI" ) 
</dt> </dl>

UserSID 屬性會指出將執行這個啟動命令之使用者的 SID。 該使用者屬性可能是空的，但如果無法解析使用者名稱，UserSID 仍會有一個值 (例如已刪除的使用者) 。 屬性有助於區分與兩個不同使用者（具有未解析名稱）相關聯的命令。 當命令與未實際識別使用者的專案（如所有使用者）相關聯時，它可能會是 Null。

範例： S-1-5-21-1579938362-1064596589-3161144252-1006

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ StartupCommand** 類別衍生自 [**CIM \_ 設定**](cim-setting.md)。

載入作業系統之後，電腦啟動不會結束。 相反地，您可以設定 Windows 作業系統，讓啟動命令在每次 Windows 啟動時執行。 啟動命令會儲存在登錄中或做為使用者設定檔的一部分，並在每次載入 Windows 時用來自動啟動指定的腳本或應用程式。

在大部分情況下，自動啟動程式很有用;它們可確保在每次載入 Windows 時，會自動啟動並執行某些應用程式，例如防病毒工具。 不過，自動啟動程式也可以負責問題，例如：

-   需要很長時間才能啟動的電腦。 這可能是因為每次 Windows 啟動時都必須啟動的許多應用程式所造成的結果。
-   在工作列或工作管理員中表示的應用程式，即使使用者未啟動它們也是一樣。 雖然這些應用程式不一定會造成問題，但可能會導致來自不熟悉這些程式的使用者，以及其執行原因的使用者，可能會收到支援工程師的來電。
-   即使電腦看似閒置也會發生問題。 這些問題通常是在沒有人察覺它們正在執行時執行的啟動命令所追蹤。

識別在啟動時自動執行的應用程式和腳本是很重要但很困難的系統管理工作，因為啟動命令可儲存在許多不同的位置：

-   HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ 執行
-   HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce
-   HKCU \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ 執行
-   HKCU \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce
-   HKU \\ ProgID \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run
-   systemdrive \\ 檔和設定 \\ 所有使用者 \\ 開始功能表 \\ 程式 \\ 啟動
-   systemdrive \\ 檔和設定使用者 \\ 名稱使用者名稱 \\ 啟動功能表 \\ 程式 \\ 啟動

您可以使用 WMI Win32 \_ StartupCommand 類別來列舉 autostart 程式，而不論儲存資訊的位置為何。

使用這個類別的呼叫進程必須在登錄所在的電腦上具有「 **SE \_ 還原 \_ 名稱** 」許可權。 例如，如果您在本機電腦上列舉此類別，您的應用程式執行所在的帳戶必須具有此許可權。 如需詳細資訊，請參閱 [執行特殊許可權作業](../wmisdk/executing-privileged-operations.md)。

您可以藉由呼叫腳本或 c + + 中的 WMI [系統登錄提供者](/previous-versions/windows/desktop/regprov/system-registry-provider)方法，來變更 **Win32 \_ StartupCommand** 取得資料的登錄值。 如需詳細資訊，請參閱 [修改系統登錄](../wmisdk/modifying-the-system-registry.md)。

## <a name="examples"></a>範例

下列 VBScript 列舉電腦上的啟動命令。


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colStartupCommands = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_StartupCommand")
For Each objStartupCommand in colStartupCommands
 Wscript.Echo "Command: " & objStartupCommand.Command
 Wscript.Echo "Description: " & objStartupCommand.Description
 Wscript.Echo "Location: " & objStartupCommand.Location
 Wscript.Echo "Name: " & objStartupCommand.Name
 Wscript.Echo "SettingID: " & objStartupCommand.SettingID
 Wscript.Echo "User: " & objStartupCommand.User
Next
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

 

 
