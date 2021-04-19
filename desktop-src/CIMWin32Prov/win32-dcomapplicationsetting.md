---
description: Win32 \_ DCOMApplicationSetting&\# 8194;WMI 類別代表 DCOM 應用程式的設定。
ms.assetid: afa23faa-bf4d-4f54-9ee9-227956ff3292
ms.tgt_platform: multiple
title: Win32_DCOMApplicationSetting 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplicationSetting
- Win32_DCOMApplicationSetting.Caption
- Win32_DCOMApplicationSetting.Description
- Win32_DCOMApplicationSetting.SettingID
- Win32_DCOMApplicationSetting.AppID
- Win32_DCOMApplicationSetting.AuthenticationLevel
- Win32_DCOMApplicationSetting.CustomSurrogate
- Win32_DCOMApplicationSetting.EnableAtStorageActivation
- Win32_DCOMApplicationSetting.LocalService
- Win32_DCOMApplicationSetting.RemoteServerName
- Win32_DCOMApplicationSetting.RunAsUser
- Win32_DCOMApplicationSetting.ServiceParameters
- Win32_DCOMApplicationSetting.UseSurrogate
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 085304c5319811ba87979124613c7d8e83fd7479
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973184"
---
# <a name="win32_dcomapplicationsetting-class"></a>Win32 \_ DCOMApplicationSetting 類別

