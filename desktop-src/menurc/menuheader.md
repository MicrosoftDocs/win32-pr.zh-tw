---
title: MENUHEADER 結構
description: 包含功能表資源的版本資訊。 此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。
ms.assetid: 1e34b0b6-18ff-4cb6-901e-a2aabad0df74
keywords:
- MENUHEADER 結構功能表和其他資源
topic_type:
- apiref
api_name:
- MENUHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eacc67d34d04502aa17eeaca78240a0a3e0e219d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965694"
---
# <a name="menuheader-structure"></a>MENUHEADER 結構

包含功能表資源的版本資訊。 此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。

## <a name="syntax"></a>語法


```C++
typedef struct {
  WORD wVersion;
  WORD cbHeaderSize;
} MENUHEADER;
```



## <a name="members"></a>成員

<dl> <dt>

**wVersion**
</dt> <dd>

類型： **WORD**

</dd> <dd>

功能表範本的版本號碼。 此成員必須等於零，表示這是使用標準功能表範本建立的 [**RT \_ 功能表**](/windows/desktop/menurc/resource-types) 。

</dd> <dt>

**cbHeaderSize**
</dt> <dd>

類型： **WORD**

</dd> <dd>

功能表範本標頭的大小。 如果您使用標準功能表範本建立的功能表，此值為零。

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

[**MENUEX \_ 範本 \_ 標頭**](menuex-template-header.md)
</dt> <dt>

[**MENUEX \_ 範本 \_ 專案**](menuex-template-item.md)
</dt> <dt>

[**MENUITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate)
</dt> <dt>

[**MENUITEMTEMPLATEHEADER**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader)
</dt> <dt>

[**NORMALMENUITEM**](normalmenuitem.md)
</dt> <dt>

[**POPUPMENUITEM**](popupmenuitem.md)
</dt> <dt>

**概念**
</dt> <dt>

[資源](resources.md)
</dt> </dl>

 

