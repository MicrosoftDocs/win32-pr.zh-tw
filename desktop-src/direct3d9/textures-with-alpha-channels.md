---
description: 有兩種方式可以對呈現較複雜透明度的材質貼圖進行編碼。
ms.assetid: cae788f6-60f1-4987-8f06-bf4256bccd9b
title: '具有 Alpha 通道的材質 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 934660a62c0257de1549ccec09f9bb77e5c02c4c22baf1e1dc9cc8dffef03f4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118290521"
---
# <a name="textures-with-alpha-channels-direct3d-9"></a>具有 Alpha 通道的材質 (Direct3D 9) 

有兩種方式可以對呈現較複雜透明度的材質貼圖進行編碼。 在每個例子中，描述透明度的區塊都會優先於之前已描述完成的 64 位元區塊。 透明度通常不是透過每像素 4 個位元 (明確編碼) 的 4 x 4 點陣圖呈現，就是透過較少位元並且類比於色彩編碼的線性插補呈現。

透明度區塊及色彩區塊會如下表所示進行排列。



| 單字位址 | 64 位元區塊                      |
|--------------|-----------------------------------|
| 3:0          | 透明度區塊                |
| 7:4          | 之前已描述完成的 64 位元區塊 |



 

## <a name="explicit-texture-encoding"></a>明確材質編碼

針對 (DXT2 和 DXT3 格式的明確材質編碼) ，描述透明度之材質的 Alpha 元件會編碼為每個材質4個位的4x4 點陣圖。 這四個位元可透過不同的方式達成，例如：遞色，或是使用 Alpha 資料中最高有效的四個位元。 無論其產生方式為何，其會直接使用於程式之中，而不會有任何型式的插補。

下列簡圖呈現了一個 64 位元的透明度區塊。

![64 位元透明度區塊的簡圖](images/colors4.png)

> [!Note]  
> Direct3D 的壓縮方法會使用四個最重要的位。

 

下表描述了如何在記憶體中，針對每個 16 位元文字配置 Alpha 資訊。

此資料表包含 word 0 的版面配置。



| Bits          | Alpha      |
|---------------|------------|
| 3:0 (LSB \*)    | \[0 \] \[ 0\] |
| 7:4           | \[0 \] \[ 1\] |
| 11:8          | \[0 \] \[ 2\] |
| 15:12 (MSB \*)  | \[0 \] \[ 3\] |



 

\*最重要的 bit、最重要的位 (MSB) 

此資料表包含 word 1 的版面配置。



| Bits        | Alpha      |
|-------------|------------|
| 3:0 (LSB)   | \[1 \] \[ 0\] |
| 7:4         | \[1 \] \[ 1\] |
| 11:8        | \[1 \] \[ 2\] |
| 15:12 (MSB) | \[1 \] \[ 3\] |



 

此資料表包含 word 2 的版面配置。



| Bits        | Alpha      |
|-------------|------------|
| 3:0 (LSB)   | \[2 \] \[ 0\] |
| 7:4         | \[2 \] \[ 1\] |
| 11:8        | \[2 \] \[ 2\] |
| 15:12 (MSB) | \[2 \] \[ 3\] |



 

此資料表包含 word 3 的版面配置。



| Bits        | Alpha      |
|-------------|------------|
| 3:0 (LSB)   | \[3 \] \[ 0\] |
| 7:4         | \[3 \] \[ 1\] |
| 11:8        | \[3 \] \[ 2\] |
| 15:12 (MSB) | \[3 \] \[ 3\] |



 

DXT2 和 DXT3 之間的差異在於，使用 DXT2 格式時，會假設色彩資料已由 Alpha 預乘。 使用 DXT3 格式時，會假設色彩不會以 Alpha 預乘。 這兩種格式是需要的，因為在大部分情況下，使用材質時，檢查資料是否不足以判斷色彩值是否已乘以 Alpha。 因為在執行時間需要這項資訊，所以會使用兩個 FOURCC 碼來區分這些情況。 不過，這兩種格式所使用的資料和插補方法相同。

DXT1 中使用的色彩比較，可判斷材質是否為透明的，不會使用此格式。 若不使用色彩比較，色彩資料預設會以 4 色模式進行處理。 換句話說，DXT1 程式碼頂端的 if 語句應如下所示：


```
if ((color_0 > color_1) OR !DXT1) {
```



## <a name="three-bit-linear-alpha-interpolation"></a>Three-Bit 線性 Alpha 插補

