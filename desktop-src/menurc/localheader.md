---
title: LOCALHEADER 結構
description: 包含與 RESDIR 結構所識別之資料指標相關聯之作用點的 x 和 y 座標。 此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。
ms.assetid: 8cf74040-8b8f-447e-a881-1bcf05b151e2
keywords:
- LOCALHEADER 結構功能表和其他資源
topic_type:
- apiref
api_name:
- LOCALHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7aa2ee51e1a9e456398a42d8190781b5dbec8d14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384849"
---
# <a name="localheader-structure"></a>LOCALHEADER 結構

包含與 [**RESDIR**](resdir.md) 結構所識別之資料指標相關聯之作用點的 x 和 y 座標。 此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。

## <a name="syntax"></a>語法


```C++
typedef struct {
  WORD xHotSpot;
  WORD yHotSpot;
} LOCALHEADER;
```



## <a name="members"></a>成員

<dl> <dt>

**xHotSpot**
</dt> <dd>

類型： **WORD**

</dd> <dd>

游標作用點的 x 座標（以圖元為單位）。

</dd> <dt>

**yHotSpot**
</dt> <dd>

類型： **WORD**

</dd> <dd>

游標作用點的 y 座標（以圖元為單位）。

</dd> </dl>

## <a name="remarks"></a>備註

如果 [**RESDIR**](resdir.md)結構包含資料指標的相關資訊， **LOCALHEADER** 結構就是寫入 [RT 資料 \_ 指標](/windows/desktop/menurc/resource-types)資源的第一個資料。

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

[**RESDIR**](resdir.md)
</dt> <dt>

**概念**
</dt> <dt>

[資源](resources.md)
</dt> </dl>

 

