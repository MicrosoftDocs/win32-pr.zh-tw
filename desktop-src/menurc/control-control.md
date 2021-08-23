---
title: CONTROL 控制項
description: 定義使用者定義控制項。
ms.assetid: e5e7b7af-e2b0-41ff-b697-b9ea80e7c61f
keywords:
- 控制控制項功能表和其他資源
topic_type:
- apiref
api_name:
- CONTROL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 069449b5eef83cef7b7bdfac1c61aacb0ceac97cbbdd6e6fb2c139c43b3bae13
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663058"
---
# <a name="control-control"></a>CONTROL 控制項

定義使用者定義控制項。

``` syntax
CONTROL text, id, class, style, x, y, width, height [, extended-style]
```

<dl> <dt>

<span id="class"></span><span id="CLASS"></span>*類*
</dt> <dd>

定義類別的名稱、字元字串或16位不帶正負號的整數值。 這可以是任何一個控制項類別，如需控制項類別的清單，請參閱此描述後面的第一個清單。 如果值是應用程式所提供的重新定義名稱，則必須是以雙引號括住的字串 ( ") 。

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*風格*
</dt> <dd>

重新定義的名稱或整數值，可指定指定控制項的樣式。 *樣式* 的確切意義取決於 *類別* 值。 此描述後面的各節會顯示控制項類別和對應的樣式。

</dd> </dl>

如需控制語句之一般語法的詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。

## <a name="remarks"></a>備註

下列各節將說明六個可能的控制項類別。

### <a name="the-button-control-class"></a>Button 控制項類別

按鈕控制項是一個小型的矩形子視窗，使用者可以按一下滑鼠將其開啟或關閉。 按鈕控制項可以單獨使用，也可以在群組中使用，也可以在不使用文字的情況下標記或顯示。 按鈕控制項通常會在使用者按一下時變更外觀。

按鈕樣式將在下列主題中說明： [按鈕樣式](../controls/button-styles.md)。

### <a name="the-combo-box-control-class"></a>下拉式方塊控制項類別

下拉式方塊控制項包含選項欄位，類似于編輯控制項加上清單方塊。 清單方塊可能會隨時顯示，或在使用者選取 [選取範圍] 欄位旁的 [彈出方塊] 時下降。

根據下拉式方塊的樣式，使用者可以或無法編輯選取欄位的內容。 如果看不到清單方塊，請在選取方塊中輸入字元，將會導致符合輸入之字元的第一個專案反白顯示。 相反地，在清單方塊中選取專案時，會在 [選取範圍] 欄位中顯示選取的文字。

下列主題將說明下拉式方塊控制項樣式： [下拉式方塊樣式](../controls/combo-box-styles.md)。

### <a name="the-edit-control-class"></a>編輯控制項類別

編輯控制項是一個矩形子視窗，使用者可以在其中輸入鍵盤中的文字。 使用者選取控制項，並為其提供輸入焦點，方法是按一下其中的滑鼠，或按下 TAB 鍵。 當控制項顯示閃爍的插入點時，使用者可以輸入文字。 您可以使用滑鼠來移動游標並選取要取代的字元，或將游標置於插入字元的位置。 倒退鍵可以用來刪除字元。

編輯控制項使用固定音調字型，並顯示 Unicode 字元。 它們會將 tab 字元展開為將游標移至下一個索引標籤時所需的空白字元數。 Tab 鍵會假設為每8個字元的位置。

下列主題描述編輯控制項樣式： [編輯控制項樣式](../controls/edit-control-styles.md)。

### <a name="the-list-box-control-class"></a>清單方塊控制項類別

清單方塊控制項是由字元字串清單所組成。 每當應用程式需要顯示使用者可查看和選取的名稱清單（例如檔案名）時，就會使用此控制項。 使用者可以選取字串，方法是使用滑鼠指向字串，然後按一下滑鼠按鍵。 選取字串時，會將它反白顯示，並將通知訊息傳遞至父視窗。 捲軸可以與清單方塊控制項搭配使用，以滾動對控制項視窗而言太長或太寬的清單。

下列主題將描述清單方塊控制項樣式： [清單方塊樣式](../controls/list-box-styles.md)。

### <a name="the-scroll-bar-control-class"></a>Scroll-Bar Control 類別

捲軸控制項是包含捲動方塊的矩形，而且兩端都有方向箭號。 每當使用者按一下控制項中的滑鼠時，捲軸就會將通知訊息傳送至其父代。 如有必要，父系負責更新 thumb 位置。 捲軸控制項的外觀和功能，與一般視窗中使用的捲軸相同。 但不同于捲軸，捲軸控制項可以放在視窗內的任何位置，並在需要時使用，以提供視窗的滾動輸入。

捲軸樣式將在下列主題中說明： [捲軸控制項樣式](../controls/scroll-bar-control-styles.md)。

### <a name="the-static-control-class"></a>靜態控制項類別

靜態控制項是可用於標記、方塊或分隔其他控制項的簡單文字欄位、方塊和矩形。 靜態控制項不需要輸入，也不提供輸出。

下列主題描述靜態控制項樣式： [靜態控制項樣式](../controls/static-control-styles.md)。

 

 