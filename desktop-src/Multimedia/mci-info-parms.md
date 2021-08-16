---
title: 'MCI_INFO_PARMS 結構 (Mciapi .h) '
description: MCI \_ info \_ PARMS 結構包含 mci information 命令的資訊 \_ 。
ms.assetid: c64cff7d-a6d5-44b7-8cfb-9593f6328832
keywords:
- MCI_INFO_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_INFO_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2415fe0234c1a5b553a8b55d785febd82ebdd770f8c297bfc483549a1aa2a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118375013"
---
# <a name="mci_info_parms-structure"></a>MCI \_ 資訊 \_ PARMS 結構

**Mci \_ info \_ PARMS** 結構包含 mci information 命令的 [**資訊 \_**](mci-info.md) 。

## <a name="syntax"></a>語法


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPTSTR    lpstrReturn;
  DWORD     dwRetSize;
} MCI_INFO_PARMS;
```



## <a name="members"></a>成員

<dl> <dt>

**dwCallback**
</dt> <dd>

低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。

</dd> <dt>

**lpstrReturn**
</dt> <dd>

傳回字串的緩衝區。

</dd> <dt>

**dwRetSize**
</dt> <dd>

傳回字串的大小（以字元為單位）。

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

[**MCI \_ 資訊**](mci-info.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

