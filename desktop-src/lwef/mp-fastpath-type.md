---
title: 'MP_FASTPATH_TYPE 列舉 (MpClient .h) '
description: FastPath 類型。
ms.assetid: BD72228F-DCC0-435E-A408-BD7FB02E55E1
keywords:
- MP_FASTPATH_TYPE 列舉舊版 Windows 環境功能
- PMP_FASTPATH_TYPE 列舉指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MP_FASTPATH_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7bd9a8ce26f930a35c9c4fa547234b0d55b0b588b60881cf8aae31621e9a83a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247443"
---
# <a name="mp_fastpath_type-enumeration"></a>MP \_ FASTPATH \_ 類型列舉

FastPath 類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMP_FASTPATH_TYPE { 
  MP_FASTPATH_UNKNOWN   = 0,
  MP_FASTPATH_VDM       = 1,
  MP_FASTPATH_DISABLED  = 2
} MP_FASTPATH_TYPE, *PMP_FASTPATH_TYPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="MP_FASTPATH_UNKNOWN"></span><span id="mp_fastpath_unknown"></span>**MP \_ FASTPATH \_ 不明**
</dt> <dd>

未知。

</dd> <dt>

<span id="MP_FASTPATH_VDM"></span><span id="mp_fastpath_vdm"></span>**MP \_ FASTPATH \_ VDM**
</dt> <dd>

VDM 更新。

</dd> <dt>

<span id="MP_FASTPATH_DISABLED"></span><span id="mp_fastpath_disabled"></span>**MP \_ FASTPATH \_ 已停用**
</dt> <dd>

簽章停用通知。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



 

 





