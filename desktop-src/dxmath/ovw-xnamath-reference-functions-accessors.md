---
description: 列出 DirectXMath 程式庫所提供的向量存取子函數。
ms.assetid: 6e7453b8-0dee-6fc5-cbac-fe20e4e3ef60
title: DirectXMath 程式庫向量存取子函式
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2107638a6ccd5805858b4c67b74c0811675f2492
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974578"
---
# <a name="directxmath-library-vector-accessor-functions"></a>DirectXMath 程式庫向量存取子函式

列出 DirectXMath 程式庫所提供的向量存取子函數。

DirectXMath 向量存取子可讓開發人員撰寫程式碼，以可移植且最佳的方式取得及設定向量的個別元件。

## <a name="in-this-section"></a>本節內容



| 主題                                                                   | 描述                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**XMVectorGetByIndex**](/previous-versions/windows/desktop/legacy/hh404786(v=vs.85))<br/>             | 取出 [**XMVECTOR 資料類型**](xmvector-data-type.md) 的四個元件的值，其中包含依索引的浮點數據。<br/>                                                                          |
| [**XMVectorGetByIndexPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetbyindexptr)<br/>       | 將移至指標所參考之浮點數的實例，這是 [**XMVECTOR 資料類型**](xmvector-data-type.md) 的四個元件的值，其中包含以索引參考的浮點數據。<br/> |
| [**XMVectorGetIntByIndex**](/previous-versions/windows/desktop/legacy/hh404788(v=vs.85))<br/>       | 取出 [**XMVECTOR 資料類型**](xmvector-data-type.md) 的四個元件的值，其中包含依索引的整數資料。<br/>                                                                                 |
| [**XMVectorGetIntByIndexPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetintbyindexptr)<br/> | 將傳回到指標所參考之整數的實例，這是 [**XMVECTOR 資料類型**](xmvector-data-type.md) 的四個元件的值，其中包含以索引為依據的整數資料。<br/>                          |
| [**XMVectorGetIntW**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetintw)<br/>                   | 取出 `w` [**XMVECTOR 資料類型**](xmvector-data-type.md)的元件。<br/>                                                                                                                                        |
| [**XMVectorGetIntWPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetintwptr)<br/>             | 抓取 `w` 包含整數資料的 [**XMVECTOR 資料類型**](xmvector-data-type.md) 元件，並將該元件的值儲存在指標所參考的 uint32 \_ t 實例中。<br/>                       |
| [**XMVectorGetIntX**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetintx)<br/>                   | 取出 `x` [**XMVECTOR 資料類型**](xmvector-data-type.md)的元件。<br/>                                                                                                                                        |
| [**XMVectorGetIntXPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetintxptr)<br/>             | 抓取 `x` 包含整數資料的 [**XMVECTOR 資料類型**](xmvector-data-type.md) 元件，並將該元件的值儲存在指標所參考的 uint32 \_ t 實例中。<br/>                       |
| [**XMVectorGetIntY**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetinty)<br/>                   | 取出 `y` [**XMVECTOR 資料類型**](xmvector-data-type.md)的元件。<br/>                                                                                                                                        |
| [**XMVectorGetIntYPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetintyptr)<br/>             | 抓取 `y` 包含整數資料的 [**XMVECTOR 資料類型**](xmvector-data-type.md) 元件，並將該元件的值儲存在指標所參考的 uint32 \_ t 實例中。<br/>                       |
| [**XMVectorGetIntZ**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetintz)<br/>                   | 取出 `z` [**XMVECTOR 資料類型**](xmvector-data-type.md)的元件。<br/>                                                                                                                                        |
| [**XMVectorGetIntZPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetintzptr)<br/>             | 抓取 `z` 包含整數資料的 [**XMVECTOR 資料類型**](xmvector-data-type.md) 元件，並將該元件的值儲存在指標所參考的 uint32 \_ t 實例中。<br/>                       |
| [**XMVectorGetW**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetw)<br/>                         | 取出 `w` [**XMVECTOR 資料類型**](xmvector-data-type.md)的元件。<br/>                                                                                                                                        |
| [**XMVectorGetWPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetwptr)<br/>                   | 取出 `w` 包含浮點數據的 [**XMVECTOR 資料類型**](xmvector-data-type.md) 元件，並將該元件的值儲存在指向指標所參考的 float 實例中。<br/>                    |
| [**XMVectorGetX**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetx)<br/>                         | 取出 `x` [**XMVECTOR 資料類型**](xmvector-data-type.md)的元件。<br/>                                                                                                                                        |
| [**XMVectorGetXPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetxptr)<br/>                   | 取出 `x` 包含浮點數據的 [**XMVECTOR 資料類型**](xmvector-data-type.md) 元件，並將該元件的值儲存在指向指標所參考的 float 實例中。<br/>                    |
| [**XMVectorGetY**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgety)<br/>                         | 取出 `y` [**XMVECTOR 資料類型**](xmvector-data-type.md)的元件。<br/>                                                                                                                                        |
| [**XMVectorGetYPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetyptr)<br/>                   | 取出 `y` 包含浮點數據的 [**XMVECTOR 資料類型**](xmvector-data-type.md) 元件，並將該元件的值儲存在指向指標所參考的 float 實例中。<br/>                    |
| [**XMVectorGetZ**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetz)<br/>                         | 取出 `z` [**XMVECTOR 資料類型**](xmvector-data-type.md)的元件。<br/>                                                                                                                                        |
| [**XMVectorGetZPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorgetzptr)<br/>                   | 取出 `z` 包含浮點數據的 [**XMVECTOR 資料類型**](xmvector-data-type.md) 元件，並將該元件的值儲存在指向指標所參考的 float 實例中。<br/>                    |
| [**XMVectorSetByIndex**](/previous-versions/windows/desktop/legacy/hh404810(v=vs.85))<br/>             | 使用浮點物件來設定 [**XMVECTOR 資料類型**](xmvector-data-type.md) 之四個元件的其中一個值，其中包含索引所參考的整數資料。<br/>                                         |
| [**XMVectorSetByIndexPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetbyindexptr)<br/>       | 使用浮點實例的指標，設定 [**XMVECTOR 資料類型**](xmvector-data-type.md) 之四個元件的其中一個值，其中包含索引所參考的浮點數據。<br/>                   |
| [**XMVectorSetIntByIndex**](/previous-versions/windows/desktop/legacy/hh404813(v=vs.85))<br/>       | 使用整數實例來設定 [**XMVECTOR 資料類型**](xmvector-data-type.md) 之四個元件的其中一個值，其中包含索引所參考的整數資料。<br/>                                             |
| [**XMVectorSetIntByIndexPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetintbyindexptr)<br/> | 使用整數實例的指標，設定 [**XMVECTOR 資料類型**](xmvector-data-type.md) 的四個元件的值，其中包含索引所參考的整數資料。<br/>                                |
| [**XMVectorSetIntW**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetintw)<br/>                   | 設定 `w` [**XMVECTOR 資料類型**](xmvector-data-type.md)之元件的值。<br/>                                                                                                                                |
| [**XMVectorSetIntWPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetintwptr)<br/>             | 設定 `w` 包含整數資料之 [**XMVECTOR**](xmvector-data-type.md) 的元件，其值包含在指向指標所參考的 uint32 \_ t 實例中。<br/>                                                 |
| [**XMVectorSetIntX**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetintx)<br/>                   | 設定 `x` [**XMVECTOR 資料類型**](xmvector-data-type.md)之元件的值。<br/>                                                                                                                                |
| [**XMVectorSetIntXPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetintxptr)<br/>             | 設定 `x` 包含整數資料之 [**XMVECTOR**](xmvector-data-type.md) 的元件，其值包含在指向指標所參考的 uint32 \_ t 實例中。<br/>                                                 |
| [**XMVectorSetIntY**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetinty)<br/>                   | 設定 `y` [**XMVECTOR 資料類型**](xmvector-data-type.md)之元件的值。<br/>                                                                                                                                |
| [**XMVectorSetIntYPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetintyptr)<br/>             | 設定 `y` 包含整數資料之 [**XMVECTOR**](xmvector-data-type.md) 的元件，其值包含在指向指標所參考的 uint32 \_ t 實例中。<br/>                                                 |
| [**XMVectorSetIntZ**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetintz)<br/>                   | 設定 `z` [**XMVECTOR 資料類型**](xmvector-data-type.md)之元件的值。<br/>                                                                                                                                |
| [**XMVectorSetIntZPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetintzptr)<br/>             | 設定 `z` 包含整數資料之 [**XMVECTOR**](xmvector-data-type.md) 的元件，其值包含在指向指標所參考的 uint32 \_ t 實例中。<br/>                                                 |
| [**XMVectorSetW**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetw)<br/>                         | 設定 `w` [**XMVECTOR 資料類型**](xmvector-data-type.md)之元件的值。<br/>                                                                                                                                |
| [**XMVectorSetWPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetwptr)<br/>                   | 設定 `w` 包含浮點數據之 [**XMVECTOR**](xmvector-data-type.md) 的元件，其值包含在指向指標所參考的 float 實例中。<br/>                                              |
| [**XMVectorSetX**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetx)<br/>                         | 設定 `x` [**XMVECTOR 資料類型**](xmvector-data-type.md)之元件的值。<br/>                                                                                                                                |
| [**XMVectorSetXPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetxptr)<br/>                   | 設定 `x` 包含浮點數據之 [**XMVECTOR**](xmvector-data-type.md) 的元件，其值包含在指向指標所參考的 float 實例中。<br/>                                              |
| [**XMVectorSetY**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsety)<br/>                         | 設定 `y` [**XMVECTOR 資料類型**](xmvector-data-type.md)之元件的值。<br/>                                                                                                                                |
| [**XMVectorSetYPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetyptr)<br/>                   | 設定 `y` 包含浮點數據之 [**XMVECTOR**](xmvector-data-type.md) 的元件，其值包含在指向指標所參考的 float 實例中。<br/>                                              |
| [**XMVectorSetZ**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetz)<br/>                         | 設定 `z` [**XMVECTOR 資料類型**](xmvector-data-type.md)之元件的值。<br/>                                                                                                                                |
| [**XMVectorSetZPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetzptr)<br/>                   | 設定 `z` 包含浮點數據之 [**XMVECTOR**](xmvector-data-type.md) 的元件，其值包含在指向指標所參考的 float 實例中。<br/>                                              |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectXMath 程式庫函式](ovw-xnamath-reference-functions.md)
</dt> </dl>

 

 
