---
title: 大型整數函數
description: 下列函式會與大型整數一起使用。
ms.assetid: f34932f4-b126-4d6c-a2f0-3ad706fd5629
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aebb5bd8c3edc35098dcf1bb232d858a9c6638d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021591"
---
# <a name="large-integer-functions"></a>大型整數函數

下列函式會與大型整數一起使用。

## <a name="in-this-section"></a>本節內容



| 函式                                                                    | 描述                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Int32x32To64**](/windows/desktop/api/Winnt/nf-winnt-int32x32to64)<br/>                             | 將兩個帶正負號的32位整數相乘，並傳回帶正負號的64位整數結果。<br/>                                                                                                                   |
| [**Int64ShllMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shllmod32)<br/>                         | 針對不帶正負號的64位整數值執行左邏輯移位運算。 此函式會針對左邏輯移位提供改良的移動程式碼，其中的移位元數目位於0-31 範圍內。<br/>      |
| [**Int64ShraMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shramod32)<br/>                         | 對帶正負號的64位整數值執行右算術移位運算。 此函式會針對移位元數目在0-31 範圍內的右算術移位，提供改良的移位程式碼。<br/> |
| [**Int64ShrlMod32**](/windows/desktop/api/Winnt/nf-winnt-int64shrlmod32)<br/>                         | 針對不帶正負號的64位整數值執行右邏輯移位運算。 此函式會針對右移計數在0-31 範圍內的右邏輯移位，提供改良的移位程式碼。<br/>    |
| [**MulDiv**](/windows/desktop/api/Winbase/nf-winbase-muldiv)<br/>                                         | 將 2 32 位值相乘，然後將64位結果除以第三個32位值。<br/>                                                                                                           |
| [**Multiply128**](/windows/desktop/api/Winnt/nf-winnt-multiply128)<br/>                               | 將 2 64 位整數相乘，以產生128位整數。<br/>                                                                                                                                       |
| [**MultiplyExtract128**](/windows/desktop/api/Winnt/nf-winnt-multiplyextract128)<br/>                 | 將 2 64 位整數乘以以產生128位整數，並將產品向右移動指定的位數，並傳回結果的低64位。<br/>                           |
| [**MultiplyHigh**](/windows/desktop/api/Winnt/nf-winnt-multiplyhigh)<br/>                             | 將 2 64 位整數相乘以產生128位整數，並取得高64位。<br/>                                                                                                             |
| [**PopulationCount64**](/windows/desktop/api/Winnt/nf-winnt-populationcount64)<br/>                   | 計算在64位不帶正負號整數中)  (人口計數的一個位數。<br/>                                                                                                                     |
| [**ShiftLeft128**](/windows/desktop/api/winnt/nf-winnt-shiftleft128)<br/>                             | 向左移位128位。<br/>                                                                                                                                                                               |
| [**ShiftRight128**](/windows/desktop/api/winnt/nf-winnt-shiftright128)<br/>                           | 向右移位128位。<br/>                                                                                                                                                                              |
| [**UInt32x32To64**](/windows/desktop/api/Winnt/nf-winnt-uint32x32to64)<br/>                           | 將兩個不帶正負號的32位整數相乘，並傳回不帶正負號的64位整數結果。<br/>                                                                                                              |
| [**UnsignedMultiply128**](/windows/desktop/api/Winnt/nf-winnt-unsignedmultiply128)<br/>               | 將兩個不帶正負號的64位整數相乘，以產生不帶正負號的128位整數。<br/>                                                                                                                    |
| [**UnsignedMultiplyExtract128**](/windows/desktop/api/Winnt/nf-winnt-unsignedmultiplyextract128)<br/> | 將兩個不帶正負號的64位整數相乘以產生不帶正負號的128位整數，並將產品向右移動指定的位數，並傳回結果的低64位。<br/>        |
| [**UnsignedMulitplyHigh**](/windows/desktop/api/Winnt/nf-winnt-unsignedmultiplyhigh)<br/>             | 將 2 64 位整數相乘以產生128位整數，並取得高不帶正負號的64位。<br/>                                                                                                    |



 

 

 





