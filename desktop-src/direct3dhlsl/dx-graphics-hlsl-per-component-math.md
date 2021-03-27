---
title: Per-Component 數學運算
description: 透過 HLSL，您可以在演算法層級編寫著色器。
ms.assetid: a919df50-2d13-489d-9011-1137c997e121
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5ff30cd19b7821c9a059251e105f6acfa9cf961e
ms.sourcegitcommit: fa5c081bf792b119a7bb92182cde1f85ca75967b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/17/2021
ms.locfileid: "104974781"
---
# <a name="per-component-math-operations"></a>Per-Component 數學運算

透過 HLSL，您可以在演算法層級編寫著色器。 若要瞭解語言，您必須知道如何宣告變數和函式、使用內建函式、定義自訂資料類型，以及使用語義將著色器引數連接至其他著色器和管線。

一旦您瞭解如何在 HLSL 中撰寫著色器，您將需要瞭解 API 呼叫，以便您可以：編譯特定硬體的著色器、初始化著色器常數，以及視需要初始化其他管線狀態。

-   [向量類型](#the-vector-type)
-   [矩陣類型](#the-matrix-type)
    -   [矩陣順序](#matrix-ordering)
-   [範例](#examples)
-   [相關主題](#related-topics)

## <a name="the-vector-type"></a>向量類型

Vector 是包含一到四個元件的資料結構。


```
bool    bVector;   // scalar containing 1 Boolean
bool1   bVector;   // vector containing 1 Boolean
int1    iVector;   // vector containing 1 int
float3  fVector;   // vector containing 3 floats
double4 dVector;   // vector containing 4 doubles
```



緊接在資料類型後面的整數是向量上的元件數目。

初始化運算式也可以包含在宣告中。


```
bool    bVector = false;
int1    iVector = 1;
float3  fVector = { 0.2f, 0.3f, 0.4f };
double4 dVector = { 0.2, 0.3, 0.4, 0.5 };
```



或者，向量類型可以用來建立相同的宣告：


```
vector <bool,   1> bVector = false;
vector <int,    1> iVector = 1;
vector <float,  3> fVector = { 0.2f, 0.3f, 0.4f };
vector <double, 4> dVector = { 0.2, 0.3, 0.4, 0.5 };
```



向量類型會使用角括弧來指定元件的類型和數目。

向量最多包含四個元件，每個元件都可以使用兩個命名集的其中一個來存取：

-   設定的位置： x、y、z、w
-   色彩設定： r、g、b、a

這些語句都會傳回第三個元件的值。


```
// Given
float4 pos = float4(0,0,2,1);

pos.z    // value is 2
pos.b    // value is 2
```



命名集可以使用一或多個元件，但不能混用。


```
// Given
float4 pos = float4(0,0,2,1);
float2 temp;

temp = pos.xy  // valid
temp = pos.rg  // valid

temp = pos.xg  // NOT VALID because the position and color sets were used.
```



在讀取元件時指定一或多個向量元件，稱為 swizzling。 例如：


```
float4 pos = float4(0,0,2,1);
float2 f_2D;
f_2D = pos.xy;   // read two components 
f_2D = pos.xz;   // read components in any order       
f_2D = pos.zx;

f_2D = pos.xx;   // components can be read more than once
f_2D = pos.yy;
```



遮罩會控制寫入的元件數目。


```
float4 pos = float4(0,0,2,1);
float4 f_4D;
f_4D    = pos;     // write four components          

f_4D.xz = pos.xz;  // write two components        
f_4D.zx = pos.xz;  // change the write order

f_4D.xzyw = pos.w; // write one component to more than one component
f_4D.wzyx = pos;
```



無法將指派寫入相同的元件一次以上。 因此，此語句的左邊無效：


```
f_4D.xx = pos.xy;   // cannot write to the same destination components 
```



此外，元件命名空間也不能混用。 這是不正確元件寫入：


```
f_4D.xg = pos.rgrg;    // invalid write: cannot mix component name spaces 
```



將向量當作純量存取會存取向量的第一個元件。 下列兩個語句是相等的。


```
f_4D.a = pos * 5.0f;
f_4D.a = pos.r * 5.0f;
```



## <a name="the-matrix-type"></a>矩陣類型

矩陣是包含資料列和資料行的資料結構。 資料可以是任何純量資料類型，不過，矩陣的每個元素都是相同的資料類型。 資料列和資料行的數目是使用附加至資料類型的逐資料行字串來指定。


```
int1x1    iMatrix;   // integer matrix with 1 row,  1 column
int2x1    iMatrix;   // integer matrix with 2 rows, 1 column
...
int4x1    iMatrix;   // integer matrix with 4 rows, 1 column
...
int1x4    iMatrix;   // integer matrix with 1 row, 4 columns
double1x1 dMatrix;   // double matrix with 1 row,  1 column
double2x2 dMatrix;   // double matrix with 2 rows, 2 columns
double3x3 dMatrix;   // double matrix with 3 rows, 3 columns
double4x4 dMatrix;   // double matrix with 4 rows, 4 columns
```



資料列或資料行的最大數目為 4;最小值為1。

在宣告矩陣時，可以將它初始化：


```
float2x2 fMatrix = { 0.0f, 0.1, // row 1
                     2.1f, 2.2f // row 2
                   };   
```



或者，矩陣類型可以用來建立相同的宣告：


```
matrix <float, 2, 2> fMatrix = { 0.0f, 0.1, // row 1
                                 2.1f, 2.2f // row 2
                               };
```



矩陣類型會使用角括弧來指定類型、資料列數目和資料行數目。 這個範例會建立具有兩個數據列和兩個數據行的浮點數矩陣。 您可以使用任何純量資料類型。

這個宣告會定義浮點數的矩陣 (32 位浮點數) 有兩個數據列和三個數據行：


```
matrix <float, 2, 3> fFloatMatrix;
```



矩陣包含以資料列和資料行組織的值，可使用結構運算子 "." 來存取，後面接著兩個命名集的其中一個：

-   以零為基礎的資料列資料行位置：
    -   \_m00、 \_ m01、 \_ m02、 \_ m03
    -   \_m10、 \_ m11、 \_ m12、 \_ m13
    -   \_m20、 \_ m21、 \_ m22、 \_ m23
    -   \_m30、 \_ m31、 \_ m32、 \_ m33
-   以一為基礎的資料列資料行位置：
    -   \_11、 \_ 12、 \_ 13、 \_ 14
    -   \_21、 \_ 22、 \_ 23、 \_ 24
    -   \_31、 \_ 32、 \_ 33、 \_ 34
    -   \_41、 \_ 42、 \_ 43、 \_ 44

每個命名集的開頭都是底線，後面接著資料列編號和資料行編號。 以零為基底的慣例也會在資料列和資料行編號之前包含字母 "m"。 以下是使用兩個命名集來存取矩陣的範例：


```
// given
float2x2 fMatrix = { 1.0f, 1.1f, // row 1
                     2.0f, 2.1f  // row 2
                   }; 

float f_1D;
f_1D = matrix._m00; // read the value in row 1, column 1: 1.0
f_1D = matrix._m11; // read the value in row 2, column 2: 2.1

f_1D = matrix._11;  // read the value in row 1, column 1: 1.0
f_1D = matrix._22;  // read the value in row 2, column 2: 2.1
```



就像向量一樣，命名集可以使用命名集的一或多個元件。


```
// Given
float2x2 fMatrix = { 1.0f, 1.1f, // row 1
                     2.0f, 2.1f  // row 2
                   };
float2 temp;

temp = fMatrix._m00_m11 // valid
temp = fMatrix._m11_m00 // valid
temp = fMatrix._11_22   // valid
temp = fMatrix._22_11   // valid
```



您也可以使用陣列存取標記法來存取矩陣，這是以零為基礎的索引集合。 每個索引都在方括弧內。 使用下列索引來存取4x4 矩陣：

-   \[0 \] \[ 0 \] 、 \[ 0 \] \[ 1 \] 、 \[ 0 \] \[ 2 \] 、 \[ 0 \] \[ 3\]
-   \[1 \] \[ 0 \] ， \[ 1 \] \[ 1 \] ， \[ 1 \] \[ 2 \] ， \[ 1 \] \[ 3\]
-   \[2 \] \[ 0 \] 、 \[ 2 \] \[ 1 \] 、 \[ 2 \] \[ 2 \] 、 \[ 2 \] \[ 3\]
-   \[3 \] \[ 0 \] 、 \[ 3 \] \[ 1 \] 、 \[ 3 \] \[ 2 \] 、 \[ 3 \] \[ 3\]

以下是存取矩陣的範例：


```
float2x2 fMatrix = { 1.0f, 1.1f, // row 1
                     2.0f, 2.1f  // row 2
                   };
float temp;

temp = fMatrix[0][0] // single component read
temp = fMatrix[0][1] // single component read
```



請注意，不會使用結構運算子 "." 來存取陣列。 陣列存取標記法不能使用 swizzling 來讀取一個以上的元件。


```
float2 temp;
temp = fMatrix[0][0]_[0][1] // invalid, cannot read two components
```



不過，陣列存取可以讀取多元件向量。


```
float2 temp;
float2x2 fMatrix;
temp = fMatrix[0] // read the first row
```



如同向量，讀取一個以上的矩陣元件稱為 swizzling。 只要使用一個命名空間，就可以指派一個以上的元件。 這些都是有效的指派：


```
// Given these variables
float4x4 worldMatrix = float4( {0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} );
float4x4 tempMatrix;

tempMatrix._m00_m11 = worldMatrix._m00_m11; // multiple components
tempMatrix._m00_m11 = worldMatrix.m13_m23;

tempMatrix._11_22_33 = worldMatrix._11_22_33; // any order on swizzles
tempMatrix._11_22_33 = worldMatrix._24_23_22;
```



遮罩會控制寫入的元件數目。


```
// Given
float4x4 worldMatrix = float4( {0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} );
float4x4 tempMatrix;

tempMatrix._m00_m11 = worldMatrix._m00_m11; // write two components
tempMatrix._m23_m00 = worldMatrix._m00_m11;
```



無法將指派寫入相同的元件一次以上。 因此，此語句的左邊無效：


```
// cannot write to the same component more than once
tempMatrix._m00_m00 = worldMatrix._m00_m11;
```



此外，元件命名空間也不能混用。 這是不正確元件寫入：


```
// Invalid use of same component on left side
tempMatrix._11_m23 = worldMatrix._11_22; 
```



### <a name="matrix-ordering"></a>矩陣順序

統一參數的矩陣封裝順序預設會設定為 [資料行主要]。 這表示矩陣的每個資料行都會儲存在單一常數暫存器中。 另一方面，資料列主要矩陣會將矩陣的每個資料列封裝在單一常數暫存器中。 您可以使用 **\# pragmapack \_ 矩陣** 指示詞，或使用資料列 **\_ 主要** 關鍵字或資料行 **\_ 主要** 關鍵字來變更矩陣封裝。

在著色器執行之前，矩陣中的資料會載入著色器常數暫存器中。 如何讀取矩陣資料的選項有兩種：以資料列為主的順序或依資料行的順序。 資料行主要順序表示每個矩陣資料行都會儲存在單一常數暫存器中，而資料列主要順序表示矩陣的每個資料列都會儲存在單一常數暫存器中。 這是用於矩陣的常數暫存器數目的重要考慮。

資料列主要矩陣的配置方式如下所示：



|     |     |     |     |
|-----|-----|-----|-----|
| 11  | 12  | 13  | 14  |
| 21  | 22  | 23  | 24  |
| 31  | 32  | 33  | 34  |
| 41  | 42  | 43  | 44  |



 

資料行主要矩陣的配置方式如下所示：



|     |     |     |     |
|-----|-----|-----|-----|
| 11  | 21  | 31  | 41  |
| 12  | 22  | 32  | 42  |
| 13  | 23  | 33  | 43  |
| 14  | 24  | 34  | 44  |



 

資料列-主要和資料行主要矩陣順序：決定從著色器輸入讀取矩陣元件的順序。 一旦資料寫入常數暫存器中，矩陣順序就不會影響資料在著色器程式碼中的使用或存取方式。 此外，在著色器主體中宣告的矩陣不會封裝成常數暫存器。 資料列-主要和資料行主要封裝順序不會影響函式的封裝順序 (其一律遵循資料列主要順序) 。

矩陣中的資料順序可以在編譯時期宣告，或編譯器會在執行時間為數據排序，以獲得最有效率的使用方式。

## <a name="examples"></a>範例

HLSL 會使用兩種特殊類型：向量類型和矩陣類型，讓程式設計2D 和3D 圖形變得更容易。 其中每個類型都包含一個以上的元件;向量最多包含四個元件，而矩陣最多包含16個元件。 當向量和矩陣在標準 HLSL 方程式中使用時，所執行的數學會設計為每個元件的工作。 比方說，HLSL 會執行這個乘法：


```
float4 v = a*b;
```



四個元件的乘法。 結果為四個純量：


```
float4 v = a*b;

v.x = a.x*b.x;
v.y = a.y*b.y;
v.z = a.z*b.z;
v.w = a.w*b.w;
```



這是四個乘法運算，其中每個結果都會儲存在 v 的個別元件中。 這稱為四個元件的乘法。 HLSL 會使用元件數學，讓寫入著色器非常有效率。

這與通常實作為點乘積的乘法（會產生單一純量）非常不同：


```
v = a.x*b.x + a.y*b.y + a.z*b.z + a.w*b.w;
```



矩陣也會使用 HLSL 中的每個元件作業：


```
float3x3 mat1,mat2;
...
float3x3 mat3 = mat1*mat2;
```



結果會是兩個矩陣 (的每個元件乘，而不是標準3x3 矩陣乘以) 。 每個元件矩陣乘法會產生第一個詞彙：


```
mat3.m00 = mat1.m00 * mat2._m00;
```



這與會產生第一個詞彙的3x3 矩陣相乘不同：


```
// First component of a four-component matrix multiply
mat.m00 = mat1._m00 * mat2._m00 + 
          mat1._m01 * mat2._m10 + 
          mat1._m02 * mat2._m20 + 
          mat1._m03 * mat2._m30;
```



相乘內建函式的多載版本，其中一個運算元是向量，另一個運算元是矩陣。 例如：向量 \* 向量、向量 \* 矩陣、矩陣 \* 向量和矩陣 \* 矩陣。 例如：


```
float4x3 World;

float4 main(float4 pos : SV_POSITION) : SV_POSITION
{
    float4 val;
    val.xyz = mul(pos,World);
    val.w = 0;

    return val;
}   
```



產生相同的結果，如下所示：


```
float4x3 World;

float4 main(float4 pos : SV_POSITION) : SV_POSITION
{
    float4 val;
    val.xyz = (float3) mul((float1x4)pos,World);
    val.w = 0;

    return val;
}   
```



此範例會使用 (float1x4) 轉換，將 pos 向量轉換成資料行向量。 藉由轉型來變更向量，或將提供給乘法的引數的順序交換，相當於將矩陣轉置。

自動轉換轉換會導致乘法和 dot 內建函式傳回與此處所用相同的結果：


```
{
  float4 val;
  return mul(val,val);
}
```



相乘的結果是 \* 4x1 = 1x1 向量。 這相當於點乘積：


```
{
  float4 val;
  return dot(val,val);
}
```



傳回單一純量值的。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ (DirectX HLSL) 的資料類型 ](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 




