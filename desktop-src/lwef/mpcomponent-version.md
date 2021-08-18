---
title: 'MPCOMPONENT_VERSION 結構 (MpClient .h) '
description: 個別元件的版本和更新時間。
ms.assetid: 43468230-EE13-4630-8C09-F8DF983EF748
keywords:
- MPCOMPONENT_VERSION 結構舊版 Windows 環境功能
- PMPCOMPONENT_VERSION 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPCOMPONENT_VERSION
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6092fe2f3ec7ba921b1ef3adfc9355feeeae67f2381836056f2af65b276921cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976068"
---
# <a name="mpcomponent_version-structure"></a>MPCOMPONENT \_ 版本結構

個別元件的版本和更新時間。

## <a name="syntax"></a>語法


```C++
typedef struct tagMPCOMPONENT_VERSION {
  ULONGLONG      Version;
  ULARGE_INTEGER UpdateTime;
} MPCOMPONENT_VERSION, *PMPCOMPONENT_VERSION;
```



## <a name="members"></a>成員

<dl> <dt>

**版本**
</dt> <dd>

類型： **ULONGLONG**

</dd> <dd>

版本欄位。 每個 **單字** 都代表主要、次要、組建和修訂。

</dd> <dt>

**UpdateTime**
</dt> <dd>

類型： **ULARGE \_ 整數**

</dd> <dd>

元件的上次更新時間（以 **FILETIME** 格式）。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



 

 





