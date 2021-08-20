---
title: 'MCI_TMSF_TRACK 宏 (Mciapi) '
description: MCI \_ TMSF \_ TRACK 宏會從包含封裝曲目/分鐘/秒/畫面格的參數抓取 TRACK 元件， (TMSF) 資訊。
ms.assetid: 3455442c-5c66-47c7-b06b-1a2de0e2dfed
keywords:
- MCI_TMSF_TRACK 宏 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_TMSF_TRACK
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7090a2a9b652d7c989aadd70d8843ece04bf467bbbe353c22c3f76fee8a9712b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137949"
---
# <a name="mci_tmsf_track-macro"></a>MCI \_ TMSF \_ TRACK 宏

**MCI \_ TMSF \_ TRACK** 宏會從包含封裝曲目/分鐘/秒/畫面格的參數抓取 TRACK 元件， (TMSF) 資訊。

## <a name="syntax"></a>語法


```C++
BYTE MCI_TMSF_TRACK(
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

傳回所指定 TMSF 資訊的「追蹤」元件。

## <a name="remarks"></a>備註

TMSF 格式的時間是以 **DWORD** 值來表示，其中包含最不重要的位元組，其中包含追蹤、下一個最不重要的位元組包含分鐘、下一個最不重要的位元組（包含秒），以及最重要的位元組（包含框架）。

**MCI \_ TMSF \_ TRACK** 巨集定義如下：


```C++
#define MCI_TMSF_TRACK(tmsf) ((BYTE)(tmsf)) 
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

 

 





