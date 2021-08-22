---
title: 'C (OpenGL) '
description: 以字母 C 為開頭之 OpenGL 詞彙的定義。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 037c39b1-b728-41d3-a664-c0aa6c487103
keywords:
- 用戶端電腦
- 用戶端記憶體
- 剪輯座標
- 裁剪
- 色彩索引
- 色彩索引模式
- 色彩對應
- components
- 內容
- 凸
- 凸殼
- 座標系統
- 撲殺
- 目前的矩陣
- 目前的點陣位置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39007e4719e1f4507555bf5aafa3187a897756d1d33580e9facc8fa0f6d8fa3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675988"
---
# <a name="c-opengl"></a>C (OpenGL) 

[](a.md) [B](b.md) C [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [](u-v.md) [W](w.md) [X Y Z](x-y-z.md)

<dl> <dt>

<span id="opengl_client_computer"></span><span id="OPENGL_CLIENT_COMPUTER"></span>**用戶端電腦**
</dt> <dd>

用來發出 OpenGL 命令的電腦。 發出 OpenGL 命令的電腦可以透過網路連接到執行命令的另一部電腦，或者可以在同一部電腦上發出和執行命令。 另請參閱 [伺服器](s.md)。

</dd> <dt>

<span id="opengl_client_memory"></span><span id="OPENGL_CLIENT_MEMORY"></span>**用戶端記憶體**
</dt> <dd>

在用戶端電腦) 儲存程式變數的主要記憶體 (。

</dd> <dt>

<span id="opengl_clip_coordinates"></span><span id="OPENGL_CLIP_COORDINATES"></span>**剪輯座標**
</dt> <dd>

接下來的座標系統會依照投射矩陣進行轉換，然後在透視區之前。 視圖-磁片區裁剪是在剪切座標中完成，但應用程式特定的剪輯則否。 另請參閱 [應用程式特定的剪輯](a.md)。

</dd> <dt>

<span id="opengl_clipping"></span><span id="OPENGL_CLIPPING"></span>**裁剪**
</dt> <dd>

消除裁剪平面所定義之半形以外的幾何基本物件部分。 只有在外部時，才會拒絕點。 將會排除一半空格以外的線條或多邊形的部分，並視需要產生額外的頂點，以在裁剪的一半空間內完成基本。 幾何基本專案和目前的點陣位置 (當指定的) 一律會針對視圖音量的左邊、右邊、下、上、近端和目前平面所定義的六個空格進行裁剪。 應用程式可以指定選擇性的應用程式特定裁剪平面，以套用於眼睛座標中。

</dd> <dt>

<span id="opengl_color_index"></span><span id="OPENGL_COLOR_INDEX"></span>**色彩索引**
</dt> <dd>

表示依名稱的色彩，而不是依值的單一值。 OpenGL 色彩索引會視為連續值 (例如，浮點數) ，而運算（例如插補和遞色）則會在其上執行。 不過，儲存在框架緩衝區中的色彩索引一律為整數值。 浮點數索引會四捨五入為最接近的整數值，以轉換成整數。

</dd> <dt>

<span id="opengl_color_index_mode"></span><span id="OPENGL_COLOR_INDEX_MODE"></span>**色彩索引模式**
</dt> <dd>

OpenGL 內容的模式，其中的色彩緩衝區會儲存色彩索引，而不是紅色、綠色、藍色和 Alpha 色彩的元件。

</dd> <dt>

<span id="opengl_color_map"></span><span id="OPENGL_COLOR_MAP"></span>**色彩地圖**
</dt> <dd>

顯示硬體所存取之索引至 RGB 對應的資料表。 每個色彩索引都會從色彩緩衝區讀取，並在顏色對應中透過查閱轉換成 RGB 三重，並傳送至監視器。

</dd> <dt>

<span id="opengl_component"></span><span id="OPENGL_COMPONENT"></span>**元件**
</dt> <dd>

單一、連續的 (例如，代表濃度或數量的浮點) 值。 通常，元件值為零代表最小值或濃度，而元件值為1代表最大值或濃度，不過有時候會使用其他正規化。 由於元件值會在正規化的範圍內轉譯，因此它們會與實際的解析度分開指定。 例如，RGB 三 (1，1，1) 是白色，不論色彩緩衝區儲存的是4、8或12位。 範圍外的元件通常會壓制至正規化範圍，而不會被截斷或以其他方式轉譯。 例如，RGB 三 (1.4、1.5、0.9) 壓制為 (1.0、1.0、0.9) ，然後再用來更新色彩緩衝區。 紅色、綠色、藍色、Alpha 和深度一律會被視為元件，而不是索引。

</dd> <dt>

<span id="opengl_context"></span><span id="OPENGL_CONTEXT"></span>**上下文**
</dt> <dd>

一組完整的 OpenGL 狀態變數。 請注意，畫面格緩衝區內容不是 OpenGL 狀態的一部分，但畫面格緩衝區的設定為。

</dd> <dt>

<span id="opengl_convex"></span><span id="OPENGL_CONVEX"></span>**凸**
</dt> <dd>

多邊形的條件，在多邊形的平面中，沒有任何直線與多邊形相交兩倍以上。

</dd> <dt>

<span id="opengl_convex_hull"></span><span id="OPENGL_CONVEX_HULL"></span>**凸殼**
</dt> <dd>

封閉指定點群組的最小凸區域。 在兩個維度中，凸殼在概念上是藉由在點周圍延展橡皮線來找出，讓所有點都落在頻內。

</dd> <dt>

<span id="opengl_coordinate_system"></span><span id="OPENGL_COORDINATE_SYSTEM"></span>**座標系統**
</dt> <dd>

在 n 維度空間中，一組 n 個線性獨立的向量，而且錨定某個點 (稱為原點)。 座標群組會指定 spaceIn n 維度空間中的點，這是一組指向點 (的 n 個線性獨立向量，稱為「原始) 」。 一組座標會指定空間中的某個點 (或是從原點算起的向量)，方法是指出要沿著每一個向量行進多遠才能到達此點 (或是向量的尖端)。 從原點) 的 (或向量，指出每個向量的行進距離，以達到向量)  (或刀尖的位置。

</dd> <dt>

<span id="opengl_culling"></span><span id="OPENGL_CULLING"></span>**撲殺**
</dt> <dd>

消除多邊形正面或背面的程式，讓臉部不會繪製。

</dd> <dt>

<span id="opengl_current_matrix"></span><span id="OPENGL_CURRENT_MATRIX"></span>**目前的矩陣**
</dt> <dd>

將一個座標系統中的座標轉換成另一個系統座標的矩陣。 OpenGL 中有三個目前的矩陣：模型矩陣，此矩陣會將程式設計人員) 指定的座標 (座標轉換為眼睛座標;將眼睛座標轉換成剪切座標的透視圖矩陣;和材質矩陣，會轉換指定或產生的材質座標（如同矩陣所述）。 每個目前的矩陣都是矩陣堆疊上的最上層元素。 這三個堆疊中的每一個都可以使用 OpenGL 矩陣操作命令來操作。

</dd> <dt>

<span id="opengl_current_raster_position"></span><span id="OPENGL_CURRENT_RASTER_POSITION"></span>**目前的點陣位置**
</dt> <dd>

視窗座標位置，指定影像基本的位置（當影像成為柵格化時）。 呼叫 glRasterpos 時，會更新目前的點陣位置和其他目前的點陣參數。

</dd> </dl>

 

 




