---
title: 'MCI_MAKE_TMSF 宏 (Mciapi) '
description: MCI \_ MAKE \_ TMSF 宏會從指定的曲目、分、秒和框架值，以封裝的曲目/分鐘/秒/框架 (TMSF) 格式來建立時間值。
ms.assetid: ff2d6938-0ff7-46d5-92be-42b4b6f35524
keywords:
- MCI_MAKE_TMSF 宏 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_MAKE_TMSF
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f06cd6a400f742b49dc29063e8473465ad7e32dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968799"
---
# <a name="mci_make_tmsf-macro"></a>MCI \_ MAKE \_ TMSF 宏

**MCI \_ MAKE \_ TMSF** 宏會從指定的曲目、分、秒和框架值，以封裝的曲目/分鐘/秒/框架 (TMSF) 格式來建立時間值。

## <a name="syntax"></a>語法


```C++
DWORD MCI_MAKE_TMSF(
   BYTE tracks,
   BYTE minutes,
   BYTE seconds,
   BYTE frames
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*tracks* 
</dt> <dd>

曲目數目。

</dd> <dt>

*分鐘* 
</dt> <dd>

分鐘數。

</dd> <dt>

*seconds* 
</dt> <dd>

秒數。

</dd> <dt>

*框架* 
</dt> <dd>

畫面格數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

以壓縮的 TMSF 格式傳回時間。

## <a name="remarks"></a>備註

TMSF 格式的時間是以 **DWORD** 值來表示，其中包含最不重要的位元組，其中包含追蹤、下一個最不重要的位元組包含分鐘、下一個最不重要的位元組（包含秒），以及最重要的位元組（包含框架）。

**MCI \_ MAKE \_ TMSF** 宏的定義如下：


```C++
#define MCI_MAKE_TMSF(t, m, s, f) ((DWORD)(((BYTE)(t) | \ 
                                  ((WORD)(m) << 8)) | \ 
                                  (((DWORD)(BYTE)(s) | \ 
                                  ((WORD)(f) << 8)) << 16))) 
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

 

 





