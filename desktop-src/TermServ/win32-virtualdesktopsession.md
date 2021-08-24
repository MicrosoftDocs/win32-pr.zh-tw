---
title: Win32_VirtualDesktopSession 類別
description: 管理虛擬桌面會話。
ms.assetid: a5a0d2a4-6e19-42ac-988c-2d3787946325
ms.tgt_platform: multiple
keywords:
- Win32_VirtualDesktopSession 類別遠端桌面服務
- Win32_VirtualDesktopSession 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_VirtualDesktopSession
- Win32_VirtualDesktopSession.VMHostName
- Win32_VirtualDesktopSession.SessionId
- Win32_VirtualDesktopSession.VMName
- Win32_VirtualDesktopSession.ConnectState
- Win32_VirtualDesktopSession.UserName
- Win32_VirtualDesktopSession.DomainName
- Win32_VirtualDesktopSession.CollectionId
- Win32_VirtualDesktopSession.ClientMachineName
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01e039df658ded4534e3e2582f08ba4e5f5a04530d810349fff5633730a84332
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137421"
---
# <a name="win32_virtualdesktopsession-class"></a>Win32 \_ VirtualDesktopSession 類別

管理虛擬桌面會話。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_VirtualDesktopSession
{
  string VMHostName;
  uint32 SessionId;
  string VMName;
  uint32 ConnectState;
  string UserName;
  string DomainName;
  string CollectionId;
  string ClientMachineName;
};
```

## <a name="members"></a>成員

**Win32 \_ VirtualDesktopSession** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 \_ VirtualDesktopSession** 類別具有這些方法。



| 方法                                                         | 描述                                                                |
|:---------------------------------------------------------------|:---------------------------------------------------------------------------|
| [**中斷連線**](disconnect-win32-virtualdesktopsession.md)   | 中斷虛擬桌面會話的連線。<br/>                        |
| [**登出**](logoff-win32-virtualdesktopsession.md)           | 登出虛擬桌面會話的使用者。<br/>             |
| [**SendMessage**](sendmessage-win32-virtualdesktopsession.md) | 透過虛擬桌面會話傳送訊息給使用者。<br/> |



 

### <a name="properties"></a>屬性

**Win32 \_ VirtualDesktopSession** 類別具有這些屬性。

<dl> <dt>

**ClientMachineName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得連接到會話的用戶端電腦名稱稱。

</dd> <dt>

**CollectionId**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得裝載虛擬機器之虛擬桌面集合的名稱。

</dd> <dt>

**ConnectState**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得會話的連接狀態。

</dd> <dt>

**DomainName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得使用者的功能變數名稱。

</dd> <dt>

**SessionId**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

取得虛擬桌面會話的識別碼。

</dd> <dt>

**使用者名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得指派給會話的使用者帳戶名稱。

</dd> <dt>

**VMHostName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

取得裝載虛擬機器之遠端桌面虛擬化主機伺服器的名稱。

</dd> <dt>

**VMName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得指派給會話的虛擬機器名稱。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                              |
| 命名空間<br/>                | 根 \\ cimv2 \\ rdm<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[遠端桌面管理服務提供者](rdms-api-reference.md)
</dt> </dl>

 

