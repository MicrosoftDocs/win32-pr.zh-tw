---
title: 使用進展來表示填補和記憶體版面配置
description: DirectML 張量是由稱為 *大小* 的屬性和 *tensor 的進展* 所描述。
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: b944b1a2600febe27f209bffcc0e355c6a9fc7db
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/23/2019
ms.locfileid: "104548392"
---
# <a name="using-strides-to-express-padding-and-memory-layout"></a>使用進展來表示填補和記憶體版面配置

DirectML 張量是由 &mdash; Direct3D 12 緩衝區所支援，其 &mdash; 由稱為 *大小* 和 tensor *進展的* 屬性來描述。 Tensor 的 *大小* 會描述 tensor 的邏輯維度。 例如，2D tensor 的高度可能是2，而寬度為3。 邏輯上來說，tensor 具有6個相異的元素，但大小並不會指定這些元素如何儲存在記憶體中。 Tensor 的進展 *會描述 tensor* 元素的實體記憶體配置。

## <a name="two-dimensional-2d-arrays"></a>二維 (2D) 陣列

請考慮高度為2且寬度為3的 2D tensor;資料是由文字字元所組成。 在 C/c + + 中，這可能會使用多維度陣列來表示。

```cpp
constexpr int rows = 2;
constexpr int columns = 3;
char tensor[rows][columns];
tensor[0][0] = 'A';
tensor[0][1] = 'B';
tensor[0][2] = 'C';
tensor[1][0] = 'D';
tensor[1][1] = 'E';
tensor[1][2] = 'F';
```

上述 tensor 的邏輯視圖如下所示。

```console
A B C
D E F
```

在 C/c + + 中，多維度陣列是以資料列主要順序儲存。 換句話說，沿著寬度維度的連續元素會連續儲存線上性記憶體空間中。

位移：|0|1|2|3|4|5
-|-|-|-|-|-|-
值：|A|B|C|D|E|F

維度的 *跨距* 是要跳過的專案數，以便存取該維度中的下一個專案。 努力表達記憶體中 tensor 的版面配置。 以資料列為主的順序而言，寬度維度的跨距一律為1，因為沿著維度的相鄰元素會連續儲存。 高度維度的 stride 取決於寬度維度的大小;在上述範例中，沿著高度維度的連續元素之間的距離 (例如，A 到 D) 等於 tensor (的寬度，在此範例) 中為3。

若要說明不同的版面配置，請考慮使用資料行主要順序。 換句話說，沿著高度維度的連續元素會連續儲存線上性記憶體空間中。 在此情況下，高度跨距一律為1，而寬度跨距為 2 (高度維度) 的大小。

位移：|0|1|2|3|4|5
-|-|-|-|-|-|-
值：|A|D|B|E|C|F

## <a name="higher-dimensions"></a>較高的維度

當超過兩個維度時，將配置參考為數據列或資料行的版面配置就變得很困難。 因此，本主題的其餘部分會使用這些詞彙和標籤。

- 2D：「HW」 &mdash; 高度是 (資料列主要) 的最高序位維度。
- 2D：「WH」 &mdash; 寬度是 (資料行主要) 的最高序位維度。
- 3D：「DHW」 &mdash; 深度是最高順序的維度，後面接著 height，然後是 width。
- 3D：「WHD」 &mdash; 寬度是最高順序的維度，後面接著高度，然後是深度。
- 4D： "NCHW" &mdash; (批次大小) 的影像數目，然後是通道的數目，再接著高度，然後是寬度。

一般而言，維度的 *封裝* 跨距等於低序位維度之大小的乘積。 例如，使用 "DHW" 配置，D stride 等於 H * W;H stride 等於 W;而 W stride 等於1。 當 tensor 的總實體大小等於 tensor 的總邏輯大小時，就會將進展視為已 *封裝* ;換句話說，沒有額外的空格或重迭的元素。

讓我們將2D 範例延伸至三個維度，讓我們有深度2、高度2和寬度 3 (的 tensor，共12個邏輯元素) 。

```console
A B C
D E F

G H I
J K L
```

使用 "DHW" 配置時，此 tensor 會以下列格式儲存。

位移：|0|1|2|3|4|5|6|7|8|9|10|11|
-|-|-|-|-|-|-|-|-|-|-|-|-|
值：|A|B|C|D|E|F|G|H|I|J|K|L|

- D-stride = height (2) * width (3) = 6 (例如，' A ' 和 ' G ' ) 之間的距離。
- H-stride = width (3) = 3 (例如，' A ' 和 ' d ' ) 之間的距離。
- W-stride = 1 (例如，' A ' 和 ' B ' ) 之間的距離。

專案的索引/座標的點乘積和進展會提供緩衝區中該元素的位移。 例如，H 元素的位移 (d = 1，h = 0，w = 1) 為7。

{1，0，1} ⋅ {6，3，1} = 1 * 6 + 0 * 3 + 1 * 1 = 7

## <a name="packed-tensors"></a>封裝張量

