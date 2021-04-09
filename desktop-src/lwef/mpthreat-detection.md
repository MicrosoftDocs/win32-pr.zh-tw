---
title: 'MPTHREAT_DETECTION 列舉 (MpClient .h) '
description: 可能是已知的錯誤威脅偵測類型。
ms.assetid: 14FCA9BD-A9A1-488B-B8E8-88DE0DF18F27
keywords:
- MPTHREAT_DETECTION 列舉舊版 Windows 環境功能
- PMPTHREAT_DETECTION 列舉指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPTHREAT_DETECTION
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86edc0e1ca4ee130f2a2a4a678447771f1ae40ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685784"
---
# <a name="mpthreat_detection-enumeration"></a>MPTHREAT \_ 偵測列舉

可能是已知的錯誤威脅偵測類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMPTHREAT_DETECTION { 
  MP_THREAT_DETECTION_CONCRETE    = 0,
  MP_THREAT_DETECTION_HEURISTIC   = 1,
  MP_THREAT_DETECTION_GENERIC     = 2,
  MP_THREAT_DETECTION_SUSPICIOUS  = 4,
  MP_THREAT_DETECTION_FASTPATH    = 8
} MPTHREAT_DETECTION, *PMPTHREAT_DETECTION;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="MP_THREAT_DETECTION_CONCRETE"></span><span id="mp_threat_detection_concrete"></span>**MP \_ 威脅 \_ 偵測 \_ 實體**
</dt> <dd>

經由具體簽章偵測到威脅。

</dd> <dt>

<span id="MP_THREAT_DETECTION_HEURISTIC"></span><span id="mp_threat_detection_heuristic"></span>**MP \_ 威脅 \_ 偵測 \_ 啟發學習法**
</dt> <dd>

透過啟發學習法偵測到威脅。

</dd> <dt>

<span id="MP_THREAT_DETECTION_GENERIC"></span><span id="mp_threat_detection_generic"></span>**MP \_ 威脅 \_ 偵測 \_ 泛型**
</dt> <dd>

透過泛型簽章偵測到威脅。

</dd> <dt>

<span id="MP_THREAT_DETECTION_SUSPICIOUS"></span><span id="mp_threat_detection_suspicious"></span>**MP \_ 威脅 \_ 偵測 \_ 可疑**
</dt> <dd>

透過行為監視偵測到威脅。

</dd> <dt>

<span id="MP_THREAT_DETECTION_FASTPATH"></span><span id="mp_threat_detection_fastpath"></span>**MP \_ 威脅 \_ 偵測 \_ FASTPATH**
</dt> <dd>

透過 fastpath 偵測到威脅。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



 

 