DXT4 和 DXT5 格式的透明度編碼是以類似于色彩使用的線性編碼的概念為基礎。 兩個 8 位元 Alpha 值和一個每個像素中有三個位元的 4 x 4 點陣圖，會儲存於區塊中前八個位元組。 代表 Alpha 值會作為插補中繼 Alpha 值之用途使用。 其他資訊會以兩個 Alpha 值儲存的方式供作使用。 如果 Alpha \_ 0 大於 Alpha \_ 1，則插補會建立六個中間 Alpha 值。 若為小於，則四個中繼 Alpha 值會插補於指定的 Alpha 極端值之間。 另外兩個額外隱含 Alpha 值則為 0 (完全透明) 及 255 (完全不透明)。

下列程式碼示範了這個演算法。


```
// 8-alpha or 6-alpha block?    
if (alpha_0 > alpha_1) {    
    // 8-alpha block:  derive the other six alphas.    
    // Bit code 000 = alpha_0, 001 = alpha_1, others are interpolated.
    alpha_2 = (6 * alpha_0 + 1 * alpha_1 + 3) / 7;    // bit code 010
    alpha_3 = (5 * alpha_0 + 2 * alpha_1 + 3) / 7;    // bit code 011
    alpha_4 = (4 * alpha_0 + 3 * alpha_1 + 3) / 7;    // bit code 100
    alpha_5 = (3 * alpha_0 + 4 * alpha_1 + 3) / 7;    // bit code 101
    alpha_6 = (2 * alpha_0 + 5 * alpha_1 + 3) / 7;    // bit code 110
    alpha_7 = (1 * alpha_0 + 6 * alpha_1 + 3) / 7;    // bit code 111  
}    
else {  
    // 6-alpha block.    
    // Bit code 000 = alpha_0, 001 = alpha_1, others are interpolated.
    alpha_2 = (4 * alpha_0 + 1 * alpha_1 + 2) / 5;    // Bit code 010
    alpha_3 = (3 * alpha_0 + 2 * alpha_1 + 2) / 5;    // Bit code 011
    alpha_4 = (2 * alpha_0 + 3 * alpha_1 + 2) / 5;    // Bit code 100
    alpha_5 = (1 * alpha_0 + 4 * alpha_1 + 2) / 5;    // Bit code 101
    alpha_6 = 0;                                      // Bit code 110
    alpha_7 = 255;                                    // Bit code 111
}
```



Alpha 區塊的記憶體配置如下︰



| Byte | Alpha                                                          |
|------|----------------------------------------------------------------|
| 0    | Alpha \_ 0                                                       |
| 1    | Alpha \_ 1                                                       |
| 2    | \[0 \] \[ 2 \] (2 MSBs) ， \[ 0 \] \[ 1 \] ， \[ 0 \] \[ 0\]                    |
| 3    | \[1 \] \[ 1 \] (1 MSB) 、 \[ 1 \] \[ 0 \] 、 \[ 0 \] \[ 3 \] 、 \[ 0 \] \[ 2 \] (1 LSB)  |
| 4    | \[1 \] \[ 3 \] ， \[ 1 \] \[ 2 \] ， \[ 1 \] \[ 1 \] (2 LSBs)                     |
| 5    | \[2 \] \[ 2 \] (2 MSBs) ， \[ 2 \] \[ 1 \] ， \[ 2 \] \[ 0\]                    |
| 6    | \[3 \] \[ 1 \] (1 MSB) 、 \[ 3 \] \[ 0 \] 、 \[ 2 \] \[ 3 \] 、 \[ 2 \] \[ 2 \] (1 LSB)  |
| 7    | \[3 \] \[ 3 \] ， \[ 3 \] \[ 2 \] ， \[ 3 \] \[ 1 \] (2 LSBs)                     |



 

DXT4 和 DXT5 之間的差異在於，在 DXT4 格式中，假設色彩資料已由 Alpha 預乘。 使用 DXT5 格式時，會假設色彩未以 Alpha 預乘。 這兩種格式是需要的，因為在大部分情況下，使用材質時，檢查資料是否不足以判斷色彩值是否已乘以 Alpha。 因為在執行時間需要這項資訊，所以會使用兩個 FOURCC 碼來區分這些情況。 不過，這兩種格式所使用的資料和插補方法相同。

DXT1 中使用的色彩比較，可判斷材質是否為透明，而不會搭配這些格式使用。 若不使用色彩比較，色彩資料預設會以 4 色模式進行處理。 換句話說，DXT1 程式碼頂端的 if 語句應該是：


```
if ((color_0 > color_1) OR !DXT1) {
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[壓縮的材質資源](compressed-texture-resources.md)
</dt> </dl>

 

 



