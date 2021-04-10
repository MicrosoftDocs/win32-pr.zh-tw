---
title: NEWHEADER 結構
description: 包含資源群組中的圖示或游標元件數目。 此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。
ms.assetid: 1549579a-b558-42a9-9b3b-5b382334221c
keywords:
- NEWHEADER 結構功能表和其他資源
topic_type:
- apiref
api_name:
- NEWHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d215bc00ef414d4e626d3da657dcecfd7a8a6c8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934052"
---
# <a name="newheader-structure"></a>NEWHEADER 結構

包含資源群組中的圖示或游標元件數目。 此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。

## <a name="syntax"></a>語法


```C++
typedef struct {
  WORD Reserved;
  WORD ResType;
  WORD ResCount;
} NEWHEADER, *NEWHEADER;
```



## <a name="members"></a>成員

<dl> <dt>

**已保留**
</dt> <dd>

類型： **WORD**

</dd> <dd>

保護必須為零。

</dd> <dt>

**Azuremmblobcontainer.restype**
</dt> <dd>

類型： **WORD**

</dd> <dd>

資源類型。 這個成員必須有下列其中一個值。



| 值                                                                                                                                                                                                       | 意義                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="RES_CURSOR"></span><span id="res_cursor"></span><dl> <dt>**RES \_資料指標**</dt> <dt>2</dt> </dl> | Cursor 資源類型。<br/> |
| <span id="RES_ICON"></span><span id="res_icon"></span><dl> <dt>**RES \_圖示**</dt> <dt>1</dt> </dl>       | 圖示資源類型。<br/>   |



 

</dd> <dt>

**ResCount**
</dt> <dd>

類型： **WORD**

</dd> <dd>

資源群組中的圖示或游標元件數目。

</dd> </dl>

## <a name="remarks"></a>備註

一或多個 [**RESDIR**](resdir.md) 結構會緊接在 .res 檔中的 **NEWHEADER** 結構後面。 **ResCount** 成員會指定 **RESDIR** 結構的數目。

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

 

 





