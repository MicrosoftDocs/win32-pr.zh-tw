---
title: 'MCI_VCR_SETTUNER_PARMS 結構 (Vcr) '
description: MCI \_ VCR \_ SETTUNER \_ PARMS 結構包含適用于 \_ video-卡帶燒錄機之 mci SETTUNER 命令的參數。
ms.assetid: 8254b4c0-80bb-44e4-9f51-1d7434d3b08f
keywords:
- MCI_VCR_SETTUNER_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_VCR_SETTUNER_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 891ddf3b4b3dcb9532a2431901b0b2b9d84b0e52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685983"
---
# <a name="mci_vcr_settuner_parms-structure"></a>MCI \_ VCR \_ SETTUNER \_ PARMS 結構

**Mci \_ VCR \_ SETTUNER \_ PARMS** 結構包含適用于 video-卡帶燒錄機之 [**mci \_ SETTUNER**](mci-settuner.md)命令的參數。

## <a name="syntax"></a>語法


```C++
typedef struct tagMCI_VCR_SETTUNER_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwChannel;
  DWORD     dwNumber;
} MCI_VCR_SETTUNER_PARMS;
```



## <a name="members"></a>成員

<dl> <dt>

**dwCallback**
</dt> <dd>

低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。

</dd> <dt>

**dwChannel**
</dt> <dd>

新頻道號碼。

</dd> <dt>

**dwNumber**
</dt> <dd>

[**MCI \_ SETTUNER**](mci-settuner.md)命令影響的邏輯調諧器。

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

[**MCI \_ SETTUNER**](mci-settuner.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

