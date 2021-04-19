---
description: BBControl 資料表會列出要顯示在每個佈告欄上的控制項。
ms.assetid: 2ab31a32-6d33-46b7-a295-199560efa7fb
title: BBControl 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfebbdbc474ef88cbf26f34555deb4874840d005
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106987490"
---
# <a name="bbcontrol-table"></a>BBControl 資料表

BBControl 資料表會列出要顯示在每個佈告欄上的控制項。

BBControl 資料表具有下列資料行。



| Column      | 類型                               | 答案 | Nullable |
|-------------|------------------------------------|-----|----------|
| 廣告 牌\_ | [識別碼](identifier.md)       | Y   | N        |
| BBControl   | [識別碼](identifier.md)       | Y   | N        |
| 類型        | [識別碼](identifier.md)       | N   | N        |
| X           | [整數](integer.md)             | N   | N        |
| Y           | [整數](integer.md)             | N   | N        |
| 寬度       | [整數](integer.md)             | N   | N        |
| 高度      | [整數](integer.md)             | N   | N        |
| 屬性  | [DoubleInteger](doubleinteger.md) | N   | Y        |
| Text        | [Text](text.md)                   | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Billboard_"></span><span id="billboard_"></span><span id="BILLBOARD_"></span>廣告 牌\_
</dt> <dd>

佈告欄的名稱。

[佈告欄資料表](billboard-table.md)中第一個資料行的外部索引鍵。

</dd> <dt>

<span id="BBControl"></span><span id="bbcontrol"></span><span id="BBCONTROL"></span>BBControl
</dt> <dd>

控制項的名稱。 這個名稱在佈告欄內必須是唯一的，但可以在不同的公告欄上重複。 這個資料行會與佈告欄資料 \_ 行結合，形成資料表的主要索引鍵。

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>類型
</dt> <dd>

控制項的類型。 只有靜態控制項（例如 [文字](text-control.md)、 [點陣圖](bitmap-control.md)、 [圖示](icon-control.md)或自訂控制項）才能放置在佈告欄上。 如需完整的控制項清單，請參閱 [控制項](controls.md) 一節。

</dd> <dt>

<span id="X"></span><span id="x"></span>X
</dt> <dd>

控制項矩形界限左上角的水準座標。 單位為 [安裝程式單位](installer-units.md)。 此座標是相對於佈告欄控制項來測量，而不是相對於對話方塊。 只使用非負數值。

</dd> <dt>

<span id="Y"></span><span id="y"></span>Y
</dt> <dd>

控制項矩形界限左上角的垂直座標。 單位為 [安裝程式單位](installer-units.md)。 此座標是相對於佈告欄控制項來測量，而不是相對於對話方塊。 此數位必須為非負數。

</dd> <dt>

<span id="Width"></span><span id="width"></span><span id="WIDTH"></span>寬度
</dt> <dd>

控制項矩形邊界的寬度。 單位為 [安裝程式單位](installer-units.md)。 此數位必須為非負數。

</dd> <dt>

<span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>高度
</dt> <dd>

控制項矩形界限的高度。 單位為 [安裝程式單位](installer-units.md)。 此數位必須為非負數。

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性
</dt> <dd>

32位字，指定要套用至這個控制項的屬性旗標。 此數位必須為非負數，並且針對可放置於佈告欄的靜態控制項指定屬性。 如需在此欄位中輸入之數值的詳細資訊，請參閱 [控制項屬性](control-attributes.md)下的特定屬性。

</dd> <dt>

<span id="Text"></span><span id="text"></span><span id="TEXT"></span>文本
</dt> <dd>

此資料行包含可當地語系化的字串，可用來在控制項顯示文字時，設定控制項中的初始文字。 如果文字太長而無法容納在控制項上，則字串會被截斷。 如果控制項是按鈕或包含圖示或點陣圖的核取方塊，則此資料行會包含 [二進位資料表](binary-table.md) 中的索引鍵。 不可能同時在相同的按鈕上顯示文字和圖片。 此資料行可以保留空白。

</dd> </dl>

## <a name="remarks"></a>備註

X、y、寬度和高度的整數值是在 [安裝程式單位](installer-units.md)中，而不是對話方塊單位。 安裝程式單位等於10點 MS sans-serif 字型大小的一到第十二個高度。 控制項的座標相對於佈告欄控制項而不是對話方塊。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE45](ice45.md)  
[ICE95](ice95.md)  
</dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
</dt> </dl>

 

 



