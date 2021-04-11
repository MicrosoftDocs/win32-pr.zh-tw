---
title: DSA_SEC_PAGE_INFO 結構
description: 搭配使用 WM \_ ADSPROP \_ 工作表 \_ 建立和 WM \_ DSA \_ 工作表 \_ 建立 \_ 通知訊息，以在 Active Directory MMC 嵌入式管理單元中定義次要屬性工作表。
ms.assetid: 422d84dc-6b5e-43bf-ac4f-3b99cb59f9df
ms.tgt_platform: multiple
keywords:
- DSA_SEC_PAGE_INFO 結構 Active Directory
- PDSA_SEC_PAGE_INFO 結構指標 Active Directory
topic_type:
- apiref
api_name:
- DSA_SEC_PAGE_INFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e4c8602a958c50c72942d89657a812d24f64571d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934640"
---
# <a name="dsa_sec_page_info-structure"></a>DSA \_ 秒 \_ 頁面 \_ 資訊結構

[ **DSA \_ SEC] \_ 頁面 \_ 資訊** 結構可搭配 [ [**wm \_ ADSPROP \_ 工作表 \_ 建立**](wm-adsprop-sheet-create.md) ] 和 [ [**WM \_ DSA \_ 工作表] \_ 建立 \_ 通知**](wm-dsa-sheet-create-notify.md) 訊息，以在 Active Directory MMC 嵌入式管理單元中定義次要屬性工作表。

> [!Note]  
> 此結構未定義于已發行的標頭檔中。 若要使用此結構，請使用所示的確切格式來定義它。

 

## <a name="syntax"></a>語法


```C++
typedef struct _DSA_SEC_PAGE_INFO {
  HWND          hwndParentSheet;
  DWORD         offsetTitle;
  DSOBJECTNAMES dsObjectNames;
} DSA_SEC_PAGE_INFO, *PDSA_SEC_PAGE_INFO;
```



## <a name="members"></a>成員

<dl> <dt>

**hwndParentSheet**
</dt> <dd>

包含次要屬性工作表之父系的視窗控制碼。

</dd> <dt>

**offsetTitle**
</dt> <dd>

包含以位元組為單位的位移，從 **DSA \_ SEC \_ 頁面 \_ 資訊** 結構的開頭到以 Null 終止的 Unicode 字串，其中包含次要屬性工作表的標題。

</dd> <dt>

**dsObjectNames**
</dt> <dd>

包含定義次要屬性工作表的 [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) 結構。 一次只能建立一個次要屬性工作表，因此 **DSOBJECTNAMES** 結構只能包含一個 [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) 結構。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WM \_ ADSPROP \_ 工作表 \_ 建立**](wm-adsprop-sheet-create.md)
</dt> <dt>

[**WM \_ DSA \_ 工作表 \_ 建立 \_ 通知**](wm-dsa-sheet-create-notify.md)
</dt> <dt>

[**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames)
</dt> <dt>

[**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)
</dt> </dl>

 

 





