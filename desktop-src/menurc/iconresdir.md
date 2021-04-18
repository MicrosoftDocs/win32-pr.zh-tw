---
title: ICONRESDIR 結構
description: 包含資源群組中個別圖示影像的維度和色彩格式。 此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。
ms.assetid: 4c727369-2e90-40ad-85af-96d7e060b97a
keywords:
- ICONRESDIR 結構功能表和其他資源
topic_type:
- apiref
api_name:
- ICONRESDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: de3d15bf250685e0b0cad935cd5e8094b2f2ceee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968563"
---
# <a name="iconresdir-structure"></a>ICONRESDIR 結構

包含資源群組中個別圖示影像的維度和色彩格式。 此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。

## <a name="syntax"></a>語法


```C++
typedef struct {
  BYTE Width;
  BYTE Height;
  BYTE ColorCount;
  BYTE reserved;
} ICONRESDIR;
```



## <a name="members"></a>成員

<dl> <dt>

**寬度**
</dt> <dd>

類型： **位元組**

</dd> <dd>

圖示的寬度（以圖元為單位）。 可接受的值為16、32和64。

</dd> <dt>

**高度**
</dt> <dd>

類型： **位元組**

</dd> <dd>

圖示的高度（以圖元為單位）。 可接受的值為16、32和64。

</dd> <dt>

**ColorCount**
</dt> <dd>

類型： **位元組**

</dd> <dd>

圖示中的色彩數目。 可接受的值為2、8和16。

</dd> <dt>

**保留**
</dt> <dd>

類型： **位元組**

</dd> <dd>

保護必須設定為圖示檔案標頭中保留字段的相同值。

</dd> </dl>

## <a name="remarks"></a>備註

如果 **RESDIR** 結構描述圖示，則會在 [**RESDIR**](resdir.md)結構中傳遞 **ICONRESDIR** 結構。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**RESDIR**](resdir.md)
</dt> <dt>

**概念**
</dt> <dt>

[資源](resources.md)
</dt> </dl>

 

 





