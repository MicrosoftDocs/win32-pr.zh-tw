---
title: 'MCI_VD_PLAY_PARMS 結構 (Mciapi .h) '
description: MCI \_ VD \_ PLAY \_ PARMS 結構包含 VIDEODISC 裝置的 mci PLAY 命令的位置和速度資訊 \_ 。
ms.assetid: 9fa8418f-3f69-4a9c-b23e-7d2e2c75c7af
keywords:
- MCI_VD_PLAY_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_VD_PLAY_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62c2aef6915d1e3cc325d5b9f8e1c7fe176a878c2d84080b5f8a77eaf034afc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783863"
---
# <a name="mci_vd_play_parms-structure"></a>MCI \_ VD \_ PLAY \_ PARMS 結構

**Mci \_ VD \_ PLAY \_ PARMS** 結構包含 videodisc 裝置的 [**mci \_ PLAY**](mci-play.md)命令的位置和速度資訊。

## <a name="syntax"></a>語法


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwSpeed;
} MCI_VD_PLAY_PARMS;
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

</dd> <dt>

**dwSpeed**
</dt> <dd>

每秒畫面格的播放速度。

</dd> </dl>

## <a name="remarks"></a>備註

將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。

如果您不是使用擴充的資料成員，您可以使用 [**mci \_ play \_ PARMS**](mci-play-parms.md) 結構，而不是 **mci \_ VD \_ PLAY \_ PARMS** 。

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

[**MCI \_ 播放**](mci-play.md)
</dt> <dt>

[**MCI \_ PLAY \_ PARMS**](mci-play-parms.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

