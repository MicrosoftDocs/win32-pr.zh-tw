---
title: 'MCI_HMS_MINUTE 宏 (Mciapi) '
description: MCI \_ HMS \_ MINUTE 宏會從包含「壓縮的小時/分鐘/秒」參數的參數抓取分鐘元件 (HMS) 資訊。
ms.assetid: d083f769-9825-48cc-80f9-34ce3ef66ad6
keywords:
- MCI_HMS_MINUTE 宏 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_HMS_MINUTE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49c91d2dcb13ea6b206df2a0dbc0d6a2e7096e59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106211"
---
# <a name="mci_hms_minute-macro"></a>MCI \_ HMS \_ MINUTE 宏

**MCI \_ HMS \_ MINUTE** 宏會從包含「壓縮的小時/分鐘/秒」參數的參數抓取分鐘元件 (HMS) 資訊。

## <a name="syntax"></a>語法


```C++
BYTE MCI_HMS_MINUTE(
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

傳回所指定 HMS 資訊的分鐘元件。

## <a name="remarks"></a>備註

HMS 格式的時間以 **DWORD** 值表示，其中最小的位元組包含小時、下一個最不重要的位元組（包含分鐘），以及下一個最不重要的位元組（包含秒）。 最重要的位元組未使用。

**MCI \_ HMS \_ MINUTE** 巨集定義如下：


```C++
#define MCI_HMS_MINUTE(hms) ((BYTE)(((WORD)(hms)) >> 8)) 
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

 

 





