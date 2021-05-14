---
description: 包含要新增至 [檔案管理員] 工具列之自訂按鈕的相關資訊。 這些按鈕是由檔案管理員延伸模組 DLL 提供。
title: 'FMS_TOOLBARLOAD 結構 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_TOOLBARLOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 7185f9e5-10c6-43cc-b85b-cd077378338f
ms.openlocfilehash: 3a993312b9e365561018459c43dab87afbd3c2b2
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842159"
---
# <a name="fms_toolbarload-structure"></a>FMS \_ TOOLBARLOAD 結構

包含要新增至 [檔案管理員] 工具列之自訂按鈕的相關資訊。 這些按鈕是由檔案管理員延伸模組 DLL 提供。

## <a name="syntax"></a>語法


```C++
typedef struct _FMS_TOOLBARLOAD {
  DWORD        dwSize;
  LPEXT_BUTTON lpButtons;
  WORD         cButtons;
  WORD         cBitmaps;
  WORD         idBitmap;
  HBITMAP      hBitmap;
} FMS_TOOLBARLOAD;
```



## <a name="members"></a>成員

<dl> <dt>

**dwSize**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

結構的大小（以位元組為單位）。 檔案管理員會在呼叫延伸模組之前設定大小，並且在擴充程式傳回後檢查大小。

</dd> <dt>

**lpButtons**
</dt> <dd>

類型： **LPEXT \_ 按鈕**

</dd> <dd>

[**EXT \_ 按鈕**](ext-button.md)結構陣列的位址。

</dd> <dt>

**cButtons**
</dt> <dd>

類型： **WORD**

</dd> <dd>

**LpButtons** 成員所指向陣列中的 [**EXT \_ 按鈕**](ext-button.md)結構數目。 此數位等於要加入至工具列的按鈕和分隔符號數目。

</dd> <dt>

**cBitmaps**
</dt> <dd>

類型： **WORD**

</dd> <dd>

給定點陣圖所表示的按鈕數目。

</dd> <dt>

**idBitmap**
</dt> <dd>

類型： **WORD**

</dd> <dd>

延伸模組 DLL 的可執行檔中點陣圖資源的識別碼。 點陣圖資源包含 **cBitmaps** 所指定之按鈕數目的影像。 [檔案管理員] 會載入點陣圖資源，然後使用它來顯示按鈕。

</dd> <dt>

**hBitmap**
</dt> <dd>

類型： **HBITMAP**

</dd> <dd>

點陣圖的控制碼，如果 **idBitmap** 為0，則會使用檔案管理員來取得和顯示按鈕影像。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wfext。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**FMEVENT \_ TOOLBARLOAD**](fmevent-toolbarload.md)
</dt> </dl>

 

 




