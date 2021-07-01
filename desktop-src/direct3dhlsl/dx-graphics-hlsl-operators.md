---
title: 操作員
description: 運算式是由運算子引起哈欠的變數和常值序列。
ms.assetid: c31aa0b8-1284-48aa-b000-d72433f0f5cc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d7a44fe02983038658247fedaec7122f09306548
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119603"
---
# <a name="operators"></a>運算子

運算式是由[運算子](dx-graphics-hlsl-statement-blocks.md)引起哈欠的[變數](dx-graphics-hlsl-variable-syntax.md)和常值序列。 運算子決定變數和常值如何合併、比較、選取等等。 這些運算子包括：



| 操作員名稱                                                                                | 運算子                                                                   |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [加法和乘法運算子](#additive-and-multiplicative-operators) | +, -, \*, /, %                                                     |
| [陣列運算子](#array-operator)                                               | \[i\]                                                              |
| [指派運算子](#assignment-operators)                                   | =, +=, -=, \*=, /=, %=                                             |
| [二進位轉換](#binary-casts)                                                   | 適用于 float 和 int 的 c 規則、適用于 bool 的 C 規則或 HLSL 內建函式     |
| [位元運算子](#bitwise-operators)                                         | ~、 <<、 >>、&、 \| 、^、 <<=、 >>=、&=、 \| =、^ = |
| [布耳運算運算子](#boolean-math-operators)                               | & &、 \| \| 、？：                                                      |
| [轉換運算子](#cast-operator)                                                 |  (類型)                                                              |
| [逗點運算子](#comma-operator)                                               | ,                                                                  |
| [比較運算子](#comparison-operators)                                   | <、>、= =、！ =、<=、>=                                   |
| [前置或後置運算子](#prefix-or-postfix-operators)                     | ++, --                                                             |
| [Structure 運算子](#structure-operator)                                       | .                                                                  |
| [一元運算子](#unary-operators)                                             | !, -, +                                                            |



 

許多運算子都是每個元件，這表示會針對每個變數的每個元件獨立執行作業。 例如，單一元件變數已執行一項作業。 另一方面，四個元件的變數有四個執行的作業，每個元件各一個。

對值執行某些動作的所有運算子（例如 + 和 \* ）都會依元件運作。

除非您使用 [**all**](dx-graphics-hlsl-all.md) 或 [**any**](dx-graphics-hlsl-any.md) 內建函式搭配多重元件變數，否則比較運算子需要單一元件才能運作。 下列作業會失敗，因為 if 語句需要單一 bool，但卻收到 bool4：


```
if (A4 < B4)
```



下列作業會成功：


```
if ( any(A4 < B4) )
if ( all(A4 < B4) )
```



二元轉換運算子會針對每個元件 [**asfloat**](dx-graphics-hlsl-asfloat.md)、 [**asint**](dx-graphics-hlsl-asint.md)等工作，但會記載其特殊規則的 [**asdouble**](asdouble.md) 除外。

點、逗號和陣列括弧等選取運算子無法針對每個元件運作。

轉換運算子會變更元件的數目。 下列轉換作業顯示其相等：


```
(float) i4 ->   float(i4.x)
(float4)i ->   float4(i, i, i, i)
```



## <a name="additive-and-multiplicative-operators"></a>加法和乘法運算子

加法和乘法運算子為： +、-、 \* 、/、%


```
int i1 = 1;
int i2 = 2;
int i3 = i1 + i2;  // i3 = 3
i3 = i1 * i2;        // i3 = 1 * 2 = 2
```




```
i3 = i1/i2;       // i3 = 1/3 = 0.333. Truncated to 0 because i3 is an integer.
i3 = i2/i1;       // i3 = 2/1 = 2
```




```
float f1 = 1.0;
float f2 = 2.0f;
float f3 = f1 - f2; // f3 = 1.0 - 2.0 = -1.0
f3 = f1 * f2;         // f3 = 1.0 * 2.0 = 2.0
```




```
f3 = f1/f2;        // f3 = 1.0/2.0 = 0.5
f3 = f2/f1;        // f3 = 2.0/1.0 = 2.0
```



模數運算子會傳回除法的餘數。 使用整數和浮點數時，會產生不同的結果。 小數的整數餘數將會被截斷。


```
int i1 = 1;
int i2 = 2;
i3 = i1 % i2;      // i3 = remainder of 1/2, which is 1
i3 = i2 % i1;      // i3 = remainder of 2/1, which is 0
i3 = 5 % 2;        // i3 = remainder of 5/2, which is 1
i3 = 9 % 2;        // i3 = remainder of 9/2, which is 1
```



使用整數時，模數運算子會截斷小數餘數。


```
f3 = f1 % f2;      // f3 = remainder of 1.0/2.0, which is 0.5
f3 = f2 % f1;      // f3 = remainder of 2.0/1.0, which is 0.0
```



只有當兩個邊都是正數或兩邊都是負數時，才會定義% 運算子。 與 C 不同的是，它也會針對浮點數資料類型以及整數來運作。

## <a name="array-operator"></a>陣列運算子

陣列成員選取運算子 " \[ i \] " 選取陣列中的一或多個元件。 它是一組包含以零為基底之索引的方括弧。


```
int arrayOfInts[4] = { 0,1,2,3 };
arrayOfInts[0] = 2;
arrayOfInts[1] = arrayOfInts[0];
```



Array 運算子也可以用來存取 vector。


```
float4 4D_Vector = { 0.0f, 1.0f, 2.0f, 3.0f  };         
float 1DFloat = 4D_Vector[1];          // 1.0f
```



藉由加入額外的索引，陣列運算子也可以存取矩陣。


```
float4x4 mat4x4 = {{0,0,0,0}, {1,1,1,1}, {2,2,2,2}, {3,3,3,3} };
mat4x4[0][1] = 1.1f;
float 1DFloat = mat4x4[0][1];      // 0.0f
```



第一個索引是以零為基礎的資料列索引。 第二個索引是以零為基底的資料行索引。

## <a name="assignment-operators"></a>指派運算子

指派運算子為： =、+ =、-=、 \* =、/=

變數可以指派常值：


```
int i = 1;            
float f2 = 3.1f; 
bool b = false;
string str = "string";
```



您也可以將數學運算的結果指派給變數：


```
int i1 = 1;
i1 += 2;           // i1 = 1 + 2 = 3
```



變數可以在等號的任一邊使用：


```
float f3 = 0.5f;
f3 *= f3;          // f3 = 0.5 * 0.5 = 0.25
```



浮點數變數的除法是預期的，因為 decimal 餘數不是問題。


```
float f1 = 1.0;
f1 /= 3.0f;        // f1 = 1.0/3.0 = 0.333
```



如果您使用的整數可能會被整除，特別是當截斷影響結果時，請務必小心。 這個範例與上一個範例相同，但資料類型除外。 截斷會產生非常不同的結果。


```
int i1 = 1;
i1 /= 3;           // i1 = 1/3 = 0.333, which gets truncated to 0
```



## <a name="binary-casts"></a>二進位轉換

Int 和 float 之間的轉換運算會將數值轉換成 C 規則之後的適當標記法，以截斷 int 型別。 將值從 float 轉換成 int，再轉換回浮點數，將會根據目標的有效位數來產生失真轉換。

二進位轉換也可以使用 [**內建函式 (DIRECTX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)來執行，這會將數位的位標記法重新解譯到目標資料類型。


```
asfloat() // Cast to float
asint()   // Cast to int 
asuint()  // Cast to uint
```



## <a name="bitwise-operators"></a>位元運算子

HLSL 支援下列位運算子，其遵循與 C 相關的優先順序，與其他運算子有關。 下表描述這些運算子。

> [!Note]  
> 位運算子需要具有 Direct3D 10 和更高硬體的 [著色器模型 4 \_ 0](dx-graphics-hlsl-sm4.md) 。

 



| 運算子          |  函式                 |
|-----------|-------------------|
| ~         | 邏輯 Not       |
| <<  | 左移        |
| >>  | 右移       |
| &         | 邏輯 And       |
| \|        | 邏輯 Or        |
| ^         | 邏輯 Xor       |
| <<= | 左移等於  |
| >>= | 右 Shift 等於 |
| &=        | 和相等         |
| \|=       | 或等於          |
| ^=        | Xor 等於         |



 

位運算子定義為只在 int 和 uint 資料類型上運作。 嘗試在 float 或 struct 資料類型上使用位運算子將會產生錯誤。

## <a name="boolean-math-operators"></a>布耳運算運算子

布林數學運算子為：  &&、 \| \| 、？：


```
bool b1 = true;
bool b2 = false;
bool b3 = b1 && b2 // b3 = true AND false = false
b3 = b1 || b2                // b3 = true OR false = true
```



與 C 的 &&、和？：的短路評估不同的 \| \| 是，HLSL 運算式永遠不會將評估短路，因為它們是向量作業。 一律會評估運算式的所有兩側。

布林運算子會以每個元件為基礎運作。 這表示，如果您比較兩個向量，則結果會是包含每個元件比較之布林結果的向量。

針對使用布林運算子的運算式，每個變數的大小和元件類型都會在作業發生之前升級為相同的。 升級型別會決定作業的解決方式，以及運算式的結果型別。 例如，int3 + float 運算式會升級為 float3 + float3 進行評估，而其結果會是 float3 類型。

## <a name="cast-operator"></a>轉換運算子

前面加上括弧中類型名稱的運算式是明確的類型轉換。 類型轉換會將原始運算式轉換成轉換的資料類型。 一般情況下，單一資料型別可以轉換成更複雜的資料類型 (有提升轉換) ，但是只有一些複雜的資料類型可以轉換成簡單的資料類型 (並) 降級轉換。

只有右手邊型別轉換是合法的。 例如，的運算式 `(int)myFloat = myInt;` 不合法。 請改用 `myFloat = (float)myInt;`。

編譯器也會執行隱含類型轉換。 例如，下列兩個運算式是相等的：


```
int2 b = int2(1,2) + 2;
int2 b = int2(1,2) + int2(2,2);
```



## <a name="comma-operator"></a>逗點運算子

逗號運算子 (，) 分隔一或多個要依順序評估的運算式。 順序中最後一個運算式的值會用來做為序列的值。

以下是值得注意的一個案例。 如果不小心將 [函式類型] 保留在等號右邊，右邊就會包含四個運算式，並以三個逗號分隔。


```
// Instead of using a constructor
float4 x = float4(0,0,0,1); 

// The type on the right side is accidentally left off
float4 x = (0,0,0,1); 
```



逗號運算子會從左至右評估運算式。 這樣可以減少右手邊：


```
float4 x = 1; 
```



在此情況下，HLSL 會使用純量升階，因此其結果就像撰寫如下所示：


```
float4 x = float4(1,1,1,1);
```



在此情況下，從右邊離開 float4 類型可能會造成編譯器無法偵測到的錯誤，因為這是有效的語句。

## <a name="comparison-operators"></a>比較運算子

比較運算子為： <、>、= =、！ =、<=、>=。

比較大於 (或小於) 任何純量值的值：


```
if( dot(lightDirection, normalVector) > 0 )
   // Do something; the face is lit
```




```
if( dot(lightDirection, normalVector) < 0 )
   // Do nothing; the face is backwards
```



或者，比較等於 (或不等於) 任何純量值的值：


```
if(color.a == 0)
   // Skip processing because the face is invisible

if(color.a != 0)
   // Blend two colors together using the alpha value
```



或結合和比較大於或等於 (或小於或等於) 任何純量值的值：


```
if( position.z >= oldPosition.z )
   // Skip the new face because it is behind the existing face
```




```
if( currentValue <= someInitialCondition )
   // Reset the current value to its initial condition
```



您可以使用任何純量資料類型來完成這些比較。

若要搭配向量和矩陣類型使用比較運算子，請使用 [**all**](dx-graphics-hlsl-all.md) 或 [**any**](dx-graphics-hlsl-any.md) 內建函式。

因為 if 語句需要單一 bool 但收到 bool4，所以此作業會失敗：


```
if (A4 < B4)
```



這些作業會成功：


```
if ( any(A4 < B4) )
if ( all(A4 < B4) )
```



## <a name="prefix-or-postfix-operators"></a>前置或後置運算子

前置詞和後置運算子為： + +、--。 前置運算子會在評估運算式之前變更變數的內容。 後置運算子會在評估運算式之後變更變數的內容。

在此情況下，迴圈會使用我的內容來追蹤迴圈計數。


```
float4 arrayOfFloats[4] = { 1.0f, 2.0f, 3.0f, 4.4f };

for (int i = 0; i<4; )
{
    arrayOfFloats[i++] *= 2; 
}
```



因為使用後置遞增運算子 (+ +) ，所以在 \[ 遞增之前，arrayOfFloats i \] 乘以2。 這可能會稍微重新排列以使用前置遞增運算子。 雖然這兩個範例都相等，但這種情況很難閱讀。


```
float4 arrayOfFloats[4] = { 1.0f, 2.0f, 3.0f, 4.4f };

for (int i = 0; i<4; )
{
    arrayOfFloats[++i - 1] *= 2; 
}
```



因為使用前置運算子 (+ +) ，所以在 \[ 遞增之後，arrayOfFloats i + 1-1 \] 會乘以2。

前置遞減和後置遞減運算子 (--) 會以與遞增運算子相同的順序套用。 不同之處在于遞減減去1，而不是加1。

## <a name="structure-operator"></a>Structure 運算子

結構成員選取運算子 (。 ) 是句號。 指定此結構：


```
struct position
{
float4 x;
float4 y;
float4 z;
};
```



您可以如下所示讀取：


```
struct position pos = { 1,2,3 };

float 1D_Float = pos.x
1D_Float = pos.y
```



每個成員都可以使用 structure 運算子來讀取或寫入：


```
struct position pos = { 1,2,3 };
pos.x = 2.0f;
pos.z = 1.0f;       // z = 1.0f
pos.z = pos.x      // z = 2.0f
```



## <a name="unary-operators"></a>一元運算子

一元運算子為：!,-, +

一元運算子在單一運算元上運作。


```
bool b = false;
bool b2 = !b;      // b2 = true
int i = 2;
int i2 = -i;       // i2 = -2
int j = +i2;       // j = +2
```



## <a name="operator-precedence"></a>運算子優先順序

當運算式包含一個以上的運算子時，運算子優先順序會決定評估的順序。 HLSL 的運算子優先順序遵循與 C 相同的優先順序。

## <a name="remarks"></a>備註

大括弧 ({,}) 開始和結束語句區塊。 當語句區塊使用單一語句時，大括弧是選擇性的。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ (DirectX HLSL) 的語句 ](dx-graphics-hlsl-statements.md)
</dt> </dl>

 

 




