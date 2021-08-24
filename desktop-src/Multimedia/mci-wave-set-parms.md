---
title: 'MCI_WAVE_SET_PARMS 結構 (Mciapi .h) '
description: MCI \_ WAVE \_ set PARMS 結構包含適用于 wave \_ 音訊裝置之 mci \_ SET 命令的資訊。
ms.assetid: 24c26124-274f-457e-ab87-887f3bcffce3
keywords:
- MCI_WAVE_SET_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_WAVE_SET_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85508ec493ecdc38825b90877e608683fe6c0bb7c099365c187a434890c605d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783748"
---
# <a name="mci_wave_set_parms-structure"></a>MCI \_ WAVE \_ SET \_ PARMS 結構

**Mci \_ WAVE \_ set \_ PARMS** 結構包含適用于 wave 音訊裝置之 [**mci \_ SET**](mci-set.md)命令的資訊。

## <a name="syntax"></a>語法


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
  UINT      wInput;
  UINT      wOutput;
  WORD      wFormatTag;
  WORD      wReserved2;
  WORD      nChannels;
  WORD      wReserved3;
  DWORD     nSamplesPerSec;
  DWORD     nAvgBytesPerSec;
  WORD      nBlockAlign;
  WORD      wReserved4;
  WORD      wBitsPerSample;
  WORD      wReserved5;
} MCI_WAVE_SET_PARMS;
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

音訊輸出的頻道號碼。 通常用來開啟或關閉通道。

</dd> <dt>

**wInput**
</dt> <dd>

音訊輸入通道。

</dd> <dt>

**wOutput**
</dt> <dd>

要使用的輸出裝置。 例如，如果系統有兩個已安裝的音效卡，則此值可能是2。

</dd> <dt>

**wFormatTag**
</dt> <dd>

波形音訊資料的格式，例如 WAVE \_ 格式 \_ PCM。 可能的值定義于 Mmreg 中。

</dd> <dt>

**wReserved2**
</dt> <dd>

保留的。

</dd> <dt>

**nChannels**
</dt> <dd>

Mono (1) 或身歷聲 (2) 。

</dd> <dt>

**wReserved3**
</dt> <dd>

保留的。

</dd> <dt>

**nSamplesPerSec**
</dt> <dd>

每秒樣本數。

</dd> <dt>

**nAvgBytesPerSec**
</dt> <dd>

取樣率（位元組/秒）。

</dd> <dt>

**nBlockAlign**
</dt> <dd>

封鎖資料的對齊。

</dd> <dt>

**wReserved4**
</dt> <dd>

保留的。

</dd> <dt>

**wBitsPerSample**
</dt> <dd>

每個樣本的位數。

</dd> <dt>

**wReserved5**
</dt> <dd>

保留的。

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

 

