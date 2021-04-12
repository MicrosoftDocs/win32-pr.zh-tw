---
title: Win32_RDSHServer 類別
description: 管理遠端桌面工作階段主機 (RDSH) 伺服器。
ms.assetid: 2c2840d2-16aa-484a-979b-6dbb1a08bbcf
ms.tgt_platform: multiple
keywords:
- Win32_RDSHServer 類別遠端桌面服務
- Win32_RDSHServer 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_RDSHServer
- Win32_RDSHServer.Name
- Win32_RDSHServer.ConnectionBroker
- Win32_RDSHServer.CollectionAlias
- Win32_RDSHServer.ServerState
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6434a4dfe6bc1a79fdaf4576a89ef552cebd5e1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317264"
---
# <a name="win32_rdshserver-class"></a>Win32 \_ RDSHServer 類別

管理遠端桌面工作階段主機 (RDSH) 伺服器。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDSHServer
{
  string Name;
  string ConnectionBroker;
  string CollectionAlias;
  uint32 ServerState;
};
```

## <a name="members"></a>成員

**Win32 \_ RDSHServer** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 \_ RDSHServer** 類別具有這些方法。



| 方法                                                                          | 描述                                                                                                                                                                       |
|:--------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetInt32Property**](getint32property-win32-rdshserver.md)                   | 抓取 **Win32 \_ RDSHServer** 物件的整數屬性值。<br/>                                                                                                 |
| [**GetPendingStartServerList**](win32-rdshserver-getpendingstartserverlist.md) | 抓取等候啟動的伺服器清單。<br/>                                                                                                                           |
| [**GetStringProperty**](getstringproperty-win32-rdshserver.md)                 | 抓取 **Win32 \_ RDSHServer** 物件的字串屬性值。<br/>                                                                                                   |
| [**SetInt32Property**](setint32property-win32-rdshserver.md)                   | 更新 **Win32 \_ RDSHServer** 物件的整數屬性值。<br/>                                                                                                   |
| [**SetStringProperty**](setstringproperty-win32-rdshserver.md)                 | 更新 **Win32 \_ RDSHServer** 物件的字串屬性值。<br/>                                                                                                     |
| [**TestAndSetState**](win32-rdshserver-testandsetstate.md)                     | 比較目前的狀態與指定的比較元;如果兩者相符，則狀態會設定為新的值。 不論相符的結果為何，也會傳回目前的狀態。<br/> |



 

### <a name="properties"></a>屬性

**Win32 \_ RDSHServer** 類別具有這些屬性。

<dl> <dt>

**CollectionAlias**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**選擇性**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

取得並設定指派給 RDSH 伺服器之 RDSH 集合的別名。

</dd> <dt>

**ConnectionBroker**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

取得和設定管理使用者對 RDSH 伺服器之存取權的遠端桌面連線代理人 (RDCB) 的名稱。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

取得和設定 RDSH 伺服器的名稱。

</dd> <dt>

**ServerState**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**選擇性**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

描述伺服器的狀態。 執行 (3) **的 \_ 目標** 以外的任何值都是保留的，而且應該視為不正確狀態。

可能的值為。

<dt>

<span id="TARGET_UNKNOWN"></span><span id="target_unknown"></span>

**目標 \_未知** 的 (1) 


</dt> <dd></dd> <dt>

<span id="TARGET_RUNNING"></span><span id="target_running"></span>

**目標 \_正在** 執行 (3) 


</dt> <dd></dd> <dt>

<span id="TARGET_INVALID"></span><span id="target_invalid"></span>

**目標 \_無效** 的 (8) 


</dt> <dd></dd> <dt>

<span id="TARGET_STARTING"></span><span id="target_starting"></span>

**目標 \_開始** (9) 


</dt> <dd></dd> <dt>

<span id="TARGET_STOPPING"></span><span id="target_stopping"></span>

**目標 \_停止** (10) 


</dt> <dd></dd> </dl>

**Windows server 2012 R2 和 Windows server 2012：** 此屬性在 Windows Server 2016 之前無法使用。

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

 

