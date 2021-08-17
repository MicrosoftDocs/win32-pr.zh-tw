---
title: 'RAS_SERVER_0 結構 (Rassapi .h) '
description: RasAdminServerGetInfo 函 \_ 式 \_ 會使用 ras 伺服器0結構來傳回在 RAS 伺服器上設定之埠的相關資訊。
ms.assetid: 8818ad68-b528-45fe-9ff4-eea194259f25
keywords:
- RAS_SERVER_0 結構 RAS
- PRAS_SERVER_0 結構指標 RAS
topic_type:
- apiref
api_name:
- RAS_SERVER_0
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbb7a135fd6f8d1d77b59d1085460d51ad5357e47ca1a050e3d1ba6fd89461c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789382"
---
# <a name="ras_server_0-structure"></a>RAS \_ 伺服器 \_ 0 結構

\[Windows Vista 不支援 **RAS \_ 伺服器 \_ 0** 結構。\]

[**RasAdminServerGetInfo**](rasadminservergetinfo.md)函式會使用 **ras \_ 伺服器 \_ 0** 結構來傳回在 RAS 伺服器上設定之埠的相關資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _RAS_SERVER_0 {
  WORD  TotalPorts;
  WORD  PortsInUse;
  DWORD RasVersion;
} RAS_SERVER_0, *PRAS_SERVER_0;
```



## <a name="members"></a>成員

<dl> <dt>

**TotalPorts**
</dt> <dd>

指定可供遠端用戶端連接的 RAS 伺服器上設定的埠總數。 例如，如果設定用來撥入伺服器的埠總數為四個，但其中一個埠目前用於撥出，則 **TotalPorts** 為三個。

</dd> <dt>

**PortsInUse**
</dt> <dd>

指定遠端用戶端目前正在使用的埠數目。

</dd> <dt>

**RasVersion**
</dt> <dd>

指定 RAS 伺服器的版本。 使用此資訊來取得版本特定的動作。 這個成員是下列其中一個值。



| 值                                                                                                                                                                  | 意義                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="RASDOWNLEVEL"></span><span id="rasdownlevel"></span><dl> <dt>**RASDOWNLEVEL**</dt> </dl>              | 表示 LAN Manager 1.0 版 RAS 伺服器。<br/>                      |
| <span id="RASADMIN_35"></span><span id="rasadmin_35"></span><dl> <dt>**RASADMIN \_ 35**</dt> </dl>                | 指出 Windows NT Server 3.51 及較早的 RAS 伺服器或用戶端。<br/> |
| <span id="RASADMIN_CURRENT"></span><span id="rasadmin_current"></span><dl> <dt>**RASADMIN \_ 目前**</dt> </dl> | 指出 Windows NT 4.0 RAS 伺服器或用戶端。<br/>                     |



 

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

[**RasAdminServerGetInfo**](rasadminservergetinfo.md)
</dt> </dl>

 

 





