---
description: HWConfig 類別是 Windows XP 上硬體設定事件的父類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 47f062c0-fdf0-4beb-906d-257571324de9
title: HWConfig 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig
api_type:
- NA
api_location: ''
ms.openlocfilehash: cfb194e09701dbc52b00279b624877f09ffac24b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852803"
---
# <a name="hwconfig-class"></a>HWConfig 類別

**HWConfig** 類別是 Windows XP 上硬體設定事件的父類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}")]
class HWConfig : MSNT_SystemTrace
{
};
```

## <a name="members"></a>成員

**HWConfig** 類別不會定義任何成員。

## <a name="remarks"></a>備註

這些事件會提供電腦的硬體設定。 不同于其他 NT 核心記錄器事件，核心會話會自動產生硬體設定事件;當您啟動 NT Kernel 記錄器會話時，不會啟用這些事件。

**Windows 2000：** 不支援。

如需 Windows Vista 和 Windows Server 2003 上的硬體設定事件，請參閱 [SystemConfig](systemconfig.md) 類別。

事件追蹤取用者可以藉由呼叫 [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) 函式並將 [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) 指定為 *pGuid* 參數，來執行硬體設定事件的特殊處理。 使用下列事件種類來識別使用事件時的實際硬體設定事件。



| 事件類型                                                                      | 描述                                                                                                                                      |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| **活動 \_追蹤 \_ 類型 \_ 設定 \_ CPU** (事件種類值為 10) <br/>          | CPU 設定事件。 [**HWConfig \_ CPU**](hwconfig-cpu.md) MOF 類別會定義此事件的事件資料。                            |
| **活動 \_追蹤 \_ 類型 \_ 設定 \_ LOGICALDISK** (事件種類值為 12) <br/>  | 邏輯磁片設定事件。 [**HWConfig \_ LogDisk**](hwconfig-logdisk.md) mof 類別 mof 類別會定義此事件的事件資料。 |
| **活動 \_追蹤 \_ 類型 \_ CONFIG \_ NIC** (事件種類值為 13) <br/>          | NIC 設定事件。 [**HWConfig \_ NIC**](hwconfig-nic.md) MOF 類別會定義此事件的事件資料。                            |
| **活動 \_追蹤 \_ 類型 \_ 設定 \_ PHYSICALDISK** (事件種類值為 11) <br/> | 實體磁片設定事件。 [**HWConfig \_ PhyDisk**](hwconfig-phydisk.md) MOF 類別會定義此事件的事件資料。          |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**HWConfig \_ CPU**](hwconfig-cpu.md)
</dt> <dt>

[**HWConfig \_ LogDisk**](hwconfig-logdisk.md)
</dt> <dt>

[**HWConfig \_ NIC**](hwconfig-nic.md)
</dt> <dt>

[**HWConfig \_ PhyDisk**](hwconfig-phydisk.md)
</dt> </dl>

 

 
