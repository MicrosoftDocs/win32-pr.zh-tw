---
title: 點陣圖資源
description: 定義應用程式在其螢幕顯示中使用的點陣圖，或為功能表或控制項中的專案。
ms.assetid: 2db2f7f0-735f-4aac-9813-c04a2f7788b2
keywords:
- 點陣圖資源功能表與其他資源
topic_type:
- apiref
api_name:
- BITMAP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff75f235e8aa1787e93f9420b4d7ed27f440cdc09510547295ebced4ec494bdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118734896"
---
# <a name="bitmap-resource"></a>點陣圖資源

定義應用程式在其螢幕顯示中使用的點陣圖，或為功能表或控制項中的專案。

``` syntax
nameID BITMAP filename
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*
</dt> <dd>

識別資源的唯一名稱或16位不帶正負號的整數值。

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*檔案名*
</dt> <dd>

包含資源的檔案名。 名稱必須是有效的檔案名;如果檔案不在目前的工作目錄中，它必須是完整路徑。 路徑應該是加上引號的字串。

</dd> </dl>

此外，也支援某些屬性以提供回溯相容性。 如需詳細資訊，請參閱 [一般資源屬性](common-resource-attributes.md)。

## <a name="examples"></a>範例

下列範例會定義兩個位圖資源：

``` syntax
disk1   BITMAP "disk.bmp"
12      BITMAP "diskette.bmp"
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用點陣圖](/windows/desktop/gdi/using-bitmaps)
</dt> <dt>

[**LoadBitmap**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa)
</dt> <dt>

[**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea)
</dt> </dl>

 

 