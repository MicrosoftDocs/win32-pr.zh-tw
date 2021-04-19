---
title: RESDIR 結構
description: 包含資源群組中個別圖示或游標元件的相關資訊。 每個群組元件都有一個 RESDIR 結構。 此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcestructures\resdir.htm
keywords:
- RESDIR 結構功能表和其他資源
topic_type:
- apiref
api_name:
- RESDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b854a4af3367131f6a559e1fef5899fae8b81107
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968332"
---
# <a name="resdir-structure"></a>RESDIR 結構

包含資源群組中個別圖示或游標元件的相關資訊。 每個群組元件都有一個 **RESDIR** 結構。 此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。

## <a name="syntax"></a>語法


```C++
typedef struct {
  ICONRESDIR Icon;
  CURSORDIR  Cursor;
  CURSORDIR  Planes;
  CURSORDIR  BitCount;
  CURSORDIR  BytesInRes;
  CURSORDIR  IconCursorId;
} RESDIR;
```



## <a name="members"></a>成員

<dl> <dt>

**圖示**
</dt> <dd>

類型： **[ **ICONRESDIR**](iconresdir.md)**

</dd> <dd>

指定圖示的寬度、高度和色彩計數。

</dd> <dt>

**資料指標**
</dt> <dd>

類型： **[ **CURSORDIR**](cursordir.md)**

</dd> <dd>

指定之游標的寬度和高度。

</dd> <dt>

**飛機**
</dt> <dd>

類型： **[ **CURSORDIR**](cursordir.md)**

</dd> <dd>

圖示或游標點陣圖中的色彩平面數目。

</dd> <dt>

**BitCount**
</dt> <dd>

類型： **[ **CURSORDIR**](cursordir.md)**

</dd> <dd>

圖示或游標點陣圖中每個圖元的位數。

</dd> <dt>

**BytesInRes**
</dt> <dd>

類型： **[ **CURSORDIR**](cursordir.md)**

</dd> <dd>

資源的大小（以位元組為單位）。

</dd> <dt>

**IconCursorId**
</dt> <dd>

類型： **[ **CURSORDIR**](cursordir.md)**

</dd> <dd>

具有唯一序數識別碼的圖示或游標。

</dd> </dl>

## <a name="remarks"></a>備註

一或多個 **RESDIR** 結構會緊接在 .res 檔中的 [**NEWHEADER**](newheader.md) 結構後面。 **NEWHEADER** 結構的 **ResCount** 成員會指定 **RESDIR** 結構的數目。 請注意， **RESDIR** 結構是由 [**ICONRESDIR**](iconresdir.md) 結構或 [**CURSORDIR**](cursordir.md) 結構所組成，後面接著 **平面**、 **BitCount**、 **BytesInRes** 和 **IconCursorId** 成員。 如果 **RESDIR** 結構包含資料指標的相關資訊，則資源編譯器寫入至 [RT 資料 \_ 指標](/windows/desktop/menurc/resource-types)資源的前兩個 **字** 是 [**LOCALHEADER**](localheader.md)結構的 **xHotSpot** 和 **yHotSpot** 成員。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**CURSORDIR**](cursordir.md)
</dt> <dt>

[**ICONRESDIR**](iconresdir.md)
</dt> <dt>

[**LOCALHEADER**](localheader.md)
</dt> <dt>

[**NEWHEADER**](newheader.md)
</dt> <dt>

**概念**
</dt> <dt>

[資源](resources.md)
</dt> </dl>

 

