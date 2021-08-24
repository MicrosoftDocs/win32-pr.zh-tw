---
title: 'MM_MCISIGNAL 訊息 (Mmsystem .h) '
description: MM \_ MCISIGNAL 訊息會傳送至視窗，以通知應用程式 mci 裝置已達先前的信號 ( MCI 信號) 命令中所定義的位置 \_ 。
ms.assetid: 12512d23-9a89-4e38-9ec5-88845766f4f6
keywords:
- MM_MCISIGNAL 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- MM_MCISIGNAL
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb54b56d35ad34d10d95c2a34b52b370fb856d9c958dd42223c7f0a08ddbdfb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807438"
---
# <a name="mm_mcisignal-message"></a>MM \_ MCISIGNAL 訊息

**MM \_ MCISIGNAL** 訊息會傳送至視窗，以通知應用程式 mci 裝置已達先前的 [**信號**](signal.md) ( [**MCI \_ 信號**](mci-signal.md)) 命令中所定義的位置。


```C++
MM_MCISIGNAL 
wParam = (WPARAM) wID      
lParam = (LONG) lUserParm  
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="wID"></span><span id="wid"></span><span id="WID"></span>*Wid*
</dt> <dd>

起始信號訊息之裝置的識別碼。

</dd> <dt>

<span id="lUserParm"></span><span id="luserparm"></span><span id="LUSERPARM"></span>*lUserParm*
</dt> <dd>

當 **信號** 命令已定義此回呼函式時，會在 **MCI \_ DGV \_ 信號 \_ PARAMS** 結構的 **dwUserParm** 成員中傳遞值。 或者，它可能會包含位置值。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Mmsystem (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[MCI 訊息](mci-messages.md)
</dt> <dt>

[**信號**](signal.md)
</dt> </dl>

 

 