**Win32 \_ DCOMApplicationSetting** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表 DCOM 應用程式的設定。 它包含與登錄中的 **AppID** 金鑰相關聯的 DCOM 設定選項。 這些選項在以邏輯方式分組于指定應用程式類別之下的元件上是有效的。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A561-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_DCOMApplicationSetting : Win32_COMSetting
{
  string  Caption;
  string  Description;
  string  SettingID;
  string  AppID;
  uint32  AuthenticationLevel;
  string  CustomSurrogate;
  boolean EnableAtStorageActivation;
  string  LocalService;
  string  RemoteServerName;
  string  RunAsUser;
  string  ServiceParameters;
  boolean UseSurrogate;
};
```

## <a name="members"></a>成員

**Win32 \_ DCOMApplicationSetting** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 \_ DCOMApplicationSetting** 類別具有這些方法。



| 方法                                                                                                                        | 描述                                                                                                                                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAccessSecurityDescriptor**](getaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md)               | 取得安全描述項，以控制允許存取 DCOM 應用程式的人員。<br/>                                                                                                                              |
| [**GetConfigurationSecurityDescriptor**](getconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md) | 取得安全描述項，以控制允許哪些人設定 DCOM 應用程式。<br/>                                                                                                                           |
| [**GetLaunchSecurityDescriptor**](getlaunchsecuritydescriptor-in-class-win32-dcomapplicationsetting.md)                      | 取得安全描述項，可控制哪些人可以啟動 DCOM 應用程式。<br/>                                                                                                                              |
| [**SetAccessSecurityDescriptor**](setaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md)               | 使用 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) 類別的實例所定義的新安全描述項，更新 DCOM 應用程式的存取安全描述項。<br/>        |
| [**SetConfigurationSecurityDescriptor**](setconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md) | 使用 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) 類別的實例所定義的新安全描述項，更新 DCOM 應用程式的設定安全描述項。<br/> |
| [**SetLaunchSecurityDescriptor**](setlaunchsecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md)               | 使用 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) 類別的實例所定義的新安全描述項，更新 DCOM 應用程式的啟動安全描述項。<br/>        |



 

### <a name="properties"></a>屬性

**Win32 \_ DCOMApplicationSetting** 類別具有這些屬性。

<dl> <dt>

**AppID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ AppID \\ \\ {GUID} \[ Default \] " ) 
</dt> </dl>

這個 DCOM 應用程式的全域唯一識別碼 (GUID) 。

</dd> <dt>

**AuthenticationLevel**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ AppID \\ \\ {GUID} \[ AuthenticationLevel \] " ) 
</dt> </dl>

此 COM 伺服器所需的最小用戶端驗證等級。 如果是 **Null**，則會使用預設值。

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**無** (1) 


</dt> <dd>

無 (不執行任何驗證) 

</dd> <dt>

<span id="Connect"></span><span id="connect"></span><span id="CONNECT"></span>

<span id="Connect"></span><span id="connect"></span><span id="CONNECT"></span>**連接** (2) 


</dt> <dd>

只有當用戶端與應用程式建立關聯性時，才會執行 Connect (驗證) 

</dd> <dt>

<span id="Call"></span><span id="call"></span><span id="CALL"></span>

<span id="Call"></span><span id="call"></span><span id="CALL"></span>**呼叫** (3) 


</dt> <dd>

只有當應用程式收到要求時，才會在每次呼叫開始時執行呼叫 (驗證) 

</dd> <dt>

<span id="Packet"></span><span id="packet"></span><span id="PACKET"></span>

<span id="Packet"></span><span id="packet"></span><span id="PACKET"></span>封 **包** (4) 


</dt> <dd>

封包 (驗證是在從用戶端接收的所有資料上執行) 

</dd> <dt>

<span id="PacketIntegrity"></span><span id="packetintegrity"></span><span id="PACKETINTEGRITY"></span>

<span id="PacketIntegrity"></span><span id="packetintegrity"></span><span id="PACKETINTEGRITY"></span>**PacketIntegrity** (5) 


</dt> <dd>

PacketIntegrity (在用戶端和應用程式之間傳送的所有資料都會經過驗證和驗證) 

</dd> <dt>

<span id="PacketPrivacy"></span><span id="packetprivacy"></span><span id="PACKETPRIVACY"></span>

<span id="PacketPrivacy"></span><span id="packetprivacy"></span><span id="PACKETPRIVACY"></span>**PacketPrivacy** (6) 


</dt> <dd>

PacketPrivacy (會使用其他驗證等級的屬性，並加密所有資料) 

</dd> </dl>

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 
</dt> </dl>

目前物件的簡短文字描述。

這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。

</dd> <dt>

**CustomSurrogate**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ AppID \\ \\ {GUID} \[ DllSurrogate \] " ) 
</dt> </dl>

啟用內含式 DCOM 應用程式之自訂代理的名稱。 如果這個值是 **Null** ，且 **UseSurrogate** 索引鍵為 **TRUE**，則系統會提供代理程式。

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

**EnableAtStorageActivation**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ AppID \\ \\ {GUID} \[ ActivateAtStorage \] " ) 
</dt> </dl>

DCOM 應用程式會從第一次初始化應用程式的狀態，抓取應用程式的儲存狀態或開始。

</dd> <dt>

**LocalService**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ AppID \\ \\ {GUID} \[ LocalService \] " ) 
</dt> </dl>

DCOM 應用程式所提供之服務的名稱。

</dd> <dt>

**RemoteServerName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ AppID \\ \\ {GUID} \[ RemoteServerName \] " ) 
</dt> </dl>

啟用應用程式的遠端伺服器名稱。

</dd> <dt>

**RunAsUser**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ AppID \\ \\ {GUID} \[ RunAs \] " ) 
</dt> </dl>

要在啟用時執行應用程式的特定使用者帳戶。

</dd> <dt>

**ServiceParameters**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ AppID \\ \\ {GUID} \[ ServiceParameters \] " ) 
</dt> </dl>

傳遞至 DCOM 應用程式的命令列參數。 只有當應用程式是以 Windows 為基礎的服務撰寫時，才會有效。

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 
</dt> </dl>

已知目前物件的識別碼。

這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。

</dd> <dt>

**UseSurrogate**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| HKEY \_ LOCAL \_ MACHINE \\ \\ SOFTWARE class \\ \\ \\ \\ AppID \\ \\ {GUID} \[ DllSurrogate \] " ) 
</dt> </dl>

您可以使用代理可執行檔，將 DCOM 應用程式啟用為跨進程伺服器。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ DCOMApplicationSetting** 類別衍生自 [**win32 \_ COMSetting**](win32-comsetting.md)。

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

[**Win32 \_ COMSetting**](win32-comsetting.md)
</dt> <dt>

[作業系統類別](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**許可權常數**](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[WMI 安全描述項物件](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[變更安全物件的存取安全性](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

