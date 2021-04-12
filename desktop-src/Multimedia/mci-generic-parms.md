---
title: 'MCI_GENERIC_PARMS 結構 (Mciapi .h) '
description: MCI \_ 泛型 \_ PARMS 結構包含接收通知訊息的視窗控制碼。 此結構用於具有空白參數清單的 MCI 命令訊息。
ms.assetid: 706e406c-d263-4347-932c-e5f125acfe0f
keywords:
- MCI_GENERIC_PARMS 結構 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_GENERIC_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1f96482ed5ec7e27253f234031cd099600bf1b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464984"
---
# <a name="mci_generic_parms-structure"></a>MCI \_ 一般 \_ PARMS 結構

**MCI \_ 泛型 \_ PARMS** 結構包含接收通知訊息的視窗控制碼。 此結構用於具有空白參數清單的 MCI 命令訊息。

## <a name="syntax"></a>語法


```C++
typedef struct {
  DWORD_PTR dwCallback;
} MCI_GENERIC_PARMS;
```



## <a name="members"></a>成員

<dl> <dt>

**dwCallback**
</dt> <dd>

低序位字組指定用於 MCI 通知旗標的視窗控制碼 \_ 。

</dd> </dl>

## <a name="remarks"></a>備註

**Mci \_ CLOSE \_ PARMS** 和 **Mci \_ 認識 \_ PARMS** 結構與 **mci \_ 一般 \_ PARMS** 結構相同。

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

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

