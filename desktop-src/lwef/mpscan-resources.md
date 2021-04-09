---
title: 'MPSCAN_RESOURCES 結構 (MpClient .h) '
description: 掃描操作期間傳遞的資源資訊。
ms.assetid: D97712A6-547D-44CC-B55D-039A5CCE20BF
keywords:
- MPSCAN_RESOURCES 結構舊版 Windows 環境功能
- PMPSCAN_RESOURCES 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPSCAN_RESOURCES
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69ee9ea259bca6bf66eb81fcd17b13d509d5a065
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935103"
---
# <a name="mpscan_resources-structure"></a>MPSCAN \_ 資源結構

掃描操作期間傳遞的資源資訊。

## <a name="syntax"></a>語法


```C++
typedef struct tagMPSCAN_RESOURCES {
  DWORD            dwResourceCount;
  PMPRESOURCE_INFO pResourceList;
} MPSCAN_RESOURCES, *PMPSCAN_RESOURCES;
```



## <a name="members"></a>成員

<dl> <dt>

**dwResourceCount**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

資源計數。

</dd> <dt>

**pResourceList**
</dt> <dd>

類型： **PMPRESOURCE \_ 資訊**

</dd> <dd>

資源的陣列。 請參閱 [**MPRESOURCE \_ 資訊**](mpresource-info.md)。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MPRESOURCE \_ 資訊**](mpresource-info.md)
</dt> </dl>

 

 





