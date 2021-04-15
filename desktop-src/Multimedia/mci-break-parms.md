---
title: 'MCI_BREAK_PARMS 結構 (Mciapi .h) '
description: MCI \_ break \_ PARMS 結構包含了 mci break 命令的虛擬金鑰程式碼和視窗資訊 \_ 。
ms.assetid: c8df8c55-cc6b-4dd7-b275-784d3eb9dce1
keywords:
- MCI_BREAK_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_BREAK_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e66b52992827b447b6d4b5585ca3f98564142680
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508476"
---
# <a name="mci_break_parms-structure"></a>MCI \_ BREAK \_ PARMS 結構

**Mci \_ break \_ PARMS** 結構包含了 [**mci \_ break**](mci-break.md)命令的虛擬金鑰程式碼和視窗資訊。

## <a name="syntax"></a>語法


```C++
typedef struct {
  DWORD_PTR dwCallback;
  int       nVirtKey;
  HWND      hwndBreak;
} MCI_BREAK_PARMS;
```



## <a name="members"></a>成員

<dl> <dt>

**dwCallback**
</dt> <dd>

低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。

</dd> <dt>

**nVirtKey**
</dt> <dd>

Break 鍵的虛擬按鍵碼。

</dd> <dt>

**hwndBreak**
</dt> <dd>

視窗的控制碼，必須是中斷偵測的目前視窗。

</dd> </dl>

## <a name="remarks"></a>備註

將資料指派給此結構的成員時，請在 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85))函數的 *fdwCommand* 參數中設定對應的旗標，以驗證成員。 以下是定義的旗標：

MCI \_ BREAK \_ HWND

驗證 **hwndBreak** 成員，指定必須有焦點才能啟用中斷偵測的視窗。

MCI \_ 中斷 \_ 金鑰

驗證 **nVirtKey** 成員，其指定要用於 break 索引鍵的虛擬機器碼程式碼。

MCI \_ 中斷 \_

停用任何現有的 break 鍵。

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

[**MCI \_ 斷路**](mci-break.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

