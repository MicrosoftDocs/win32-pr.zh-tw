---
title: 'MPTHREAT_TYPE 列舉 (MpClient .h) '
description: 可能的威脅類型。
ms.assetid: 56061F12-AA89-4203-BED4-99613E24002A
keywords:
- MPTHREAT_TYPE 列舉舊版 Windows 環境功能
- PMPTHREAT_TYPE 列舉指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPTHREAT_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b858501603b67451db9b565609d0c263040d2186cf44d91646e6df6ce3871ea1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247139"
---
# <a name="mpthreat_type-enumeration"></a>MPTHREAT \_ 類型列舉

可能的威脅類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMPTHREAT_TYPE { 
  MPTHREAT_TYPE_KNOWNBAD   = 0,
  MPTHREAT_TYPE_BEHAVIOR   = 1,
  MPTHREAT_TYPE_UNKNOWN    = 2,
  MPTHREAT_TYPE_KNOWNGOOD  = 3,
  MPTHREAT_TYPE_NIS        = 4,
  MPTHREAT_TYPE_MAXVALUE   = 4
} MPTHREAT_TYPE, *PMPTHREAT_TYPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="MPTHREAT_TYPE_KNOWNBAD"></span><span id="mpthreat_type_knownbad"></span>**MPTHREAT \_ 類型 \_ KNOWNBAD**
</dt> <dd>

透過簽章偵測到已知的不良威脅。

</dd> <dt>

<span id="MPTHREAT_TYPE_BEHAVIOR"></span><span id="mpthreat_type_behavior"></span>**MPTHREAT \_ 類型 \_ 行為**
</dt> <dd>

透過行為監視偵測到可疑的威脅。

</dd> <dt>

<span id="MPTHREAT_TYPE_UNKNOWN"></span><span id="mpthreat_type_unknown"></span>**未知的 MPTHREAT \_ 類型 \_**
</dt> <dd>

未知的威脅 (非分類的) 。

</dd> <dt>

<span id="MPTHREAT_TYPE_KNOWNGOOD"></span><span id="mpthreat_type_knowngood"></span>**MPTHREAT \_ 類型 \_ KNOWNGOOD**
</dt> <dd>

已知的良好威脅。

</dd> <dt>

<span id="MPTHREAT_TYPE_NIS"></span><span id="mpthreat_type_nis"></span>**MPTHREAT \_ 類型 \_ NIS**
</dt> <dd>

NIS 威脅偵測。

</dd> <dt>

<span id="MPTHREAT_TYPE_MAXVALUE"></span><span id="mpthreat_type_maxvalue"></span>**MPTHREAT \_ 類型 \_**
</dt> <dd>

可能的最大值。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



 

 





