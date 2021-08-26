---
title: 'MCI_HMS_HOUR 宏 (Mciapi) '
description: MCI \_ HMS \_ HOUR 宏會從包含「壓縮的小時/分鐘/秒」參數的參數取出時陣列件 (HMS) 資訊。
ms.assetid: 55968b2b-2bfe-48ac-a50f-5c8741d11e33
keywords:
- MCI_HMS_HOUR 宏 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_HMS_HOUR
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97b8000e642d18f8499be5f8622a1cf7540fefbd041b7d34f23e1fd5e231815a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039268"
---
# <a name="mci_hms_hour-macro"></a>MCI \_ HMS \_ HOUR 宏

**MCI \_ HMS \_ HOUR** 宏會從包含「壓縮的小時/分鐘/秒」參數的參數取出時陣列件 (HMS) 資訊。

## <a name="syntax"></a>語法


```C++
BYTE MCI_HMS_HOUR(
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

傳回所指定 HMS 資訊的時陣列件。

## <a name="remarks"></a>備註

HMS 格式的時間以 **DWORD** 值表示，其中最小的位元組包含小時、下一個最不重要的位元組（包含分鐘），以及下一個最不重要的位元組（包含秒）。 最重要的位元組未使用。

**MCI \_ HMS \_ HOUR** 巨集定義如下：


```C++
#define MCI_HMS_HOUR(hms) ((BYTE)(hms)) 
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Mciapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[MCI 宏](mci-macros.md)
</dt> </dl>

 

 





