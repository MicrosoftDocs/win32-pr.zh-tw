---
title: 'MCI_OVLY_LOAD_PARMS 結構 (Mmsystem .h) '
description: MCI \_ OVLY \_ LOAD PARMS 結構包含適用于影片重迭裝置之 \_ MCI \_ LOAD 命令的資訊。
ms.assetid: 701c27da-72bf-493d-a679-9e0bd210215d
keywords:
- MCI_OVLY_LOAD_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_OVLY_LOAD_PARMS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2029e92f7991f1ae5d8d0bdbabc76eef456a36ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024566"
---
# <a name="mci_ovly_load_parms-structure"></a>MCI \_ OVLY \_ LOAD \_ PARMS 結構

**Mci \_ OVLY \_ LOAD \_ PARMS** 結構包含適用于影片重迭裝置之 [**MCI \_ LOAD**](mci-load.md)命令的資訊。

## <a name="syntax"></a>語法


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpfilename;
  RECT      rc;
} MCI_OVLY_LOAD_PARMS;
```



## <a name="members"></a>成員

<dl> <dt>

**dwCallback**
</dt> <dd>

低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。

</dd> <dt>

**lpfilename**
</dt> <dd>

要載入之檔案的名稱。

</dd> <dt>

**鋼筋混凝土**
</dt> <dd>

識別要更新的影片緩衝區區域。 在 MCI 中，[矩形](/previous-versions//ms536136(v=vs.85))結構的處理方式不同于 Windows 的其他部分;在 MCI 中， **.rc** 會包含矩形和 rc 的寬度 **。下方** 包含其高度。

</dd> </dl>

## <a name="remarks"></a>備註

將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Mmsystem。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Mci**](mci.md)
</dt> <dt>

[**MCI 結構**](mci-structures.md)
</dt> <dt>

[**MCI \_ 負載**](mci-load.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> <dt>

[矩形](/previous-versions//ms536136(v=vs.85))
</dt> </dl>

 

