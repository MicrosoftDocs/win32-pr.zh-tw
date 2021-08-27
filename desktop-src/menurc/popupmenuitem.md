---
title: POPUPMENUITEM 結構
description: 包含功能表資源中開啟功能表或子功能表的功能表項目相關資訊。 此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。
ms.assetid: cb8faeb2-bca9-4ff5-8f80-d273c3fca504
keywords:
- POPUPMENUITEM 結構功能表和其他資源
topic_type:
- apiref
api_name:
- POPUPMENUITEM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 62d769e9756f0d15e7377a79f9aa94802a469746807e3a32b5ba329f76484b82
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011698"
---
# <a name="popupmenuitem-structure"></a>POPUPMENUITEM 結構

包含功能表資源中開啟功能表或子功能表的功能表項目相關資訊。 此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。

## <a name="syntax"></a>語法


```C++
typedef struct {
  DWORD   type;
  DWORD   state;
  DWORD   id;
  WORD    resInfo;
  szOrOrd menuText;
} POPUPMENUITEM;
```



## <a name="members"></a>成員

<dl> <dt>

**type**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

描述功能表項目。 這個成員可以有的一些值包含下列清單所示的值。

除了顯示的值以外，這個成員也可以是與 [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)結構的 **fType** 成員一起列出的型別值組合。 型別值是以 MFT 開頭的值 \_ 。 若要使用這些預先定義 \_ \* 的 MFT 類型值，請在您的 .rc 檔中加入下列語句：

`#include "winuser.h"`



| 值                                                                                                                                                                                                    | 意義                                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="MF_END"></span><span id="mf_end"></span><dl> <dt>**MF \_END**</dt> <dt>0x80</dt> </dl>       | 功能表項目是功能表上的最後一個;系統會在內部使用旗標。 <br/>   |
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <dt>**MF \_POPUP**</dt> <dt>0x01</dt> </dl> | 功能表項目會開啟功能表或子功能表;系統會在內部使用旗標。 <br/> |



 

</dd> <dt>

**state**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

描述功能表項目。 這個成員可以是與 [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)結構的 **dwState** 成員一起列出之狀態值的組合。 狀態值是以 MFS 開頭的值 \_ 。 若要使用這些預先定義 \_ \* 的 MFS 狀態值，請在 .rc 檔中加入下列語句：

`#include "winuser.h"`

</dd> <dt>

**id**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

識別在 [**WM \_ 命令**](wm-command.md) 訊息中傳遞之功能表項目的數值運算式。

</dd> <dt>

**resInfo**
</dt> <dd>

類型： **WORD**

</dd> <dd>

指定功能表項目類型的一組位旗標。 這個成員可以是下列其中一個值。



| 值                                                                                                                                                                                                       | 意義                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MFR_END"></span><span id="mfr_end"></span><dl> <dt>**MFR \_END**</dt> <dt>0x80</dt> </dl>       | 功能表項目是此子功能表或功能表資源中的最後一個;系統會在內部使用此旗標。<br/> |
| <span id="MFR_POPUP"></span><span id="mfr_popup"></span><dl> <dt>**MFR \_POPUP**</dt> <dt>0x01</dt> </dl> | 功能表項目會開啟功能表或子功能表;系統會在內部使用旗標。<br/>                     |



 

</dd> <dt>

**menuText**
</dt> <dd>

類型： **szOrOrd**

</dd> <dd>

以 null 終止的 Unicode 字串，其中包含這個功能表項目的文字。 這個字串的大小沒有固定限制。

</dd> </dl>

## <a name="remarks"></a>備註

開啟功能表或子功能表的每個功能表項目都有一個 **POPUPMENUITEM** 結構。 藉由將 **類型** 成員設定為 **MF \_ 快顯視窗**，以及將 **resInfo** 成員中的 **MFR 快 \_** 顯位設定為0x0001，來識別這種類型的功能表項目。 在此情況下，針對功能表或子功能表，寫入 [**RT \_ 功能表**](/windows/desktop/menurc/resource-types) 資源的最後資料是 [**MENUHELPID**](menuhelpid.md) 結構。 **MENUHELPID** 包含可在 [**WM \_**](../shell/wm-help.md) 說明處理期間識別功能表的數值運算式。

此外，在 **resInfo** 成員中設定 **MFR 快 \_** 顯位的每個 **POPUPMENUITEM** 結構，後面都會接著 [**MENUHELPID**](menuhelpid.md)結構，再加上一個額外的 **POPUPMENUITEM** 結構，其中每個功能表項目都是該子功能表中的每個功能表項目。 子功能表中的最後一個 **POPUPMENUITEM** 結構會在 **resInfo** 成員中設定 **MFR \_ 結束** 位。 若要找出資源的結尾，請尋找每個 **MFR \_ 快顯視窗** 的相符 **MFR \_ 端**，再加上一個符合最外層功能表項目的額外 **MFR \_ 端**。

將 **類型** 成員設定為 **MF \_ END** 以表示最後一個功能表項目。 由於您可以嵌套子功能表，因此可能會有多個層級的 **MF \_ END**。 在這些情況下，功能表項目是連續的。

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

[**MENUHELPID**](menuhelpid.md)
</dt> <dt>

[**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)
</dt> <dt>

[**NORMALMENUITEM**](normalmenuitem.md)
</dt> <dt>

**概念**
</dt> <dt>

[資源](resources.md)
</dt> </dl>

 

