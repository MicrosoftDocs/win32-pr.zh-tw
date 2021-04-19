---
description: UVAtlas 的回呼函數。
ms.assetid: a605ae27-10c9-49b4-98fe-8c788c2c0752
title: LPD3DXU加值稅LASCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbda7c58ef001a936b01f3af2027f9207c3d2770
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970892"
---
# <a name="lpd3dxuvatlascb"></a>LPD3DXU加值稅LASCB

UVAtlas 的回呼函數。

## <a name="syntax"></a>語法


```
typedef HRESULT (*LPD3DXUVATLASCB ( 
    FLOAT fPercentDone,
    LPVOID lpUserContext
);
```



## <a name="parameters"></a>參數

\[out \] fPercentDone-介於0和1.0 之間的浮點數，代表已完成的計算百分比 (介於0到 100%) 之間。

\[在 lpUserCoNtext 中，指向 \] 傳遞給回呼函式的使用者定義值的指標; 通常由應用程式用來傳遞資料結構的指標，該結構會提供回呼函數的內容資訊。

## <a name="return-value"></a>傳回值

必須實作為此函式，才能 \_ 讓執行模擬器的正常運作。 任何其他值都會終止模擬器。

## <a name="remarks"></a>備註

宣告回呼函數時，請務必指定 [**Windows 資料類型**](../winprog/windows-data-types.md) 呼叫慣例。 否則，可能會發生堆疊溢位。



|                          |             |
|--------------------------|-------------|
| 標頭                   | d3dx9mesh。h |
| 匯入程式庫           | d3dx9 .lib   |
| 最低作業系統 | Windows 98  |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[回呼函式](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
