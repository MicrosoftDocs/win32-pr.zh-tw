---
title: 'glPixelTransferf 函式 (Gl) '
description: 'GlPixelTransferf 和 glPixelTransferi 函數會設定圖元傳輸模式。 |glPixelTransferf 函式 (Gl) '
ms.assetid: c18ecbb9-af2a-4662-8e3f-0ac850b04fc1
keywords:
- glPixelTransferf 函式 OpenGL
topic_type:
- apiref
api_name:
- glPixelTransferf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc2268147511a40aaf70a928c77b177f76870e65a7f40da4f2c6bf9428f67db8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118358568"
---
# <a name="glpixeltransferf-function"></a>glPixelTransferf 函式

**GlPixelTransferf** 和 [**glPixelTransferi**](glpixeltransferi.md)函數會設定圖元傳輸模式。

## <a name="syntax"></a>語法


```C++
void WINAPI glPixelTransferf(
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pname* 
</dt> <dd>

要設定之圖元傳輸參數的符號名稱。 下表提供每個以 **glPixelTransfer** 設定之圖元傳輸參數的類型、初始值和有效值範圍。



| Pname             | 類型    | 初始值  | 有效範圍  |
|-------------------|---------|----------------|--------------|
| GL \_ 地圖 \_ 色彩    | Boolean | false          | true/false   |
| GL \_ 地圖 \_ 範本  | Boolean | false          | true/false   |
| GL \_ 索引 \_ 移位  | 整數 | 0              |  (8、8)         |
| GL \_ 索引 \_ 位移 | 整數 | 0              |  (8、8)         |
| GL \_ RED \_ SCALE    | 整數 | 1.0            |  (8、8)         |
| GL \_ 綠 \_ 級  | FLOAT   | 1.0            |  (8、8)         |
| GL \_ 藍色 \_ 調整   | FLOAT   | 1.0            |  (8、8)         |
| GL \_ ALPHA \_ 刻度  | FLOAT   | 1.0            |  (8、8)         |
| GL \_ 深度 \_ 調整  | FLOAT   | 1.0            |  (8、8)         |
| GL \_ 紅色 \_ 偏差     | FLOAT   | 0.0            |  (8、8)         |
| GL \_ 綠色 \_ 偏差   | FLOAT   | 0.0            |  (8、8)         |
| GL \_ 藍色 \_ 偏差    | FLOAT   | 0.0            |  (8、8)         |
| GL \_ ALPHA \_ 偏差   | FLOAT   | 0.0            |  (8、8)         |
| GL \_ 深度 \_ 偏差   | FLOAT   | 0.0            |  (8、8)         |



 

</dd> <dt>

*param* 
</dt> <dd>

*Pname* 設定為的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

**GlPixelTransfer** 函式會設定圖元傳輸模式，其會影響後續 [**glCopyPixels**](glcopypixels.md)、 [**glCopyTexImage1D**](glcopyteximage1d.md)、 [**glCopyTexImage2D**](glcopyteximage2d.md)、 [**glCopyTexSubImage1D**](glcopytexsubimage1d.md)、 [**glCopyTexSubImage2D**](glcopytexsubimage2d.md)、 [**glDrawPixels**](gldrawpixels.md)、 [**glReadPixels**](glreadpixels.md)、 [**glTexImage1D**](glteximage1d.md)、 [**glTexImage2D**](glteximage2d.md)、 [**glTexSubImage1D**](gltexsubimage1d.md)和 [**glTexSubImage2D**](gltexsubimage2d.md)命令的操作。 圖元傳輸模式所指定的演算法在從畫面格緩衝區讀取之後，會以圖元為單位運作， (**glReadPixels** 和 **glCopyPixels**) 或從用戶端記憶體 (**glDrawPixels**、 **glTexImage1D** 和 **glTexImage2D**) 解壓縮。 圖元傳送作業會以相同的順序進行，並以相同的方式執行，而不論造成圖元運算的命令為何。 圖元儲存模式 ([**glPixelStore**](glpixelstore-functions.md)) 控制要從用戶端記憶體中讀取的圖元，以及將圖元包裝回用戶端記憶體的方式。

圖元傳輸作業會處理四個基本圖元類型： *色彩*、 *色彩索引*、 *深度* 和 *樣板。* 色彩圖元是由四個具有未指定尾數和指數大小的浮點值所組成，其縮放比例為0.0 表示零濃度，1.0 代表完整濃度。 色彩索引是由單一固定點值組成，而且在二進位點右邊沒有未指定的精確度。 深度圖元組成單一浮點值，具有未指定的尾數和指數大小，可進行調整以使0.0 表示最小深度緩衝區值，1.0 則代表最大深度緩衝區值。 最後，樣板圖元是由單一固定點值組成，而且在二進位點右邊沒有未指定的精確度。

在四個基本圖元類型上執行的圖元傳送作業如下所示：



| 圖元類型  | 圖元傳送作業                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Color       | 四個色彩元件的每一個都乘以一個縮放因數，然後再加上偏差因數。 也就是說，紅色的元件會乘以 GL \_ red \_ scale，然後新增至 gl \_ 紅色 \_ 偏差; 綠色的元件會乘以 gl \_ 綠 \_ 級，然後新增至 gl \_ 綠色 \_ 偏差; 藍色元件會乘以 GL \_ 藍色 \_ 比例，然後再新增至 gl \_ blue \_ 偏差; Alpha 元件會乘以 gl \_ Alpha 小數位數，然後 \_ 再新增至 gl \_ Alpha \_ 偏差。 當四個色彩元件都經過縮放和偏誤之後，每個都壓制至範圍 \[ 0，1 \] 。 所有色階和偏差值都是使用 **glPixelTransfer** 來指定。 <br/> 如果 GL \_ 地圖 \_ 色彩為 true，每個色彩元件都會依對應的色彩對應色彩來調整，然後由已調整的元件所索引的地圖內容取代。 也就是說，紅色的元件會依照 GL \_ 圖元 \_ 地圖 \_ r 大小調整 \_ \_ \_ ，然後 \_ 以 gl 圖元地圖 r 的內容取代 \_ \_ \_ 為 \_ 其本身的索引。 綠色的元件會依 GL \_ 圖元 \_ 地圖 \_ g 大小調整 \_ \_ \_ ，然後以 gl 圖元地圖 g 的內容取代 \_ \_ \_ \_ 為 \_ 其本身的索引。 藍色元件會依照 GL \_ 圖元 \_ 地圖 b 的 \_ \_ 大小調整為 \_ b \_ ，然後 \_ 以 gl 圖元地圖 b 的內容取代 \_ \_ \_ 為 b 的 \_ 索引。 Alpha 元件會依照 GL \_ 圖元 \_ 地圖 a 調整 \_ \_ 為 \_ \_ 大小，然後以 gl 圖元地圖的內容取代為 \_ \_ \_ \_ \_ 索引。 從對應取得的所有元件都會壓制至範圍 \[ 0、1 \] 。 GL \_ 地圖 \_ 色彩是以 **glPixelTransfer** 指定的。 不同對應的內容是以 **glPixelMap** 指定的。<br/>                                                                                                                        |
| 色彩索引 | 每個色彩索引都會由 GL \_ 索引 \_ 移位位左移，填滿由固定點索引所送出之分數位數目以外的零。 如果 GL \_ 索引 \_ 移位是負數，則右移會再次填滿零。 然後，會將 GL \_ 索引 \_ 位移新增至索引。 GL \_ 索引 \_ 移位和 gl \_ 索引 \_ 位移會以 **glPixelTransfer** 指定。<br/> 從此時開始，作業分歧取決於所產生之圖元的必要格式。 如果產生的圖元要寫入至色彩索引緩衝區，或將它們讀回 GL 色彩索引格式的用戶端記憶體 \_ \_ ，則會繼續將圖元視為索引。 如果 GL \_ 對應 \_ 色彩為 true，則每個索引都會遮罩 2 ^ *n* 1，其中 *n* 是 gl \_ 圖元 \_ 地圖 \_ i \_ 到 \_ i 的 \_ 大小，然後以 gl 圖元地圖的內容取代，並 \_ \_ \_ \_ 以 \_ 遮罩的值進行索引。 GL \_ 地圖 \_ 色彩是以 **glPixelTransfer** 指定的。 索引對應的內容是以 **glPixelMap** 指定的。<br/> 如果產生的圖元要寫入 RGBA 色彩緩衝區，或將其以 GL 色彩索引以外的格式讀回用戶端記憶體 \_ \_ ，則會參考四個 maps GL \_ 圖元 \_ 地圖 \_ i \_ 到 \_ R、GL \_ 圖元 \_ 地圖 \_ i \_ 到 \_ G、gl \_ 圖元 \_ 地圖 \_ i \_ 到 \_ B，以及將 \_ i 圖元地圖移 \_ \_ \_ 至 \_ a，以從索引轉換為色彩。 在進行取值之前，索引會由2個 n 1 遮罩，其中 n 是 GL \_ 圖元 \_ 對應 \_ i \_ 到 \_ 紅色地圖的 R \_ 大小、gl \_ 圖元地圖 i 至綠色地圖的大小、gl 圖元地圖 i 到 \_ B 的 \_ \_ \_ \_ \_ 藍色地圖大小， \_ \_ \_ \_ \_ 以及 gl \_ 圖元 \_ 地圖 \_ i \_ 至 \_ \_ Alpha 地圖的大小。 從對應取得的所有元件都會壓制至範圍 \[ 0、1 \] 。 四個對應的內容是以 **glPixelMap** 指定的。<br/> |
| 深度       | 每個深度值乘以 GL \_ 深度 \_ 比例、新增至 GL \_ 深度 \_ 偏差，然後壓制至範圍 \[ 0，1 \] 。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| 樣板     | 每個索引都會改 \_ 為將 GL 索引 \_ 移位位移位，如同色彩索引為，然後新增至 GL \_ 索引 \_ 位移。 如果 GL \_ 對應樣板 \_ 為 true，則每個索引都會由 2n 1 遮罩，其中 *n* 是 gl \_ 圖元 \_ 地圖 \_ s \_ 到 \_ s \_ 大小，然後 \_ \_ \_ \_ 以 \_ 由遮罩值所編制索引之 gl 圖元地圖的內容取代。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

[**GlPixelTransferf**](glpixeltransfer.md)函式可以用來設定任何圖元傳輸參數。 如果參數類型為布林值，0.0 表示 false，而任何其他值則表示 true。 如果 *pname* 是整數參數，則會將 *param* 四捨五入至最接近的整數。

同樣地， **glPixelTransferi** 也可以用來設定任何圖元傳輸參數。 如果 *param* 為0，則布林參數設定為 false，否則為 true。 *Param* 參數在指派給實值參數之前，會先轉換成浮點數。

如果 [ [**glDrawPixels**](gldrawpixels.md)]、[ [**glReadPixels**](glreadpixels.md)]、[ [**glCopyPixels**](glcopypixels.md)]、[ [**glTexImage1D**](glteximage1d.md)] 或 [ [**glTexImage2D**](glteximage2d.md) ] 命令都放在顯示清單中 (請參閱 [**glNewList**](glnewlist.md) 和 [**glCallList**](glcalllist.md)) ， *執行* 顯示清單時生效的圖元傳輸模式設定就是所使用的值。 當命令編譯到顯示清單中時，它們可能會與設定不同。

下列函式會取出與 **glPixelTransfer** 相關的資訊：

[](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)具有引數 GL \_ 對應 \_ 色彩的 glGet

具有引數 GL 對應樣板的 **glGet** \_ \_

具有引數 GL \_ 索引 \_ 移位的 glGet

具有引數 GL \_ 索引 \_ 位移的 glGet

具有引數 GL \_ RED \_ SCALE 的 glGet

具有引數 GL \_ 紅色 \_ 偏差的 glGet

具有引數 GL \_ 綠 \_ 級的 glGet

**glGet** 與引數 GL \_ 綠色 \_ 偏差

具有引數 GL \_ BLUE \_ SCALE 的 glGet

**glGet** 與引數 GL \_ 藍色 \_ 偏差

具有引數 GL \_ ALPHA \_ 刻度的 glGet

**glGet** 與引數 GL \_ ALPHA \_ 偏差

具有引數 GL \_ 深度 \_ 比例的 glGet

具有引數 GL \_ 深度 \_ 偏差的 glGet

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Gl</dt> </dl>         |
| 程式庫<br/>                  | <dl> <dt>Opengl32 .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glNewList**](glnewlist.md)
</dt> <dt>

[**glPixelMap**](glpixelmap.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelZoom**](glpixelzoom.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





