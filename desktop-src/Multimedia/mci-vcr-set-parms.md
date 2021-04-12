---
title: 'MCI_VCR_SET_PARMS 結構 (Vcr) '
description: MCI \_ VCR \_ set \_ PARMS 結構包含適用于 vcd 燒錄機之 mci \_ SET 命令的參數。
ms.assetid: f55515f5-14f6-47e4-8be2-4524975fc950
keywords:
- MCI_VCR_SET_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_VCR_SET_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0066adf80446843fe5a3e1e3defbb2109484cbb6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385138"
---
# <a name="mci_vcr_set_parms-structure"></a>MCI \_ VCR \_ SET \_ PARMS 結構

**Mci \_ VCR \_ set \_ PARMS** 結構包含適用于 vcd 燒錄機之 [**mci \_ SET**](mci-set.md)命令的參數。

## <a name="syntax"></a>語法


```C++
typedef struct tagMCI_VCR_SET_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
  DWORD     dwTimeMode;
  DWORD     dwRecordFormat;
  DWORD     dwCounterFormat;
  DWORD     dwIndex;
  DWORD     dwTracking;
  DWORD     dwSpeed;
  DWORD     dwLength;
  DWORD     dwCounter;
  DWORD     dwClock;
  DWORD     dwPauseTimeout;
  DWORD     dwPrerollDuration;
  DWORD     dwPostrollDuration;
} MCI_VCR_SET_PARMS;
```



## <a name="members"></a>成員

<dl> <dt>

**dwCallback**
</dt> <dd>

低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。

</dd> <dt>

**dwTimeFormat**
</dt> <dd>

目前的時間格式。

</dd> <dt>

**dwAudio**
</dt> <dd>

未使用。

</dd> <dt>

**dwTimeMode**
</dt> <dd>

常數，指定裝置所使用的時間來源。 時間來源是記錄在磁帶上的時間碼，或是裝置中有意義磁帶移動的計數器。

</dd> <dt>

**dwRecordFormat**
</dt> <dd>

錄製速率。

</dd> <dt>

**dwCounterFormat**
</dt> <dd>

新計數器時間值的格式。

</dd> <dt>

**dwIndex**
</dt> <dd>

螢幕上顯示的內容。

</dd> <dt>

**dwTracking**
</dt> <dd>

追蹤 VCR 播放速率時使用的速度調整。

</dd> <dt>

**dwSpeed**
</dt> <dd>

裝置用來作為整數的播放速度。 正常播放速度為1000、雙速度為2000，而半速度為500。

</dd> <dt>

**dwLength**
</dt> <dd>

裝置無法偵測長度時的磁帶長度。

</dd> <dt>

**dwCounter**
</dt> <dd>

新計數器值。

</dd> <dt>

**dwClock**
</dt> <dd>

新的時鐘時間。

</dd> <dt>

**dwPauseTimeout**
</dt> <dd>

Pause 命令的新超時值。

</dd> <dt>

**dwPrerollDuration**
</dt> <dd>

穩定 VCR 輸出所需的磁帶長度。

</dd> <dt>

**dwPostrollDuration**
</dt> <dd>

發出 [**mci \_ STOP**](mci-stop.md) 或 [**mci \_ PAUSE**](mci-pause.md) 命令時，煞車 VCR 傳輸所需的磁帶長度。

</dd> </dl>

## <a name="remarks"></a>備註

將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vcr</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Mci**](mci.md)
</dt> <dt>

[**MCI 結構**](mci-structures.md)
</dt> <dt>

[**MCI \_ 暫停**](mci-pause.md)
</dt> <dt>

[**MCI \_ 組**](mci-set.md)
</dt> <dt>

[**MCI \_ 停止**](mci-stop.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

