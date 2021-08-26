---
title: 'MCI_RECORD_PARMS 結構 (Mciapi .h) '
description: MCI \_ 記錄 \_ PARMS 結構包含 mci 記錄命令的位置資訊 \_ 。
ms.assetid: 5d502cf8-3963-49d6-b515-d26e19195322
keywords:
- MCI_RECORD_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_RECORD_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c531b5b186a6119a22cafc4e252424ace2e388b2545461b440cd7957694494b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039078"
---
# <a name="mci_record_parms-structure"></a>MCI \_ 記錄 \_ PARMS 結構

**Mci \_ 記錄 \_ PARMS** 結構包含 [**mci \_ 記錄**](mci-record.md)命令的位置資訊。

## <a name="syntax"></a>語法


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
} MCI_RECORD_PARMS;
```



## <a name="members"></a>成員

<dl> <dt>

**dwCallback**
</dt> <dd>

低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。

</dd> <dt>

**dwFrom**
</dt> <dd>

要播放的位置。

</dd> <dt>

**dwTo**
</dt> <dd>

要播放的位置。

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

[**MCI \_ 記錄**](mci-record.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

