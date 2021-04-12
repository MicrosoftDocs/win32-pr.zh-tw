---
title: Win32_SessionDirectorySession 類別
description: 提供屬性，以用來查看遠端桌面連線代理人 (RD 連線代理人) 會話的屬性。
ms.assetid: 34b5a898-3952-493c-ba62-dd0d298b0600
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectorySession 類別遠端桌面服務
- Win32_SessionDirectorySession 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_SessionDirectorySession
- Win32_SessionDirectorySession.ServerName
- Win32_SessionDirectorySession.SessionID
- Win32_SessionDirectorySession.UserName
- Win32_SessionDirectorySession.DomainName
- Win32_SessionDirectorySession.ServerIPAddress
- Win32_SessionDirectorySession.TSProtocol
- Win32_SessionDirectorySession.ApplicationType
- Win32_SessionDirectorySession.ResolutionWidth
- Win32_SessionDirectorySession.ResolutionHeight
- Win32_SessionDirectorySession.ColorDepth
- Win32_SessionDirectorySession.CreateTime
- Win32_SessionDirectorySession.DisconnectTime
- Win32_SessionDirectorySession.SessionState
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fba8fdbdffc764c3bdcc1a8f5bc53aa479f318d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384149"
---
# <a name="win32_sessiondirectorysession-class"></a>Win32 \_ SessionDirectorySession 類別

提供屬性，以用來查看遠端桌面連線代理人 (RD 連線代理人) 會話的屬性。

> [!Note]  
> 在 Windows Server 2008 R2 中，終端機服務會話代理人 (TS 會話代理人) 的名稱已變更為 RD 連線代理人。 除非另有說明，否則這些屬性適用于所有支援的作業系統。

 

## <a name="syntax"></a>語法

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYSESSION_Prov"), AMENDMENT]
class Win32_SessionDirectorySession
{
  string   ServerName;
  uint32   SessionID;
  string   UserName;
  string   DomainName;
  string   ServerIPAddress;
  uint32   TSProtocol;
  string   ApplicationType;
  uint32   ResolutionWidth;
  uint32   ResolutionHeight;
  uint32   ColorDepth;
  DateTime CreateTime;
  DateTime DisconnectTime;
  uint32   SessionState;
};
```

## <a name="members"></a>成員

**Win32 \_ SessionDirectorySession** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ SessionDirectorySession** 類別具有這些屬性。

<dl> <dt>

**ApplicationType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

應用程式已開始使用此會話。 這與 [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md)的 **StartProgram** 屬性相同。

</dd> <dt>

**ColorDepth**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

會話的色彩深度，以每圖元的位數來測量。

</dd> <dt>

**Createtimefilterend**
</dt> <dd> <dl> <dt>

資料類型： **DateTime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

建立會話的日期和時間。 當會話中斷連接並重新連接時，不會重設此值。

</dd> <dt>

**DisconnectTime**
</dt> <dd> <dl> <dt>

資料類型： **DateTime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

會話中斷連線的日期和時間 (如果適用) 。

</dd> <dt>

**DomainName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

登入此會話之使用者的功能變數名稱。

</dd> <dt>

**ResolutionHeight**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此會話的會話高度（以圖元為單位）。

</dd> <dt>

**ResolutionWidth**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此會話的會話寬度（以圖元為單位）。

</dd> <dt>

**Microsoft.sqlserver.management.smo.wmi.serveripaddress<**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此會話的 RD 連線代理人伺服器 IP 位址。

</dd> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

此會話的 RD 連線代理人伺服器名稱。

</dd> <dt>

**SessionID**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

此會話的會話識別碼。

</dd> <dt>

**SessionState**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此會話的狀態。

<dt>

0
</dt> <dd>

會話為使用中狀態。

</dd> <dt>

1
</dt> <dd>

會話已中斷連線。

</dd> </dl>

</dd> <dt>

**TSProtocol**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此會話的通訊協定。

<dt>

0
</dt> <dd>

此會話正在實體主控台上執行。

</dd> <dt>

1
</dt> <dd>

此會話會使用專屬的協力廠商通訊協定。

</dd> <dt>

2
</dt> <dd>

此會話會使用遠端桌面通訊協定 (RDP) 。

</dd> </dl>

</dd> <dt>

**使用者名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

登入此會話之使用者的使用者名稱。

</dd> </dl>

## <a name="remarks"></a>備註

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                         |
| 命名空間<br/>                | Root\\CIMv2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>TssdWmi mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ SessionDirectoryCluster**](win32-sessiondirectorycluster.md)
</dt> <dt>

[**Win32 \_ SessionDirectoryServer**](win32-sessiondirectoryserver.md)
</dt> </dl>

 

