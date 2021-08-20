---
title: 'MCI_SET_PARMS 結構 (Mciapi .h) '
description: MCI \_ set \_ PARMS 結構包含 mci set 命令的資訊 \_ 。
ms.assetid: 58811a0f-dc89-4303-b2b2-c98933ebab80
keywords:
- MCI_SET_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_SET_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10c223534410b7e5a0543683c354728e0d5093f38ad0a2582a047a2a5362faae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117986210"
---
# <a name="mci_set_parms-structure"></a>MCI \_ 設定 \_ PARMS 結構

**Mci \_ set \_ PARMS** 結構包含 [**mci \_ set**](mci-set.md)命令的資訊。

## <a name="syntax"></a>語法


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
} MCI_SET_PARMS;
```



## <a name="members"></a>成員

<dl> <dt>

**dwCallback**
</dt> <dd>

低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。

</dd> <dt>

**dwTimeFormat**
</dt> <dd>

裝置的時間格式。

</dd> <dt>

**dwAudio**
</dt> <dd>

音訊輸出通道。

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

[**MCI \_ 組**](mci-set.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

