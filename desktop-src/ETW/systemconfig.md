---
description: SystemConfig 類別-此類別是硬體設定事件的父類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 720c2366-bd68-4895-bfaf-74aa9b64ba4a
title: SystemConfig 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4f409887f70989c65475c8b854b4b610c9ffa6c122edc25e87b5ebdc8dbc9180
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069638"
---
# <a name="systemconfig-class"></a>SystemConfig 類別

此類別是硬體設定事件的父類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}"), EventVersion(2)]
class SystemConfig : MSNT_SystemTrace
{
};
```

## <a name="members"></a>成員

**SystemConfig** 類別不會定義任何成員。

## <a name="remarks"></a>備註

這些事件會提供電腦的硬體設定。 不同于其他 NT 核心記錄器事件，核心會話會自動產生硬體設定事件;當您啟動 NT Kernel 記錄器會話時，不會啟用這些事件。

如需 Windows XP 上的硬體設定事件，請參閱[HWConfig](hwconfig.md)類別。

事件追蹤取用者可以藉由呼叫 [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) 函式並將 [**EventTraceConfigGuid**](nt-kernel-logger-constants.md) 指定為 *pGuid* 參數，來執行硬體設定事件的特殊處理。 使用下列事件種類來識別使用事件時的實際硬體設定事件。



| 事件類型                                                                      | 描述                                                                                                                                                                         |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **活動 \_追蹤 \_ 類型 \_ 設定 \_ CPU** (事件種類值為 10) <br/>          | CPU 設定事件。 [**SystemConfig \_ CPU**](systemconfig-cpu.md) MOF 類別會定義此事件的事件資料。                                                       |
| **活動 \_追蹤 \_ 類型 \_ 設定 \_ IDECHANNEL** (事件種類值為 23) <br/>   | 主要和次要 IDE 通道設定事件。 [**SystemConfig \_ IDEChannel**](systemconfig-idechannel.md) mof 類別 mof 類別會定義此事件的事件資料。 |
| **活動 \_追蹤 \_ 類型 \_ 設定 \_ IRQ** (事件種類值為 21) <br/>          | 中斷要求 (IRQ) 事件。 [**SystemConfig \_ IRQ**](systemconfig-irq.md) mof 類別 mof 類別會定義此事件的事件資料。                                       |
| **活動 \_追蹤 \_ 類型 \_ 設定 \_ LOGICALDISK** (事件種類值為 12) <br/>  | 邏輯磁片設定事件。 [**SystemConfig \_ LogDisk**](systemconfig-logdisk.md) mof 類別 mof 類別會定義此事件的事件資料。                            |
| **活動 \_追蹤 \_ 類型 \_ 設定 \_ NETINFO** (事件種類值為 17) <br/>      | 網路 iformation 事件。 [**SystemConfig \_ Network**](systemconfig-network.md) MOF 類別會定義此事件的事件資料。                                                |
| **活動 \_追蹤 \_ 類型 \_ CONFIG \_ NIC** (事件種類值為 13) <br/>          | NIC 設定事件。 [**SystemConfig \_ NIC**](systemconfig-nic.md) MOF 類別會定義此事件的事件資料。                                                       |
| **活動 \_追蹤 \_ 類型 \_ 設定 \_ PHYSICALDISK** (事件種類值為 11) <br/> | 實體磁片設定事件。 [**SystemConfig \_ PhyDisk**](systemconfig-phydisk.md) MOF 類別會定義此事件的事件資料。                                     |
| **活動 \_追蹤 \_ 類型 \_ CONFIG \_ PNP** (事件種類值為 22) <br/>          | 隨插即用事件。 [**SystemConfig \_ PNP**](systemconfig-pnp.md) mof 類別 MOF 類別會定義此事件的事件資料。                                                 |
| **活動 \_追蹤 \_ 類型 \_ CONFIG \_ POWER** (事件種類值為 16) <br/>        | 電源設定事件。 [**SystemConfig \_ 電源**](systemconfig-power.md)MOF 類別會定義此事件的事件資料。                                                   |
| **活動 \_追蹤 \_ 類型 \_ 設定 \_ 服務** (事件種類值為 15) <br/>     | 服務設定事件。 [**SystemConfig \_ Services**](systemconfig-services.md) MOF 類別會定義此事件的事件資料。                                          |
| **活動 \_追蹤 \_ 類型 \_ 設定 \_ 影片** (事件種類值為 14) <br/>        | 圖形配接器設定事件。 [**SystemConfig \_ Video**](systemconfig-video.md) MOF 類別會定義此事件的事件資料。                                        |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**SystemConfig \_ CPU**](systemconfig-cpu.md)
</dt> <dt>

[**SystemConfig \_ IDEChannel**](systemconfig-idechannel.md)
</dt> <dt>

[**SystemConfig \_ IRQ**](systemconfig-irq.md)
</dt> <dt>

[**SystemConfig \_ LogDisk**](systemconfig-logdisk.md)
</dt> <dt>

[**SystemConfig \_ 網路**](systemconfig-network.md)
</dt> <dt>

[**SystemConfig \_ NIC**](systemconfig-nic.md)
</dt> <dt>

[**SystemConfig \_ PhyDisk**](systemconfig-phydisk.md)
</dt> <dt>

[**SystemConfig \_ PNP**](systemconfig-pnp.md)
</dt> <dt>

[**SystemConfig \_ 電源**](systemconfig-power.md)
</dt> <dt>

[**SystemConfig \_ 服務**](systemconfig-services.md)
</dt> <dt>

[**SystemConfig \_ 影片**](systemconfig-video.md)
</dt> <dt>

[**SystemConfig \_ V0**](systemconfig-v0.md)
</dt> </dl>

 

 
