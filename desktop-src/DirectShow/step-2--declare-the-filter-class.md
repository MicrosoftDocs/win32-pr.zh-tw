---
description: 宣告 c + + 類別，此類別會繼承您在撰寫轉換篩選時所選擇的基類。
ms.assetid: 74fbfc16-541f-4f80-a72f-26b67dc09a93
title: 步驟 2： 宣告篩選類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88be97e47d529ffa22c90e9c8c200160dbd5f261
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410061"
---
# <a name="step-2-declare-the-filter-class"></a>步驟 2： 宣告篩選類別

這是 [撰寫轉換篩選](writing-transform-filters.md)之教學課程的步驟2。

從宣告繼承基類的 c + + 類別開始：


```C++
class CRleFilter : public CTransformFilter
{
    /* Declarations will go here. */
};
```



每個篩選準則類別都有相關聯的釘選類別。 視篩選準則的特定需求而定，您可能需要覆寫釘選類別。 在 **CTransformFilter** 的情況下，釘選將大部分的工作委派給篩選器，因此您可能不需要覆寫 pin。

您必須為篩選產生唯一的 CLSID。 您可以使用 Guidgen 或 Uuidgen.exe 公用程式;絕對不要複製現有的 GUID。 有幾種方式可以宣告 CLSID。 下列範例會使用 **定義 \_ GUID** 宏：


```C++
[RleFilt.h]
// {1915C5C7-02AA-415f-890F-76D94C85AAF1}
DEFINE_GUID(CLSID_RLEFilter, 
0x1915c5c7, 0x2aa, 0x415f, 0x89, 0xf, 0x76, 0xd9, 0x4c, 0x85, 0xaa, 0xf1);

[RleFilt.cpp]
#include <initguid.h>
#include "RleFilt.h"
```



接下來，撰寫篩選準則的函式方法：


```C++
CRleFilter::CRleFilter()
  : CTransformFilter(NAME("My RLE Encoder"), 0, CLSID_RLEFilter)
{ 
   /* Initialize any private variables here. */
}
```



請注意， [**CTransformFilter**](ctransformfilter-ctransformfilter.md) 函式的其中一個參數是稍早定義的 CLSID。

下一 [步：步驟3。支援媒體類型的協商](step-3--support-media-type-negotiation.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[撰寫 DirectShow 篩選器](writing-directshow-filters.md)
</dt> </dl>

 

 



