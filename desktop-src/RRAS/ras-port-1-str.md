---
title: 'RAS_PORT_1 結構 (Rassapi .h) '
description: RAS \_ 埠 \_ 1 結構包含 ras 埠的相關資訊。
ms.assetid: f226ef16-feb4-41e0-ba60-ddb2f0acd305
keywords:
- RAS_PORT_1 結構 RAS
- PRAS_PORT_1 結構指標 RAS
topic_type:
- apiref
api_name:
- RAS_PORT_1
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c73677b10743434bb9548c8d6add95100c4cf017d25bb44d7436e2f68b9ca4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673108"
---
# <a name="ras_port_1-structure"></a>RAS \_ 埠 \_ 1 結構

\[Windows Vista 不支援這個版本的 **RAS \_ 埠 \_ 1** 結構。 請改用 mprapi 中定義的較新 [**RAS \_ 埠 \_ 1**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_1) 。\]

**Ras \_ 埠 \_ 1** 結構包含 ras 埠的相關資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _RAS_PORT_1 {
  RAS_PORT_0                rasport0;
  DWORD                     LineCondition;
  DWORD                     HardwareCondition;
  DWORD                     LineSpeed;
  WORD                      NumStatistics;
  WORD                      NumMediaParms;
  DWORD                     SizeMediaParms;
  RAS_PPP_PROJECTION_RESULT ProjResult;
} RAS_PORT_1, *PRAS_PORT_1;
```



## <a name="members"></a>成員

<dl> <dt>

**rasport0**
</dt> <dd>

指定包含埠相關資訊的 [**RAS \_ 埠 \_ 0**](ras-port-0-str.md) 結構，例如埠的名稱、連接到埠的遠端使用者名稱等等。

</dd> <dt>

**LineCondition**
</dt> <dd>

指定埠的狀態。 這個成員可以是下列其中一個值。



| 值                                                                                                                                                                                            | 意義                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RAS_PORT_NON_OPERATIONAL"></span><span id="ras_port_non_operational"></span><dl> <dt>**RAS \_ 埠 \_ 無法 \_ 運作**</dt> </dl> | 埠無法運作。 檢查事件記錄檔中是否有伺服器回報的錯誤。<br/>                                                                         |
| <span id="RAS_PORT_DISCONNECTED"></span><span id="ras_port_disconnected"></span><dl> <dt>**RAS \_ 埠已 \_ 中斷連線**</dt> </dl>           | 埠目前已中斷連線。<br/>                                                                                                                         |
| <span id="RAS_PORT_CALLING_BACK"></span><span id="ras_port_calling_back"></span><dl> <dt>**RAS \_ 埠 \_ 回呼 \_**</dt> </dl>          | RAS 伺服器正在回呼 RAS 用戶端。<br/>                                                                                                              |
| <span id="RAS_PORT_LISTENING"></span><span id="ras_port_listening"></span><dl> <dt>**RAS \_ 埠 \_ 接聽**</dt> </dl>                    | 埠正在等候用戶端在中呼叫。<br/>                                                                                                                |
| <span id="RAS_PORT_AUTHENTICATING"></span><span id="ras_port_authenticating"></span><dl> <dt>**RAS \_ 埠 \_ 驗證**</dt> </dl>     | 伺服器正在驗證遠端用戶端。<br/>                                                                                           |
| <span id="RAS_PORT_AUTHENTICATED"></span><span id="ras_port_authenticated"></span><dl> <dt>**\_ \_ 已驗證的 RAS 埠**</dt> </dl>        | 遠端用戶端現在已經過驗證。<br/>                                                                                                                     |
| <span id="RAS_PORT_INITIALIZING"></span><span id="ras_port_initializing"></span><dl> <dt>**RAS \_ 埠 \_ 初始化**</dt> </dl>           | 連接到埠的裝置正在初始化。 當初始化完成時，埠的狀態將會變更為 RAS \_ 埠 \_ 接聽。<br/> |



 

</dd> <dt>

**HardwareCondition**
</dt> <dd>

指定下列其中一個值，表示連接到埠的裝置狀態。



| 值                                                                                                                                                                                                  | 意義                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="RAS_MODEM_OPERATIONAL"></span><span id="ras_modem_operational"></span><dl> <dt>**RAS \_ 數據機 \_ 操作**</dt> </dl>                 | 連接至此埠的數據機可正常運作，並已準備好接收用戶端呼叫。<br/> |
| <span id="RAS_MODEM_HARDWARE_FAILURE"></span><span id="ras_modem_hardware_failure"></span><dl> <dt>**RAS \_ 數據機 \_ 硬體 \_ 故障**</dt> </dl> | 連接至此埠的數據機有硬體問題。<br/>                              |



 

</dd> <dt>

**LineSpeed**
</dt> <dd>

指定電腦可以與埠通訊的速度（以秒為單位）。

</dd> <dt>

**NumStatistics**
</dt> <dd>

未使用這個成員。 RAS 管理功能（例如 [**RasAdminPortGetInfo**](rasadminportgetinfo.md) 函式）使用 [**ras \_ 埠 \_ 統計**](ras-port-statistics-str.md) 結構來傳回埠統計資料。

</dd> <dt>

**NumMediaParms**
</dt> <dd>

指定此埠的媒體專用參數數目。 針對序列媒體，這通常是出現在 SERIAL.INI 檔案中的值數目。

</dd> <dt>

**SizeMediaParms**
</dt> <dd>

指定所有媒體專用參數所需的緩衝區大小（以位元組為單位）。 [**RasAdminPortGetInfo**](rasadminportgetinfo.md)函式會傳回緩衝區，其中包含 [**RAS \_ 參數**](ras-parameters-str.md)結構的陣列，以及埠的媒體參數和值。

</dd> <dt>

**ProjResult**
</dt> <dd>

[**RAS \_ ppp \_ 投射 \_ 結果**](ras-ppp-projection-result-str.md)結構，指定此埠的 PPP 投射資訊。 當 RAS 用戶端連接到伺服器時，此結構會提供每個通訊協定的相關資訊。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 用戶端支援結束<br/>    | Windows XP<br/>                                                                |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                       |
| 標頭<br/>                   | <dl> <dt>Rassapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[遠端存取服務 (RAS) 總覽](about-remote-access-service.md)
</dt> <dt>

[RAS 伺服器管理結構](ras-server-administration-structures.md)
</dt> <dt>

[**RAS \_ 參數**](ras-parameters-str.md)
</dt> <dt>

[**RAS \_ 埠 \_ 0**](ras-port-0-str.md)
</dt> <dt>

[**RAS \_ 埠 \_ 統計資料**](ras-port-statistics-str.md)
</dt> <dt>

[**RAS \_ PPP \_ 投射 \_ 結果**](ras-ppp-projection-result-str.md)
</dt> <dt>

[**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md)
</dt> <dt>

[**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





