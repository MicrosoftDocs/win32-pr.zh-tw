---
title: 'MPSCAN_TYPE 列舉 (MpClient .h) '
description: 執行的掃描類型。
ms.assetid: 980A80FD-FF02-4338-B7FB-DAA141F65E89
keywords:
- MPSCAN_TYPE 列舉舊版 Windows 環境功能
- PMPSCAN_TYPE 列舉指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPSCAN_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56906bfc9ad57f93bac4c8b8c27360b5ade9592ac33efe39574fe8890299e13a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747129"
---
# <a name="mpscan_type-enumeration"></a>MPSCAN \_ 類型列舉

執行的掃描類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMPSCAN_TYPE { 
  MPSCAN_TYPE_UNKNOWN   = 0,
  MPSCAN_TYPE_QUICK     = 1,
  MPSCAN_TYPE_FULL      = 2,
  MPSCAN_TYPE_RESOURCE  = 3,
  MPSCAN_TYPE_MAXVALUE  = 3
} MPSCAN_TYPE, *PMPSCAN_TYPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="MPSCAN_TYPE_UNKNOWN"></span><span id="mpscan_type_unknown"></span>**未知的 MPSCAN \_ 類型 \_**
</dt> <dd>

僅供內部使用。

</dd> <dt>

<span id="MPSCAN_TYPE_QUICK"></span><span id="mpscan_type_quick"></span>**MPSCAN \_ 類型 \_ 快速**
</dt> <dd>

掃描執行中的進程，以及惡意程式碼通常隱藏在系統中的各種 ASEP 點。

</dd> <dt>

<span id="MPSCAN_TYPE_FULL"></span><span id="mpscan_type_full"></span>**MPSCAN \_ 類型 \_ FULL**
</dt> <dd>

執行快速掃描，然後掃描系統的所有固定磁片磁碟機。

</dd> <dt>

<span id="MPSCAN_TYPE_RESOURCE"></span><span id="mpscan_type_resource"></span>**MPSCAN \_ 類型 \_ 資源**
</dt> <dd>

掃描特定的資源，例如檔案或資料夾。

</dd> <dt>

<span id="MPSCAN_TYPE_MAXVALUE"></span><span id="mpscan_type_maxvalue"></span>**MPSCAN \_ 類型 \_**
</dt> <dd>

可能的最大值。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



 

 





