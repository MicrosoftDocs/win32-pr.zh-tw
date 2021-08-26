---
title: 'MCI_VCR_RECORD_PARMS 結構 (Vcr) '
description: MCI \_ VCR \_ 記錄 \_ PARMS 結構包含適用于 \_ 視頻磁帶燒錄機之 mci 記錄命令的參數。
ms.assetid: a95a6dab-9854-4c44-989a-032dff680106
keywords:
- MCI_VCR_RECORD_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_VCR_RECORD_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1b613c2b64bae1395b3fc402816145c0ef690801b9fd6402201198f7ff28a6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038228"
---
# <a name="mci_vcr_record_parms-structure"></a>MCI \_ VCR \_ 記錄 \_ PARMS 結構

**Mci \_ VCR \_ 記錄 \_ PARMS** 結構包含適用于視頻磁帶燒錄機之 [**mci \_ 記錄**](mci-record.md)命令的參數。

## <a name="syntax"></a>語法


```C++
typedef struct tagMCI_VCR_RECORD_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwAt;
} MCI_VCR_RECORD_PARMS;
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

**dwAt**
</dt> <dd>

影響 [**MCI \_ 記錄**](mci-record.md) 或 [**MCI \_ 提示**](mci-cue.md) 命令的時間值。 對於 **MCI \_ 記錄**，這是開始錄製的時間。 對於 **MCI \_ 提示**，這是 Cued 裝置到達 **dwFrom** 中指定位置的時間。

</dd> </dl>

## <a name="remarks"></a>備註

以目前時間格式指定位置。

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

[**MCI \_ 提示**](mci-cue.md)
</dt> <dt>

[**MCI \_ 記錄**](mci-record.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

