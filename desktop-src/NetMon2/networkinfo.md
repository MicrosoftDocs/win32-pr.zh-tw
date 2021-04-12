---
description: NETWORKINFO 結構描述 NIC。
ms.assetid: 40169409-7de5-44d1-8dff-dfa9f647edc9
title: 'NETWORKINFO 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NETWORKINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 8917966d2e090417a95a9ca20158c6c5935bda3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695395"
---
# <a name="networkinfo-structure"></a>NETWORKINFO 結構

NETWORKINFO 結構描述 NIC。

## <a name="syntax"></a>語法


```C++
typedef struct _NETWORKINFO {
  BYTE    PermanentAddr[6];
  BYTE    CurrentAddr[6];
  ADDRESS OtherAddress;
  DWORD   LinkSpeed;
  DWORD   MacType;
  DWORD   MaxFrameSize;
  DWORD   Flags;
  DWORD   TimestampScaleFactor;
  BYTE    NodeName[32];
  BOOL    PModeSupported;
  BYTE    Comment[ADAPTER_COMMENT_LENGTH];
} NETWORKINFO, *LPNETWORKINFO;
```



## <a name="members"></a>成員

<dl> <dt>

**PermanentAddr**
</dt> <dd>

永久 MAC 位址。

</dd> <dt>

**CurrentAddr**
</dt> <dd>

目前的 MAC 位址。

</dd> <dt>

**OtherAddress**
</dt> <dd>

其他支援此 (的位址，例如 IP、IPX) 。

</dd> <dt>

**LinkSpeed**
</dt> <dd>

連結速度（以 Mbps 為單位）。

</dd> <dt>

**MacType**
</dt> <dd>

媒體類型。

</dd> <dt>

**Messagingfactorysettings.amqptransportsettings.maxframesize**
</dt> <dd>

允許的框架大小上限。

</dd> <dt>

**旗標**
</dt> <dd>

此參數可以是下列其中一個資訊旗標：



| 值                                                                                                                                                                                                                                       | 意義                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NETWORKINFO_FLAGS_PMODE_NOT_SUPPORTED"></span><span id="networkinfo_flags_pmode_not_supported"></span><dl> <dt>**\_ \_ \_ 不支援 NETWORKINFO 旗標 PMODE \_**</dt> </dl>    | 網路卡不支援混合模式，這表示它只會捕捉本質為廣播或只涉及本機電腦的流量。<br/> |
| <span id="NETWORKINFO_FLAGS_RAS"></span><span id="networkinfo_flags_ras"></span><dl> <dt>**NETWORKINFO \_ 旗標 \_ RAS**</dt> </dl>                                                      | 這是一張虛擬網路卡，也就是 RAS (遠端存取服務器) 透過數據機或另一張網路卡連接。<br/>                                        |
| <span id="NETWORKINFO_FLAGS_REMOTE_CARD"></span><span id="networkinfo_flags_remote_card"></span><dl> <dt>**NETWORKINFO \_ 旗標 \_ 遠端 \_ 卡片**</dt> </dl>                             | 網路卡不在本機電腦上，而是在本機電腦 bequest 的遠端電腦上進行捕獲。<br/>                                      |
| <span id="NETWORKINFO_FLAGS_REMOTE_NAL"></span><span id="networkinfo_flags_remote_nal"></span><dl> <dt>**NETWORKINFO \_ 旗標 \_ 遠端 \_ NAL**</dt> </dl>                                | 目前請勿使用。<br/>                                                                                                                                          |
| <span id="NETWORKINFO_FLAGS_REMOTE_NAL_CONNECTED"></span><span id="networkinfo_flags_remote_nal_connected"></span><dl> <dt>**\_已連線的 NETWORKINFO 旗標 \_ 遠端 \_ NAL \_**</dt> </dl> | 目前請勿使用。<br/>                                                                                                                                          |



 

</dd> <dt>

**TimestampScaleFactor**
</dt> <dd>

例如，值為1表示1/1 毫秒、10表示1/10 毫秒、100表示 1/100 ms 等等。

</dd> <dt>

**NodeName**
</dt> <dd>

遠端工作站的名稱。

</dd> <dt>

**PModeSupported**
</dt> <dd>

NIC P 模式支援指標。

</dd> <dt>

**註解**
</dt> <dd>

介面卡批註欄位。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



 

 




