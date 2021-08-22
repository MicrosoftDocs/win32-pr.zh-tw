---
title: PROPSHEETCFG 結構
description: 用來包含屬性工作表設定資料。
ms.assetid: d3bde744-9d85-4506-894f-f8be3463721f
ms.tgt_platform: multiple
keywords:
- PROPSHEETCFG 結構 Active Directory
- PPROPSHEETCFG 結構指標 Active Directory
topic_type:
- apiref
api_name:
- PROPSHEETCFG
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 971296e1e269e977919f142d1efe24426b9c83f19ac26da2e2362ab48da0aa9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025436"
---
# <a name="propsheetcfg-structure"></a>PROPSHEETCFG 結構

**PROPSHEETCFG** 結構是用來包含屬性工作表設定資料。 此結構包含在 [**CFSTR \_ DS \_ PROPSHEETCONFIG**](cfstr-ds-propsheetconfig.md) 剪貼簿格式中。

> [!Note]  
> 此結構未定義于已發行的標頭檔中。 若要使用這個結構，您必須以所示的確切格式來定義它。

 

## <a name="syntax"></a>語法


```C++
typedef struct {
  LONG_PTR lNotifyHandle;
  HWND     hwndParentSheet;
  HWND     hwndHidden;
  WPARAM   wParamSheetClose;
} PROPSHEETCFG, *PPROPSHEETCFG;
```



## <a name="members"></a>成員

<dl> <dt>

**lNotifyHandle**
</dt> <dd>

包含通知控制碼。 這與針對 [**IExtendPropertySheet2：： CreatePropertyPages**](/previous-versions/windows/desktop/legacy/aa814847(v=vs.85))方法中的 *控制碼* 參數傳遞的控制碼相同。

</dd> <dt>

**hwndParentSheet**
</dt> <dd>

包含父屬性工作表的視窗控制碼。

</dd> <dt>

**hwndHidden**
</dt> <dd>

包含隱藏視窗的控點。

</dd> <dt>

**wParamSheetClose**
</dt> <dd>

包含應用程式定義的32位值。 此值會在「 [**WM \_ DSA \_ 工作表 \_ 關閉 \_ 通知**](wm-dsa-sheet-close-notify.md)」訊息的 *wParam* 中傳回給應用程式。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CFSTR \_ DS \_ PROPSHEETCONFIG**](cfstr-ds-propsheetconfig.md)
</dt> <dt>

[**WM \_ DSA \_ 工作表 \_ 關閉 \_ 通知**](wm-dsa-sheet-close-notify.md)
</dt> </dl>

 

