---
title: 通用控制項參數
description: 以下描述 control 資源定義語句的一般語法。
ms.assetid: e7a49a9f-93b5-4221-8006-3d1864b7a6a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abbdbf707e1ee72f62c7c08cb7065f4d1a4b8f2f4c000d52f3a28c9806a21a0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117870559"
---
# <a name="common-control-parameters"></a>通用控制項參數

以下描述 control 資源定義語句的一般語法。 以下提供每個參數的意義。 有時候，語句會以不同的方式使用參數，或可能忽略參數。 語句特定的變化會在語句的檔中說明。

``` syntax
control [[text,]] id, x, y, width, height[[, style[[, extended-style]]]][, helpId]
[{ data-element-1 [, data-element-2 [,  . . . ]]}]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*文本*
</dt> <dd>

要與控制項一起顯示的文字。 文字位於控制項內或在控制項旁邊。

此參數必須包含以雙引號括住的零或多個字元 ( ") 。 字串會自動以 null 終止，並在產生的資源檔中轉換成 Unicode。

依預設，雙引號之間列出的字元是 ANSI 字元，而 escape 序列則會被視為位元組 escape 序列。 如果字串前面加上 "L" 前置詞，則字串為寬字元字串，且會將 escape 序列轉譯為指定 Unicode 字元的2位元組轉義順序。 如果文字中需要雙引號，則必須包含雙引號兩次。

文字中的 & 符號 (&) 字元表示會使用下列字元作為控制項的助憶鍵字元。 當控制項顯示時，不會顯示 & 符號，但是助憶鍵字元會加上底線。 使用者可以藉由按下對應到加上底線的助憶鍵字元的按鍵來選擇控制項。 若要使用連字號做為字串中的字元，請 (&&) 插入兩個符號。

</dd> <dt>

<span id="id"></span><span id="ID"></span>*Id*
</dt> <dd>

控制識別碼。 這個值必須是0到65535範圍中的16位不帶正負號的整數，或是評估為該範圍中值的簡單算術運算式。

</dd> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

相對於對話方塊左邊的控制項左邊的 X 座標（X）。 這個值必須是0到65535範圍中的16位不帶正負號的整數。 座標是在對話方塊單位中，而且相對於對話方塊、視窗或控制項（包含指定的控制項）的原點。

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Y*
</dt> <dd>

相對於對話方塊頂端之控制項頂端的 Y 座標。 這個值必須是0到65535範圍中的16位不帶正負號的整數。 相對於對話方塊、視窗或控制項（包含指定的控制項）的原點，座標是在對話方塊單位中。

</dd> <dt>

<span id="width"></span><span id="WIDTH"></span>*寬度*
</dt> <dd>

控制項的寬度。 此值必須是介於1到65535之間的16位不帶正負號的整數。 寬度為 1/4 個字元的單位。

</dd> <dt>

<span id="height"></span><span id="HEIGHT"></span>*高度*
</dt> <dd>

控制項的高度。 此值必須是介於1到65535之間的16位不帶正負號的整數。 高度為 1/8 個字元的單位。

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*風格*
</dt> <dd>

控制項樣式。 使用位 OR (\|) 運算子來合併樣式。 如需詳細資訊，請參閱 [視窗樣式](../winmsg/window-styles.md)。

</dd> <dt>

<span id="extended-style"></span><span id="EXTENDED-STYLE"></span>*擴充樣式*
</dt> <dd>

擴充的視窗樣式。 您必須指定 *樣式* 以指定 *延伸樣式*。 如需詳細資訊，請參閱 [**EXSTYLE**](exstyle-statement.md)。

</dd> <dt>

<span id="helpId"></span><span id="helpid"></span><span id="HELPID"></span>*h*
</dt> <dd>

指出在 [**WM \_**](../shell/wm-help.md) 說明處理期間用來識別控制項之識別碼的數值運算式。

</dd> <dt>

<span id="controlData"></span><span id="controldata"></span><span id="CONTROLDATA"></span>*controlData*
</dt> <dd>

控制項的控制項特定資料。 當您建立對話方塊，並在該對話方塊中建立具有控制項特定資料的控制項時，該資料的指標會透過該控制項的 [**WM \_ CREATE**](../winmsg/wm-create.md) message *lParam* 傳遞至控制項的視窗程式。

</dd> </dl>

## <a name="remarks"></a>備註

水準對話單位是對話方塊基底寬度單位的1/4。 垂直單位是對話方塊基底高度單位的1/8。 目前的對話方塊基礎單位是從目前系統字型的高度和寬度計算。 [**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)函式會傳回對話方塊基礎單位（以圖元為單位）。 座標相對於對話方塊的原點。

 

 