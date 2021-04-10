---
title: 'MCI_SEQ_SET_PARMS 結構 (Mciapi .h) '
description: MCI \_ SEQ \_ set \_ PARMS 結構包含適用于 \_ MIDI sequencer 裝置之 MCI SET 命令的資訊。
ms.assetid: 71638a92-c1d6-474b-bc97-ea63ca586aaa
keywords:
- MCI_SEQ_SET_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_SEQ_SET_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 879dd575918a33676e3ba73bd2a8f6212e3dc412
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934032"
---
# <a name="mci_seq_set_parms-structure"></a>MCI \_ SEQ \_ SET \_ PARMS 結構

**Mci \_ SEQ \_ set \_ PARMS** 結構包含適用于 MIDI sequencer 裝置之 [**MCI \_ SET**](mci-set.md)命令的資訊。

## <a name="syntax"></a>語法


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwTimeFormat;
  DWORD     dwAudio;
  DWORD     dwTempo;
  DWORD     dwPort;
  DWORD     dwSlave;
  DWORD     dwMaster;
  DWORD     dwOffset;
} MCI_SEQ_SET_PARMS;
```



## <a name="members"></a>成員

<dl> <dt>

**dwCallback**
</dt> <dd>

低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。

</dd> <dt>

**dwTimeFormat**
</dt> <dd>

Sequencer 的時間格式。

</dd> <dt>

**dwAudio**
</dt> <dd>

音訊輸出通道。

</dd> <dt>

**dwTempo**
</dt> <dd>

節奏。

</dd> <dt>

**dwPort**
</dt> <dd>

連接埠。

</dd> <dt>

**dwSlave**
</dt> <dd>

排序器針對次級作業所使用的同步處理類型。

</dd> <dt>

**dwMaster**
</dt> <dd>

排序器針對主要作業所使用的同步處理類型。

</dd> <dt>

**dwOffset**
</dt> <dd>

資料位移。

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

[**Mci**](mci.md)
</dt> <dt>

[**MCI 結構**](mci-structures.md)
</dt> <dt>

[**MCI \_ 組**](mci-set.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

