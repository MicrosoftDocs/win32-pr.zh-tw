---
title: NORMALMENUITEM 結構
description: 包含未開啟功能表或子功能表的功能表資源中，每個專案的相關資訊。 此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。
ms.assetid: c1b84264-2d7f-4bc3-8e74-7b921a0bfe30
keywords:
- NORMALMENUITEM 結構功能表和其他資源
topic_type:
- apiref
api_name:
- NORMALMENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c90efe624346e30483c42f6f8ff51cd6d3550922
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317183"
---
# <a name="normalmenuitem-structure"></a>NORMALMENUITEM 結構

包含未開啟功能表或子功能表的功能表資源中，每個專案的相關資訊。 此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。

## <a name="syntax"></a>語法


```C++
typedef struct {
  WORD    resInfo;
  szOrOrd menuText;
} NORMALMENUITEM;
```



## <a name="members"></a>成員

<dl> <dt>

**resInfo**
</dt> <dd>

類型： **WORD**

</dd> <dd>

功能表項目的類型。 這個成員可以是下列其中一個值。



| 值                                                                                                                                                                                                       | 意義                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MFR_END"></span><span id="mfr_end"></span><dl> <dt>**MFR \_END**</dt> <dt>0x80</dt> </dl>       | 功能表項目是此子功能表或功能表資源中的最後一個;系統會在內部使用此旗標。<br/> |
| <span id="MFR_POPUP"></span><span id="mfr_popup"></span><dl> <dt>**MFR \_POPUP**</dt> <dt>0x01</dt> </dl> | 功能表項目會開啟功能表或子功能表;系統會在內部使用旗標。 <br/>                    |



 

</dd> <dt>

**menuText**
</dt> <dd>

類型： **szOrOrd**

</dd> <dd>

以 null 終止的 Unicode 字串，其中包含這個功能表項目的文字。 這個字串的大小沒有固定限制。

</dd> </dl>

## <a name="remarks"></a>備註

未開啟功能表或子功能表的每個功能表項目都有一個 **NORMALMENUITEM** 結構。 將 **resInfo** 成員設定為 **MFR \_ END**，以指出功能表上的最後一個功能表項目。

功能表分隔符號是特殊類型的功能表項目，非作用中，但會顯示為兩個現用功能表項目之間的分隔線。 藉由將 **menuText** 成員保留空白來表示功能表分隔符號。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**MENUHEADER**](menuheader.md)
</dt> <dt>

[**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

[**POPUPMENUITEM**](popupmenuitem.md)
</dt> <dt>

**概念**
</dt> <dt>

[資源](resources.md)
</dt> </dl>

 

 





