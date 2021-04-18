---
title: 資料類型轉換
description: 資料類型轉換
ms.assetid: 54688ee9-2dd7-466b-b278-13d6f9d1e6ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8135a3fb86fda9ac9ab9666ec42991a8d04d9e6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106966059"
---
# <a name="data-type-conversions"></a>資料類型轉換

每種程式設計語言都會定義資料的特定類型和容器。 大部分的資料類型，尤其是基本專案，都可以輕鬆地對應到其他程式設計語言。 不過，某些資料類型在另一種語言中沒有對等專案，而且無法轉換。

如需程式設計語言無法辨識之資料類型的特定資訊，請參閱下列主題：

-   [轉換成 c + +](translating-to-c--.md)
-   [翻譯為 Visual Basic](translating-to-visual-basic.md)
-   [轉換成 JAVA](translating-to-java.md)

下表列出一般資料類型的程式設計語言之間的轉換。



| C++                                     | Visual Basic             | Java                               | 包含                                                                                       |
|-----------------------------------------|--------------------------|------------------------------------|------------------------------------------------------------------------------------------------|
| **signed char**<br/>              | 不支援<br/> | **byte**<br/>                | 1位元組帶正負號的整數 <br/>  (VT \_ I1， \[ T \]) <br/>                                   |
| **unsigned char**<br/>            | **位元組**<br/>      | 不支援<br/>           | 1位元組不帶正負號的整數 <br/>  (VT \_ UI1， \[ V \] \[ T \] \[ P \] \[ S \]) <br/>                 |
| **unsigned char**<br/>            | **字元**<br/> | **char**<br/>                | 雙位元組 Unicode 字元 <br/>  (VT \_ UI2， \[ T \] \[ P \]) <br/>                          |
| **short**<br/>                    | **整數**<br/>   | **short**<br/>               | 2位元組帶正負號的整數 <br/>  (VT \_ I2， \[ V \] \[ T \] \[ P \] \[ S \]) <br/>                    |
| **unsigned short**<br/>           | 不支援<br/> | 不支援<br/>           | 2位元組不帶正負號的整數 <br/>  (VT \_ UI2， \[ T \] \[ P \]) <br/>                           |
| **int**<br/>                      | **Long**<br/>      | **int**<br/>                 | 4位元組帶正負號的整數 <br/>  (VT \_ I4， \[ V \] \[ T \] \[ P \] \[ S \]) <br/>                    |
| **不帶正負號的整數**<br/>             | 不支援<br/> | 不支援<br/>           | 4位元組不帶正負號的整數 <br/>  (VT \_ UI4， \[ T \] \[ P \]) <br/>                           |
| **\_\_int64**<br/>                | 不支援<br/> | **long**<br/>                | 8位元組帶正負號的整數 <br/>  (VT \_ I8， \[ T \] \[ P \]) <br/>                              |
| **未簽署的 \_ \_ int64**<br/>       | 不支援<br/> | 不支援<br/>           | 8位元組不帶正負號的整數 <br/>  (VT \_ UI8， \[ T \] \[ P \]) <br/>                           |
| **float**<br/>                    | **Single**<br/>    | **float**<br/>               | 4位元組浮點數 <br/>  (VT \_ R4， \[ V \] \[ T \] \[ P \] \[ S \]) <br/>             |
| **double**<br/>                   | **Double**<br/>    | **double**<br/>              | 8位元組浮點數 <br/>  (VT \_ R8， \[ V \] \[ T \] \[ P \] \[ S \]) <br/>             |
| **BSTR**<br/>                     | **String**<br/>    | **java lang.ini 字串**<br/>    | Automation 字串 <br/>  (VT \_ BSTR， \[ V \] \[ T \] \[ P \] \[ S \]) <br/>                      |
| **Bool**<br/>                     | **布林值**<br/>   | **boolean**<br/>             | Boolean <br/>  (VT \_ BOOL， \[ V \] \[ T \] \[ P \] \[ S \]) <br/>                                |
| **變異**<br/>                  | **變異**<br/>   | **.com.. .com. Variant**<br/>  | 變得更遠\* <br/>  (VT \_ VARIANT， \[ V \] \[ T \] \[ P \] \[ S \]) <br/>                       |
| [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)<br/> | **object**<br/>    | **.com. .com**<br/> | IDispatch 介面指標 <br/>  (VT \_ 分派， \[ V \] \[ T \] \[ P \] \[ S \]) <br/>        |
| **DATE**<br/>                     | **日期**<br/>      | **.com.. .com. Variant**<br/>  | Date <br/>  (VT \_ DATE， \[ V \] \[ T \] \[ P \] \[ S \]) <br/>                                   |
| **CURRENCY**<br/>                 | **貨幣**<br/>  | **.com.. .com. Variant**<br/>  | 貨幣 <br/>  (VT \_ CY、 \[ v \] \[ t \] \[ P \] \[ s \] 或 VT \_ DECIMAL、 \[ v \] \[ t \] \[ S \]) <br/> |



 

如需 VARTYPE 值和其使用方式的相關資訊，請參閱 [IDispatch 資料類型和結構](/previous-versions/ms221600(v=vs.100))。

指令碼語言之間的資料類型轉換比程式設計語言的轉換簡單得多。 JScript 和 JavaScript 都支援相同的資料類型，而 VBScript 僅支援單一資料類型，也就是 **Variant**。 因此，當轉換成 VBScript 時，所有的 JScript 和 JavaScript 資料類型都會變成 **Variant** 類型。 當您將 VBScript 轉換成 JScript 或 JavaScript 時， **變數** 類型會變成數位、字串、布林值等等。

 

