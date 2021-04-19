---
description: 埠 \_ 資訊 \_ 2 結構會識別支援的印表機埠。
ms.assetid: 93675294-61d4-40e4-b84c-f252978e0285
title: 'PORT_INFO_2 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PORT_INFO_2
- _PORT_INFO_2A
- _PORT_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 1d2186193318387bb6e37a228bd4d2fd64eca6b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984592"
---
# <a name="port_info_2-structure"></a>埠 \_ 資訊 \_ 2 結構

**埠 \_ 資訊 \_ 2** 結構會識別支援的印表機埠。

## <a name="syntax"></a>語法


```C++
typedef struct _PORT_INFO_2 {
  LPTSTR pPortName;
  LPTSTR pMonitorName;
  LPTSTR pDescription;
  DWORD  fPortType;
  DWORD  Reserved;
} PORT_INFO_2, *PPORT_INFO_2;
```



## <a name="members"></a>成員

<dl> <dt>

**pPortName**
</dt> <dd>

識別支援之印表機埠 (以 null 終止的字串指標，例如 "LPT1：" ) 。

</dd> <dt>

**pMonitorName**
</dt> <dd>

識別已安裝的監視器 (之以 null 結束的字串指標，例如「PJL 監視器」 ) 。 這可以是 **Null**。

</dd> <dt>

**pDescription**
</dt> <dd>

以 null 終止的字串指標，此字串會更詳細地描述埠 (例如，如果 **pPortName** 是 "LPT1："， **pDescription** 是 "printer port" ) 。 這可以是 **Null**。

</dd> <dt>

**fPortType**
</dt> <dd>

描述埠類型的位元遮罩。 這個成員可以是下列值的組合：

<dl><span id="PORT_TYPE_WRITE"></span><span id="port_type_write"></span><dt>

**埠 \_ 類型 \_ 寫入**
</dt><span id="PORT_TYPE_READ"></span><span id="port_type_read"></span><dt>

**埠 \_ 類型 \_ 讀取**
</dt><span id="PORT_TYPE_REDIRECTED"></span><span id="port_type_redirected"></span><dt>

**重新 \_ 導向的埠類型 \_**
</dt><span id="PORT_TYPE_NET_ATTACHED"></span><span id="port_type_net_attached"></span><dt>

**連接的埠 \_ 類型 \_ NET \_**
</dt> </dl> </dd> <dt>

**已保留**
</dt> <dd>

保護必須為零。

</dd> </dl>

## <a name="remarks"></a>備註

如果已安裝多個支援相同埠的監視器，請在呼叫 [**EnumPorts**](enumports.md)時使用 **埠 \_ 資訊 \_ 2** 結構。

您可以查詢 **fPortType** 成員，以判斷埠的相關資訊。 請注意，通訊埠設定不會影響印表機資訊 (的 [印表機 [**\_ 資訊 \_**](printer-info-2.md) ]) 的 **屬性** 成員所傳回的印表機屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **\_ 埠 \_ 資訊 \_ 2w** (Unicode) 和 **\_ 埠 \_ 資訊 \_ 2a** (ANSI) <br/>                                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 結構](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPorts**](enumports.md)
</dt> </dl>

 

 




