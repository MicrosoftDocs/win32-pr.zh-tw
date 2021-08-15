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
ms.openlocfilehash: dd70b442e7179d516d2e9c60b81e6c52b0f696f5719a255871e8687773bf71ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747347"
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
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MPRESOURCE \_ 資訊**](mpresource-info.md)
</dt> </dl>

 

 





