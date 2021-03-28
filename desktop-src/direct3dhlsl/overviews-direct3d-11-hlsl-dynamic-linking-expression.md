---
title: 介面使用限制
description: 目前的 GPU 硬體在著色器執行時間不支援不同的位置資訊。 因為結果介面參考無法在條件運算式內修改，例如 if 或 switch 語句。
ms.assetid: 95a505d8-3ec4-49b7-bb2b-f29a655e4225
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8825d192dcb874ce8b148c4ade5c579a55857311
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300560"
---
# <a name="interface-usage-restrictions"></a>介面使用限制

目前的 GPU 硬體在著色器執行時間不支援不同的位置資訊。 因為結果介面參考無法在條件運算式內修改，例如 if 或 switch 語句。

下列著色器程式碼說明何時會發生這項限制，以及可能的替代方法。

假設有下列介面聲明：


```
interface A
{
    float GetRatio();
    bool IsGood();
};

interface B
{
    float GetValue();
};

A arrayA[6];
B arrayB[6];
```



假設有下列類別宣告：


```
class C1 : A
{
    float var;
    float GetRatio() { return 1.0f; }
    bool IsGood() { return true; }
};

class C2 : C1, B
{
    float GetRatio() { return C1::GetRatio() * 0.33f; }
    float GetValue() { return 5.0f; }
    bool IsGood() { return false; }
};

class C3 : B
{
    float var;
    float GetValue() { return -1.0f; }
};

class C4 : A, B
{
    float var;
    float GetRatio() { return var; }
    float GetValue() { return var * 2.0f; }
    bool IsGood() { return var > 0.0f; }
};
```



介面參考無法在條件運算式內修改 (if 語句) ：


```
float main() : wicked
{
    float rev;
    {
        A a = arrayA[0];
        for( uint i = 0; i < 6; ++i )
        {
            if( arrayA[i].IsGood() )
            {
                // This forces the loop to be unrolled, 
                // since the slot information is changing.
                a = arrayA[i]; 
                rev -= arrayA[i-2].GetRatio();
            }
            else
            {
                // This causes an error since the compiler is
                // unable to determine the interface slot
                rev += arrayB[i].GetValue() + a.GetRatio(); 
            }
        }
    }
    return rev;
}
```



如果有相同的介面和類別宣告，您可以使用索引來提供相同的功能，並避免強制迴圈展開。


```
float main() : wicked
{
    float rev;
    {
        uint index = 0;
        for( uint i = 0; i < 6; ++i )
        {
            if( arrayA[i].IsGood() )
            {
                index = i;
                rev -= arrayA[i-2].GetRatio();
            }
            else
            {
                rev += arrayB[i].GetValue() + arrayA[index].GetRatio();
            }
        }
    }
    return rev;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[動態連結](overviews-direct3d-11-hlsl-dynamic-linking.md)
</dt> </dl>

 

 




