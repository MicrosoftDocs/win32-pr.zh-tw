---
description: Msvm \_ GuestFileService 包含一個方法，可用來將檔案從 hyper-v 主機複製到虛擬機器。
ms.assetid: 3599d5a8-415f-48f8-b887-00a93b7abb83
title: Msvm_GuestFileService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestFileService
- Msvm_GuestFileService.StartService
- Msvm_GuestFileService.StopService
- Msvm_GuestFileService.Caption
- Msvm_GuestFileService.CreationClassName
- Msvm_GuestFileService.Description
- Msvm_GuestFileService.InstallDate
- Msvm_GuestFileService.Name
- Msvm_GuestFileService.Started
- Msvm_GuestFileService.StartMode
- Msvm_GuestFileService.Status
- Msvm_GuestFileService.SystemCreationClassName
- Msvm_GuestFileService.SystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fa307a55963f6773682e81a08bf7d45e064c9a5bd7213f5d2d426a8d44be70b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789888"
---
# <a name="msvm_guestfileservice-class"></a>Msvm \_ GuestFileService 類別

**Msvm \_GuestFileService** 包含可用於將檔案從 hyper-v 主機複製到虛擬機器的方法。 這個類別衍生自 [**Msvm \_ GuestService**](msvm-guestservice.md)。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestFileService : Msvm_GuestService
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  datetime InstallDate;
  string   Name;
  boolean  Started;
  string   StartMode;
  string   Status;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a>成員

**Msvm \_ GuestFileService** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Msvm \_ GuestFileService** 類別具有這些方法。



| 方法                                                             | 描述                                                                                                                                                                  |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CopyFilesToGuest**](copyfilestoguest-msvm-guestfileservice.md) | 將檔案從 Hyper-v 主機複製到虛擬機器。<br/> **Windows 8.1：** 在 Windows 8.1 和 Windows Server 2012 R2 之前，不支援這個方法。<br/> |
| **StartService**                                                   | 不支援這個方法。<br/>                                                                                                                                     |
| **StopService**                                                    | 不支援這個方法。<br/>                                                                                                                                     |



 

### <a name="properties"></a>屬性

**Msvm \_ GuestFileService** 類別具有這些屬性。

<dl> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的簡短文字描述。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

建立實例時所使用之類別或子類別的名稱。 搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的文字描述。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的安裝日期和時間。 這個屬性不需要值來表示已安裝物件。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

服務的唯一識別碼，也會提供所管理功能的指示。 如需功能的詳細資訊，請參閱物件的 **Description** 屬性。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

</dd> <dt>

**已開始**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 TRUE**，表示服務已啟動。

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出服務是否自動啟動 (例如，作業系統) ，或只在要求時啟動。

包括下列值：

<dl><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span><dt>

**自動**
</dt><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span><dt>

**》**
</dt> </dl>

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的目前狀態。 這個屬性繼承自 [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)。

包括下列值：

<dl><span id="OK"></span><span id="ok"></span><dt>

**正常**
</dt><span id="Error"></span><span id="error"></span><span id="ERROR"></span><dt>

**錯誤**
</dt><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dt>

**降級**
</dt><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dt>

**不明**
</dt><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span><dt>

**「Pred 失敗」**
</dt><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dt>

**入門**
</dt><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span><dt>

**從而**
</dt><span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dt>

**維護**
</dt><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span><dt>

**強調**
</dt><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span><dt>

**"NonRecover"**
</dt><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span><dt>

**「無連絡人」**
</dt><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span><dt>

**「遺失通訊」**
</dt> </dl>

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

設定系統建立類別名稱的範圍。

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

裝載服務的系統名稱。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[僅限桌面應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | Windows Server 2012\[僅限 R2 desktop 應用程式\]<br/>                                                 |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ GuestService**](msvm-guestservice.md)
</dt> </dl>

 

