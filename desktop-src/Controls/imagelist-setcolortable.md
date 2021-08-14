---
title: ImageList_SetColorTable 函式
description: 設定影像清單的色彩表。
ms.assetid: 1b62f468-cbc4-479b-b9f8-5553c2bd8c79
keywords:
- ImageList_SetColorTable 函式 Windows 控制項
topic_type:
- apiref
api_name:
- ImageList_SetColorTable
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7de1acd8f14d9993bc75ea69b910b365e29156a6386933ccb95251a916c37244
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118412236"
---
# <a name="imagelist_setcolortable-function"></a>ImageList \_ SetColorTable 函式

設定影像清單的色彩表。

## <a name="syntax"></a>語法


```C++
int ImageList_SetColorTable(
  _In_ HIMAGELIST himl,
  _In_ int        start,
  _In_ int        len,
  _In_ RGBQUAD    *prgb
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*himl* \[在\]
</dt> <dd>

類型： **HIMAGELIST**

影像清單的控制碼。

</dd> <dt>

*開始* \[在\]
</dt> <dd>

類型： **int**

以零為基礎的色彩表索引，指定要設定的第一個色彩資料表專案。

</dd> <dt>

*len* \[在\]
</dt> <dd>

類型： **int**

要設定的色彩資料表專案數目。

</dd> <dt>

*prgb* \[在\]
</dt> <dd>

類型： **[ **RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad)\***

*Len* [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad)結構陣列的指標，其中包含 DIB 色彩表的新色彩資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **int**

如果函式成功，它會傳回函數所設定的色彩資料表專案數目。 如果函式失敗，則傳回值小於或等於零。

## <a name="remarks"></a>備註

只有使用 [**Ilc.out \_ COLOR4**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) 或 [**ilc.out \_ COLOR8**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) 旗標建立的影像清單有色彩表。 這類影像清單的色彩表通常是藉由複製加入至清單的第一個影像的色彩表來自動設定 (例如，透過 [**ImageList \_ Add**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add) 函數) 如果該影像是 DIB 的話）。 如果新增至影像清單的第一個影像不是 DIB，則會使用半色調選擇區的色彩表來 **Ilc.out \_ COLOR8** 影像清單，並使用 VGA 色彩表來 **ilc.out \_ COLOR4**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                                  |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                            |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (3.51 版或更新版本) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[色彩表](https://msdn.microsoft.com/library/ms531197(v=VS.85).aspx)
</dt> </dl>

 

