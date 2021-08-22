---
description: 這個類別是網路事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: afa994ef-dd1c-4909-a6cd-7021be4fff40
title: SystemConfig_Network 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Network
- SystemConfig_Network.TcbTablePartitions
- SystemConfig_Network.MaxHashTableSize
- SystemConfig_Network.MaxUserPort
- SystemConfig_Network.TcpTimedWaitDelay
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6b196e8c1ad5a997642cc48491e9d1a4b5e73bc26db71d5ea5258f7cf162a00a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069688"
---
# <a name="systemconfig_network-class"></a>SystemConfig \_ Network 類別

這個類別是網路事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType(17), EventTypeName("Network")]
class SystemConfig_Network : SystemConfig
{
  uint32 TcbTablePartitions;
  uint32 MaxHashTableSize;
  uint32 MaxUserPort;
  uint32 TcpTimedWaitDelay;
};
```

## <a name="members"></a>成員

**SystemConfig \_ Network** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**SystemConfig \_ Network** 類別具有這些屬性。

<dl> <dt>

**MaxHashTableSize**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (2) 
</dt> </dl>

儲存 (TCBs) 之 TCP 控制區塊的雜湊表大小。 TCP 會將控制區塊儲存在雜湊表中，以便快速找到它們。

</dd> <dt>

**MaxUserPort**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (3) 
</dt> </dl>

當應用程式向系統要求可用的使用者埠時，TCP 可指派的最高埠號碼。 一般來說，短暫) 的暫時埠 (會配置給埠號碼1024到5000。

TCP 可指派的最高使用者埠號碼值是由登錄設定所控制。 如需詳細資訊，請參閱 [MaxUserPort](/previous-versions/windows/it-pro/windows-2000-server/cc938196(v=technet.10))。

</dd> <dt>

**TcbTablePartitions**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (1) 
</dt> </dl>

傳輸控制區塊資料表中的資料分割數目。 分割傳輸控制區塊資料表可將資料表存取的爭用降至最低。 這在多處理器系統上特別有用。

</dd> <dt>

**TcpTimedWaitDelay**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (4) 
</dt> </dl>

必須經過多久的時間，TCP 才能釋放關閉的連線並重複使用其資源。 結束和釋放之間的此間隔稱為「 \_ 等候狀態」或「2MSL」狀態。 在這段期間內，您可以在用戶端和伺服器之間重新開啟連接，而不需要建立新的連接。

IETF 所發佈的 RFC 793，會要求 TCP 將間隔維持在至少等於最大區段存留期 (2MSL) 網路的間隔。 當連接釋出時，其通訊端配對和 TCP 控制區塊 (TCB) 可用來支援另一個連線。 根據預設，MSL 定義為120秒，而此專案的值等於兩個 Msls.contentitem 或4分鐘。 如需詳細資訊，請參閱 [RFC 793](https://tools.ietf.org/html/rfc973)。

使用登錄設定來縮減這個專案的值，可讓 TCP 更快釋放關閉的連線，為新的連接提供更多資源。 但是，如果值太低，TCP 可能會在連接完成之前釋出連線資源，要求伺服器使用額外的資源來重新建立連接。

一般來說，TCP 不會釋放關閉的連線，直到這個專案的值到期為止。 但是，如果 (TCBs) ，TCP 會在此值過期之前釋放連接。 系統所建立的 TCBs 數目是由登錄設定所控制。 如需詳細資訊，請參閱 [MaxFreeTCBs](/previous-versions/windows/it-pro/windows-2000-server/cc938178(v=technet.10))。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 
