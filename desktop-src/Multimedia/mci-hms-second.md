---
title: 'MCI_HMS_SECOND 宏 (Mciapi) '
description: MCI \_ HMS \_ SECOND 宏會從包含「壓縮時數/分鐘/秒」參數的參數抓取秒鐘元件 (HMS) 資訊。
ms.assetid: b6895bec-524f-4345-ae65-e75168855df2
keywords:
- MCI_HMS_SECOND 宏 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_HMS_SECOND
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30b869141d6480ba0d986450ce950097ba240009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844331"
---
# <a name="mci_hms_second-macro"></a>MCI \_ HMS \_ 第二個宏

**MCI \_ HMS \_ SECOND** 宏會從包含「壓縮時數/分鐘/秒」參數的參數抓取秒鐘元件 (HMS) 資訊。

## <a name="syntax"></a>語法


```C++
BYTE MCI_HMS_SECOND(
   DWORD dwHMS
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwHMS* 
</dt> <dd>

HMS 格式的時間。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回所指定 HMS 資訊的秒陣列件。

## <a name="remarks"></a>備註

HMS 格式的時間以 **DWORD** 值表示，其中最小的位元組包含小時、下一個最不重要的位元組（包含分鐘），以及下一個最不重要的位元組（包含秒）。 最重要的位元組未使用。

**MCI \_ HMS \_ SECOND** 宏的定義如下：


```C++
#define MCI_HMS_SECOND(hms) ((BYTE)((hms) >> 16)) 
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Mciapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[MCI 宏](mci-macros.md)
</dt> </dl>

 

 





