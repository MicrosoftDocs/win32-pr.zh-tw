---
title: MENUEX_TEMPLATE_HEADER 結構
description: 定義擴充功能表範本的標頭。 此結構定義僅供說明之用;它不會出現在任何標準標頭檔中。
ms.assetid: df763349-7127-482e-8613-74e68addde5d
keywords:
- MENUEX_TEMPLATE_HEADER 結構功能表和其他資源
topic_type:
- apiref
api_name:
- MENUEX_TEMPLATE_HEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: caa255ccdbe76c3959d9c730bcaa52ec07428742
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969960"
---
# <a name="menuex_template_header-structure"></a>MENUEX \_ 範本 \_ 標頭結構

定義擴充功能表範本的標頭。 此結構定義僅供說明之用;它不會出現在任何標準標頭檔中。

## <a name="syntax"></a>語法


```C++
typedef struct {
  WORD  wVersion;
  WORD  wOffset;
  DWORD dwHelpId;
} MENUEX_TEMPLATE_HEADER;
```



## <a name="members"></a>成員

<dl> <dt>

**wVersion**
</dt> <dd>

類型： **WORD**

</dd> <dd>

範本版本號碼。 擴充功能表範本的這個成員必須是1。

</dd> <dt>

**wOffset**
</dt> <dd>

類型： **WORD**

</dd> <dd>

相對於此結構成員結尾的第一個 [**MENUEX \_ 範本 \_ 專案**](menuex-template-item.md) 結構的位移。 如果第一個專案定義緊接在 **dwHelpId** 成員之後，這個成員應該是4。

</dd> <dt>

**dwHelpId**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

功能表列的說明識別碼。

</dd> </dl>

## <a name="remarks"></a>備註

擴充功能表範本包含 **MENUEX \_ 範本 \_ 標頭** 結構，後面接著一個或多個連續的 [**MENUEX \_ 範本 \_ 專案**](menuex-template-item.md) 結構。 **MENUEX \_ 範本 \_ 專案** 結構（長度為變數）會對齊 **DWORD** 界限。 若要從記憶體中的擴充功能表範本建立功能表，請使用 [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta)
</dt> <dt>

[**MENUEX \_ 範本 \_ 專案**](menuex-template-item.md)
</dt> <dt>

**概念**
</dt> <dt>

[功能表](menus.md)
</dt> </dl>

 

 





