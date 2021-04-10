---
title: 'MCI_TMSF_SECOND 宏 (Mciapi) '
description: MCI \_ TMSF \_ SECOND 宏會從包含封裝曲目/分鐘/秒/畫面格的參數抓取秒鐘元件， (TMSF) 資訊。
ms.assetid: 0f431545-bde0-4898-9a9d-993847aedf50
keywords:
- MCI_TMSF_SECOND 宏 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_TMSF_SECOND
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 722949487400f80ed72f9e120d5dbf8678ab81a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104009"
---
# <a name="mci_tmsf_second-macro"></a>MCI \_ TMSF \_ 第二個宏

**MCI \_ TMSF \_ SECOND** 宏會從包含封裝曲目/分鐘/秒/畫面格的參數抓取秒鐘元件， (TMSF) 資訊。

## <a name="syntax"></a>語法


```C++
BYTE MCI_TMSF_SECOND(
   DWORD dwTMSF
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwTMSF* 
</dt> <dd>

TMSF 格式的時間。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回所指定 TMSF 資訊的秒陣列件。

## <a name="remarks"></a>備註

TMSF 格式的時間是以 **DWORD** 值來表示，其中包含最不重要的位元組，其中包含追蹤、下一個最不重要的位元組包含分鐘、下一個最不重要的位元組（包含秒），以及最重要的位元組（包含框架）。

**MCI \_ TMSF \_ SECOND** 宏的定義如下：


```C++
#define MCI_TMSF_SECOND(tmsf) ((BYTE)((tmsf) >> 16)) 
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

 

 





