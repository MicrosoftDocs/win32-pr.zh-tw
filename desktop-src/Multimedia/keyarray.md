---
title: 'KEYARRAY (Mmsystem) '
description: KEYARRAY 會指定用來定義索引鍵陣列的型別。
ms.assetid: af1a1d2f-4558-4374-93ab-5a705fc879ca
keywords:
- KEYARRAY MIDIPATCHSIZE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6e45e46417fb3b6653ecae605aa60f775c1d654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965907"
---
# <a name="keyarray"></a>KEYARRAY

KEYARRAY 會指定用來定義索引鍵陣列的型別。


```C++
typedef WORD KEYARRAY[MIDIPATCHSIZE];
```



<dl> <dt>

**KEYARRAY \[ MIDIPATCHSIZE\]**
</dt> <dd>

陣列中的每個元素會對應至以金鑰為基礎的 percussion 修補程式，其中每個16位代表16個 MIDI 通道的其中一個。 系統會為每個使用該特定修補程式的通道設定 Bits。 例如，如果實體 MIDI 通道9和15使用金鑰編號60的 percussion 修補程式，則應該將陣列的元素60設定為0x8200。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 版本<br/>                  | 音樂檢測數位介面 (MIDI) 、MIDI 類型<br/>                                        |
| 標頭<br/>                   | <dl> <dt>Mmsystem (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[MIDI 類型](midi-event-types.md)
</dt> </dl>

 

 





