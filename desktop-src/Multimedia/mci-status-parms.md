---
title: 'MCI_STATUS_PARMS 結構 (Mciapi .h) '
description: MCI \_ status \_ PARMS 結構包含 mci status 命令的資訊 \_ 。
ms.assetid: c4897b34-4184-46aa-af17-2127edfbf82d
keywords:
- MCI_STATUS_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_STATUS_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2685ec70f10dc8dcecb0149f3bcf1af6c9814dd360e8f7e185d31710c24d5527
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138094"
---
# <a name="mci_status_parms-structure"></a>MCI \_ 狀態 \_ PARMS 結構

**Mci \_ status \_ PARMS** 結構包含 [**mci \_ status**](mci-status.md)命令的資訊。

## <a name="syntax"></a>語法


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD_PTR dwReturn;
  DWORD     dwItem;
  DWORD     dwTrack;
} MCI_STATUS_PARMS;
```



## <a name="members"></a>成員

<dl> <dt>

**dwCallback**
</dt> <dd>

低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。

</dd> <dt>

**dwReturn**
</dt> <dd>

包含傳回的資訊。

</dd> <dt>

**dwItem**
</dt> <dd>

正在查詢的功能。

</dd> <dt>

**dwTrack**
</dt> <dd>

曲目的長度或數目。

</dd> </dl>

## <a name="remarks"></a>備註

您 \_ \_ 必須在 [**MciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定 MCI 狀態專案旗標，以驗證 **dwItem** 成員，其中應包含其中一個表示要求狀態資訊的常數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Mciapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**MCI 結構**](mci-structures.md)
</dt> <dt>

[**MCI \_ 狀態**](mci-status.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