上述範例說明 *封裝* 的張量。 當) 元素中 tensor (的邏輯大小等於) 專案中緩衝區 (的實際大小，且每個專案都有唯一的位址/位移時，即會將 tensor 視為可 *壓縮* 。 例如，如果緩衝區的長度為12個元素，則會封裝 2x2x3 tensor，而且不會對任何一組元素共用緩衝區中的相同位移。 封裝的張量是最常見的情況;但是，進展可以更複雜的記憶體配置。

## <a name="broadcasting-with-strides"></a>具有進展的廣播

如果 tensor 的 () 專案中的緩衝區大小小於其邏輯維度的乘積，則會遵循專案中必須有一些重迭的元素。 這種情況的一般情況稱為 *廣播*;維度的元素是另一個維度的複本。 例如，讓我們重新審視2D 範例。 假設我們想要以邏輯方式2x3 的 tensor，但第二個數據列與第一個資料列相同。 如下所示。

```console
A B C
A B C
```

這可能會儲存為壓縮的 HW/資料列主要 tensor。 但是更精簡的儲存體只會包含3個元素 (A、B 和 C) ，並使用0的高度跨距，而不是3。 在此情況下，tensor 的實體大小為3個元素，但邏輯大小為6個元素。

一般情況下，如果維度的 stride 為0，則低序位維度中的所有元素都會沿著廣播維度重複;例如，如果 tensor 是 NCHW，而 C stride 是0，則每個通道的值會與 H 和 W 相同。

## <a name="padding-with-strides"></a>具有進步的填補

如果 tensor 的實體大小大於符合其元素所需的大小下限時，就會被稱為 *填補* 。 如果沒有廣播或重迭的元素，則 [專案]) 中 tensor (的最小大小就只是其維度的乘積。 您可以使用 helper 函式 `DMLCalcBufferTensorSize` (參閱 [DirectML helper](dml-helper-functions.md) 函式，以取得該函式的清單) 計算 DirectML 張量的 *最小* 緩衝區大小。

假設緩衝區包含下列值 (' x ' 元素表示填補值) 。

0|1|2|3|4|5|6|7|8|9|
-|-|-|-|-|-|-|-|-|-|
A|B|C|x|x|D|E|F|x|x

填補的 tensor 可以使用5的高度 stride 而非3來描述。 此步驟不會逐步執行3個元素來取得下一個資料列，而是 (3 個 *真正* 元素加上2個填補元素) 。 填補在電腦圖形中很常見，例如，為了確保影像的電源有兩個對齊。

```console
A B C
D E F
```

## <a name="directml-buffer-tensor-descriptions"></a>DirectML 緩衝區 tensor 描述

DirectML 可以使用各種實體 tensor 配置，因為 [ **DML_BUFFER_TENSOR_DESC** 結構](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc)同時具有 `Sizes` 和 `Strides` 成員。 某些運算子實現可能會更有效率地使用特定配置，因此變更儲存 tensor 資料的方式並不常見，以提升效能。

大部分的 DirectML 運算子都需要4D 或5D 張量，而且大小和進展值的順序是固定的。 藉由修正 tensor 描述中的大小和 stride 值順序，DirectML 可以推斷不同的實體版面配置。

**4D**
- [**DML_BUFFER_TENSOR_DESC：：**](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc) size = {N 大小，C-大小，H-大小，W 大小}
- [**DML_BUFFER_TENSOR_DESC：：**](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc) 進展 = {N 個 Stride，C Stride，H-Stride，W-stride}

**5D**
- **DML_BUFFER_TENSOR_DESC：：** size = {N 大小，C-大小，D 大小，H-大小，W-大小}
- **DML_BUFFER_TENSOR_DESC：：** 進展 = {N 個 Stride，C Stride，D-Stride，H-Stride，W-stride}

如果 DirectML 運算子需要4D 或 5D tensor，但實際資料有較小的等級 (例如，2D) ，則開頭的維度應該以1s 填滿。 例如，"HW" tensor 是使用 **DML_BUFFER_TENSOR_DESC：：大小** = {1，1，H，W} 來設定。

如果 tensor 資料儲存在 NCHW/NCDHW 中，除非您想要廣播或填補，否則不需要設定 **DML_BUFFER_TENSOR_DESC：：進步**。 您可以將 [進展] 欄位設定為 `nullptr` 。 但是，如果 tensor 的資料儲存在另一個配置中（例如 NHWC），則您需要進展，才能將 NCHW 的轉換表示為該版面配置。

如需簡單的範例，請考慮高度為3和寬度為5的 2D tensor 描述。

**封裝 NCHW (隱含的進展)**
- **DML_BUFFER_TENSOR_DESC：：大小** = {1，1，3，5}
- **DML_BUFFER_TENSOR_DESC：：進步** = `nullptr`

**封裝 NCHW (明確的進展)**
- N-stride = C-size * H-size * W-size = 1 * 3 * 5 = 15
- C-stride = H-size * W-size = 3 * 5 = 15
- H-stride = W-size = 5
- W-stride = 1
- **DML_BUFFER_TENSOR_DESC：：大小** = {1，1，3，5}
- **DML_BUFFER_TENSOR_DESC：：進步** = {15，15，5，1}

**封裝 NHWC**
- N 個 stride = H-size * W-size * C-size = 3 * 5 * 1 = 15
- H-stride = W-size * C-size = 5 * 1 = 5
- W-stride = C-大小 = 1
- C-stride = 1
- **DML_BUFFER_TENSOR_DESC：：大小** = {1，1，3，5}
- **DML_BUFFER_TENSOR_DESC：：進步** = {15，1，5，1}

## <a name="see-also"></a>另請參閱

* [DirectML helper 函式](dml-helper-functions.md)
* [DML_BUFFER_TENSOR_DESC 結構](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc)
