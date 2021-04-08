---
title: 'MCI_MAKE_HMS 宏 (Mciapi) '
description: MCI \_ MAKE \_ HMS 宏會將時間值從指定的時數、分鐘數和秒數值以 [壓縮時數/分鐘/秒] (HMS) 格式建立。
ms.assetid: 470e89eb-36e1-4b05-babd-4c986adc88dd
keywords:
- MCI_MAKE_HMS 宏 Windows 多媒體
topic_type:
- apiref
api_name:
- MCI_MAKE_HMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f37c95df89ed6a799575e964ae274e01e329ef1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686318"
---
# <a name="mci_make_hms-macro"></a>MCI \_ MAKE \_ HMS 宏

**MCI \_ MAKE \_ HMS** 宏會將時間值從指定的時數、分鐘數和秒數值以 [壓縮時數/分鐘/秒] (HMS) 格式建立。

## <a name="syntax"></a>語法


```C++
DWORD MCI_MAKE_HMS(
   BYTE hours,
   BYTE minutes,
   BYTE seconds
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*小時* 
</dt> <dd>

時數。

</dd> <dt>

*分鐘* 
</dt> <dd>

分鐘數。

</dd> <dt>

*seconds* 
</dt> <dd>

秒數。

</dd> </dl>

## <a name="return-value"></a>傳回值

以壓縮的 HMS 格式傳回時間。

## <a name="remarks"></a>備註

HMS 格式的時間以 **DWORD** 值表示，其中最小的位元組包含小時、下一個最不重要的位元組（包含分鐘），以及下一個最不重要的位元組（包含秒）。 最重要的位元組未使用。

**MCI \_ MAKE \_ HMS** 宏的定義如下：


```C++
#define MCI_MAKE_HMS(h, m, s) ((DWORD)(((BYTE)(h) | \ 
                              ((WORD)(m) << 8)) | \ 
                              (((DWORD)(BYTE)(s)) << 16))) 
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

 

 





