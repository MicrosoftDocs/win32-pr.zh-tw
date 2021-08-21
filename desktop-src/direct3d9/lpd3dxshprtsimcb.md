---
description: 預先計算 Radiance 傳輸 (的回呼函式 PRT) 模擬和壓縮。
ms.assetid: 1d7e2149-d2ca-47da-be1f-8273fd9bd30a
title: LPD3DXSHPRTSIMCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c81e510808dd2e14af1de0d9618591d8ea3b8587bb4015e72a3e01fa33157b5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118799331"
---
# <a name="lpd3dxshprtsimcb"></a>LPD3DXSHPRTSIMCB

預先計算 Radiance 傳輸 (的回呼函式 PRT) 模擬和壓縮。

## <a name="syntax"></a>語法


```
typedef HRESULT (WINAPI *LPD3DXSHPRTSIMCB)(
    FLOAT fPercentDone,
    LPVOID lpUserContext
);
```



## <a name="parameters"></a>參數

fPercentDone-介於0和1.0 之間的浮點數，代表已完成的計算百分比 (介於0到 100%) 之間。

lpUserCoNtext-傳遞給回呼函式的使用者定義值指標;通常由應用程式用來傳遞資料結構的指標，以提供回呼函數的內容資訊。

## <a name="return-value"></a>傳回值

必須實作為此函式，才能 \_ 讓執行模擬器的正常運作。 任何其他值都會終止模擬器。

## <a name="remarks"></a>備註

宣告回呼函數時，請務必指定 [**Windows 資料類型**](../winprog/windows-data-types.md)呼叫慣例。 否則，可能會發生堆疊溢位。



| 需求                         | 值            |
|--------------------------|-------------|
| 標頭                   | d3dx9mesh。h |
| 匯入程式庫           | d3dx9 .lib   |
| 最低作業系統 | Windows 98  |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[回呼函式](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
