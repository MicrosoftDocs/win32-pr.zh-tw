---
description: SystemConfig_Services 類別-這個類別是服務設定事件的事件種類類別。
ms.assetid: 7cba9992-d154-44b8-87d8-b46a8438f607
title: SystemConfig_Services 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Services
- SystemConfig_Services.ProcessId
- SystemConfig_Services.ServiceState
- SystemConfig_Services.SubProcessTag
- SystemConfig_Services.ServiceName
- SystemConfig_Services.DisplayName
- SystemConfig_Services.ProcessName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 754b0e10c3882911c6e91fc2590c11739c3f7531
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106056"
---
# <a name="systemconfig_services-class"></a>SystemConfig \_ 服務類別

此類別是服務設定事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType(15), EventTypeName("Services")]
class SystemConfig_Services : SystemConfig
{
  uint32 ProcessId;
  uint32 ServiceState;
  uint32 SubProcessTag;
  string ServiceName[];
  string DisplayName[];
  string ProcessName[];
};
```

## <a name="members"></a>成員

**SystemConfig \_ Services** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**SystemConfig \_ Services** 類別具有這些屬性。

<dl> <dt>

**DisplayName**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (5) 、 **StringTermination ( "NullTerminated" )**、 **Format ( "w" )**
</dt> </dl>

服務的顯示名稱。 服務控制管理員中的名稱會保留大小寫。 不過，顯示名稱比較一定不區分大小寫。

</dd> <dt>

**進程**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (1) ， **格式 ( "x" )**
</dt> </dl>

服務執行所在進程的識別碼。

</dd> <dt>

**ProcessName**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (6) 、 **StringTermination ( "NullTerminated" )**、 **Format ( "w" )**
</dt> </dl>

服務執行所在進程的名稱。

</dd> <dt>

**ServiceName**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (4) 、 **StringTermination ( "NullTerminated" )**、 **Format ( "w" )**
</dt> </dl>

服務的唯一識別碼。 此識別碼提供服務所提供之功能的指示。

</dd> <dt>

**ServiceState**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (2) ， **格式 ( "x" )**
</dt> </dl>

服務的目前狀態。 如需可能的值，請參閱 **服務 \_ 狀態 \_ 進程** 的 **dwCurrentState** 成員。

</dd> <dt>

**SubProcessTag**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **WmiDataId** (3) ， **格式 ( "x" )**
</dt> </dl>

識別服務。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 




