---
title: Win32_RDMSVirtualDesktop 類別
description: 代表虛擬桌面。
ms.assetid: e2952ec0-38d0-4a1c-b423-3ae1fbc701b3
ms.tgt_platform: multiple
keywords:
- Win32_RDMSVirtualDesktop 類別遠端桌面服務
- Win32_RDMSVirtualDesktop 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop
- Win32_RDMSVirtualDesktop.Name
- Win32_RDMSVirtualDesktop.HostName
- Win32_RDMSVirtualDesktop.Status
- Win32_RDMSVirtualDesktop.CollectionAlias
- Win32_RDMSVirtualDesktop.SessionState
- Win32_RDMSVirtualDesktop.SessionUserName
- Win32_RDMSVirtualDesktop.UserName
- Win32_RDMSVirtualDesktop.UserDomain
- Win32_RDMSVirtualDesktop.VMState
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 247c49c7ad069b4feff3469ac21ec803ebc9f741
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965895"
---
# <a name="win32_rdmsvirtualdesktop-class"></a>Win32 \_ RDMSVirtualDesktop 類別

代表虛擬桌面。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSVirtualDesktop
{
  string Name;
  string HostName;
  uint32 Status;
  string CollectionAlias;
  string SessionState;
  string SessionUserName;
  string UserName;
  string UserDomain;
  uint32 VMState;
};
```

## <a name="members"></a>成員

**Win32 \_ RDMSVirtualDesktop** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 \_ RDMSVirtualDesktop** 類別具有這些方法。



| 方法                                                                                              | 描述                                                                                            |
|:----------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [**GetUserAssignment**](getuserassignment-win32-rdmsvirtualdesktop.md)                             | 抓取指派給虛擬桌面使用者的使用者名稱和功能變數名稱。<br/> |
| [**GetVirtualDesktopAssignedToUser**](getvirtualdesktopassignedtouser-win32-rdmsvirtualdesktop.md) | 抓取指派給指定使用者的虛擬桌面。<br/>                       |
| [**GetVirtualDesktopDetails**](getvirtualdesktopdetails-win32-rdmsvirtualdesktop.md)               | 抓取虛擬桌面的其他相關資訊。<br/>                             |
| [**GetVirtualDesktopState**](getvirtualdesktopstate-win32-rdmsvirtualdesktop.md)                   | 捕獲虛擬桌面的狀態。<br/>                                                 |
| [**RemoveUserAssignment**](removeuserassignment-win32-rdmsvirtualdesktop.md)                       | 從虛擬桌面移除使用者指派。<br/>                                       |
| [**SetUserAssignment**](setuserassignment-win32-rdmsvirtualdesktop.md)                             | 將虛擬桌面指派給使用者。<br/>                                                        |
| [**SetVirtualDesktopState**](setvirtualdesktopstate-win32-rdmsvirtualdesktop.md)                   | 更新虛擬桌面的狀態。<br/>                                                   |



 

### <a name="properties"></a>屬性

**Win32 \_ RDMSVirtualDesktop** 類別具有這些屬性。

<dl> <dt>

**CollectionAlias**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**選擇性**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

取得管理虛擬機器之虛擬桌面集合的別名。

</dd> <dt>

**HostName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得裝載虛擬機器的電腦名稱稱。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

取得虛擬機器的名稱。

</dd> <dt>

**SessionState**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**選擇性**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

取得虛擬桌面會話的狀態。

</dd> <dt>

**SessionUserName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**選擇性**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

取得登入虛擬桌面會話之使用者的使用者名稱。

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得虛擬機器的狀態。

</dd> <dt>

**UserDomain**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**選擇性**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

取得指派給虛擬桌面之使用者的功能變數名稱。

</dd> <dt>

**使用者名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**選擇性**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

取得指派給虛擬桌面使用者的使用者名稱。

</dd> <dt>

**VMState**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

取得虛擬桌面的狀態。

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

 

