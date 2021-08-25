---
title: 'MCI_VD_ESCAPE_PARMS 結構 (Mciapi .h) '
description: MCI \_ VD \_ ESCAPE \_ PARMS 結構包含傳送至裝置的命令，用於 VIDEODISC 裝置的 MCI \_ ESCAPE 命令。
ms.assetid: 7c735943-b67a-4be5-82b5-6a058349623e
keywords:
- MCI_VD_ESCAPE_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_VD_ESCAPE_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f9a0fef0e60168d4539756c741527d751fd726ab3d2472cdbaf3b080784e70c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783843"
---
# <a name="mci_vd_escape_parms-structure"></a>MCI \_ VD \_ ESCAPE \_ PARMS 結構

**Mci \_ VD \_ ESCAPE \_ PARMS** 結構包含傳送至裝置的命令，用於 videodisc 裝置的 [**MCI \_ ESCAPE**](mci-escape.md)命令。

## <a name="syntax"></a>語法


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpstrCommand;
} MCI_VD_ESCAPE_PARMS;
```



## <a name="members"></a>成員

<dl> <dt>

**dwCallback**
</dt> <dd>

低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。

</dd> <dt>

**lpstrCommand**
</dt> <dd>

要傳送至裝置的命令。

</dd> </dl>

## <a name="remarks"></a>備註

將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。

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

[**MCI \_ ESCAPE**](mci-escape.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

