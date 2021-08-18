---
title: MENUHELPID 結構
description: '\_如果 POPUPMENUITEM 結構的 resInfo 成員設定為 MFR POPUP，則包含針對功能表或子功能表，寫入至 RT 功能表資源的最終資料 \_ 。'
ms.assetid: f17fdaaa-b37c-4902-bad4-a1181ffee9f9
keywords:
- MENUHELPID 結構功能表和其他資源
topic_type:
- apiref
api_name:
- MENUHELPID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4831074d5e7b663210f880bf6684cbc6484ad3487a0c6c9e5be308aebc66291a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825948"
---
# <a name="menuhelpid-structure"></a>MENUHELPID 結構

如果 [**POPUPMENUITEM**](popupmenuitem.md)結構的 **resInfo** 成員設定為 **MFR \_ POPUP**，則包含針對功能表或子功能表，寫入至 [**RT \_ 功能表**](/windows/desktop/menurc/resource-types)資源的最終資料。 此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。

## <a name="syntax"></a>語法


```C++
typedef struct {
  DWORD helpID;
} MENUHELPID;
```



## <a name="members"></a>成員

<dl> <dt>

**h**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

在 [**WM \_**](/windows/desktop/shell/wm-help) 說明處理期間用來識別功能表的識別碼。

</dd> </dl>

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

[**POPUPMENUITEM**](popupmenuitem.md)
</dt> <dt>

**概念**
</dt> <dt>

[資源](resources.md)
</dt> </dl>

 

