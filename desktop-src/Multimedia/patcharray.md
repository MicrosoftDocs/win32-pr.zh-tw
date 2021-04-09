---
title: 'PATCHARRAY (Mmsystem) '
description: PATCHARRAY 是一種用來定義 MIDI 修補程式陣列的型別。
ms.assetid: f48ee0d2-224a-4530-ac28-ae63160316cc
keywords:
- PATCHARRAY MIDIPATCHSIZE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e07af0e878fc0d2fc79d6d17aafd48fbd991fb39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844396"
---
# <a name="patcharray"></a>PATCHARRAY

PATCHARRAY 是一種用來定義 MIDI 修補程式陣列的型別。


```C++
typedef WORD PATCHARRAY[MIDIPATCHSIZE];
```



<dl> <dt>

**PATCHARRAY \[ MIDIPATCHSIZE\]**
</dt> <dd>

陣列中的每個元素都會對應到一個 patch，其中每個16位代表16個 MIDI 通道的其中一個。 系統會為每個使用該特定修補程式的通道設定 Bits。 例如，如果實體 MIDI 通道0和8使用 patch number 0，則陣列的元素0應該設定為0x0101。

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

 

 





