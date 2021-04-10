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
ms.openlocfilehash: a7ecab8b5de7712a9c1a5ebd5c0a4401b264d7ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025475"
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

[Mci](mci.md)
</dt> <dt>

[MCI 宏](mci-macros.md)
</dt> </dl>

 

 





