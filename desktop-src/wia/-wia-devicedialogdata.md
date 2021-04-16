---
description: 定義呼叫裝置對話方塊所需的資料。
ms.assetid: 424defa6-1452-4a8b-bacc-738209c236c3
title: 'DEVICEDIALOGDATA 結構 (Wiadefd .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEVICEDIALOGDATA
api_type:
- HeaderDef
api_location:
- Wiadefd.h
ms.openlocfilehash: 621cab4f56b39ac900048018463935b55f0eddec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513432"
---
# <a name="devicedialogdata-structure"></a>DEVICEDIALOGDATA 結構

定義呼叫裝置對話方塊所需的資料。

## <a name="syntax"></a>語法


```C++
typedef struct {
  DWORD    cbSize;
  HWND     hwndParent;
  IWiaItem *pIWiaItemRoot;
  DWORD    dwFlags;
  LONG     lIntent;
  LONG     lItemCount;
  IWiaItem **ppWiaItem;
} DEVICEDIALOGDATA;
```



## <a name="members"></a>成員

<dl> <dt>

**cbSize**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

指定此結構的大小（以位元組為單位）。

</dd> <dt>

**hwndParent**
</dt> <dd>

類型： **HWND**

</dd> <dd>

指定對話方塊父視窗的控制碼。

</dd> <dt>

**pIWiaItemRoot**
</dt> <dd>

類型： **[**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) \** _

</dd> <dd>

指向 [_ *IWiaItem* *](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)介面，表示應用程式專案樹狀結構中的有效根專案。

</dd> <dt>

**dwFlags**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

指定一組旗標來控制對話方塊的操作。 可以設定為下列任何值：



| 旗標                                 | 意義                                                                                                                                                                                     |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                                    | 預設行為。                                                                                                                                                                           |
| WIA \_ 裝置 \_ 對話方塊 \_ 單一 \_ 影像   | 在 [裝置映射取得] 對話方塊中，將影像選取範圍限制為單一影像。                                                                                                      |
| WIA \_ 裝置 \_ 對話方塊 \_ 使用 \_ 一般 \_ UI | 使用系統 UI （如果有的話），而不是廠商提供的 UI。 如果系統 UI 無法使用，則會使用廠商 UI。 如果沒有可用的 UI，函數會傳回 E \_ >notimpl。 |



 

</dd> <dt>

**lIntent**
</dt> <dd>

類型： **LONG**

</dd> <dd>

指定影像所要代表的資料類型。 如需影像意圖值的清單，請參閱 [**影像意圖常數**](-wia-imageintentconstants.md)。

</dd> <dt>

**lItemCount**
</dt> <dd>

類型： **LONG**

</dd> <dd>

接收 **ppWiaItem** 參數所指定之陣列中的專案數。

</dd> <dt>

**ppWiaItem**
</dt> <dd>

類型： **[ **IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)\*\***

</dd> <dd>

接收 [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) 介面指標陣列的位址。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Wiadefd。h</dt> </dl> |



 

 




