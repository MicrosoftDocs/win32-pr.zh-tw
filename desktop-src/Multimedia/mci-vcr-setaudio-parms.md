---
title: 'MCI_VCR_SETAUDIO_PARMS 結構 (Vcr) '
description: MCI \_ VCR \_ SETAUDIO \_ PARMS 結構包含適用于 \_ video-卡帶燒錄機之 mci SETAUDIO 命令的參數。
ms.assetid: 328d8e63-7ddd-4c9b-85d6-2e56fd802dbc
keywords:
- MCI_VCR_SETAUDIO_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_VCR_SETAUDIO_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa07d4cf8b88eb246019bf18dd1c1328413718a70b17ebb16e27606958473f5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117802956"
---
# <a name="mci_vcr_setaudio_parms-structure"></a>MCI \_ VCR \_ SETAUDIO \_ PARMS 結構

**Mci \_ VCR \_ SETAUDIO \_ PARMS** 結構包含適用于 video-卡帶燒錄機之 [**mci \_ SETAUDIO**](mci-setaudio.md)命令的參數。

## <a name="syntax"></a>語法


```C++
typedef struct tagMCI_VCR_SETAUDIO_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTrack;
  DWORD     dwTo;
  DWORD     dwNumber;
} MCI_VCR_SETAUDIO_PARMS;
```



## <a name="members"></a>成員

<dl> <dt>

**dwCallback**
</dt> <dd>

低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。

</dd> <dt>

**dwTrack**
</dt> <dd>

音訊播放軌。

</dd> <dt>

**dwTo**
</dt> <dd>

輸入或受監視輸入的類型。

</dd> <dt>

**dwNumber**
</dt> <dd>

要使用的 **dwTo** 成員) 中所指定類型的音訊輸入 (。

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

[**MCI**](mci.md)
</dt> <dt>

[**MCI 結構**](mci-structures.md)
</dt> <dt>

[**MCI \_ SETAUDIO**](mci-setaudio.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

