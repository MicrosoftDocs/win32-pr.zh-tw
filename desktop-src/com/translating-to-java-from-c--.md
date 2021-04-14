---
title: 從 c + + 轉換成 JAVA
description: 使用 c + + 程式設計語言，開發人員可以直接存取儲存特定變數的記憶體。 記憶體指標可提供此直接存取。 在 JAVA 中，系統會為您處理指標。
ms.assetid: 2c8de3d9-3410-4153-b612-4afab8a69a18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf63754782cba82819479a7e26535b518835580b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371903"
---
# <a name="translating-to-java-from-c"></a>從 c + + 轉換成 JAVA

使用 c + + 程式設計語言，開發人員可以直接存取儲存特定變數的記憶體。 記憶體指標可提供此直接存取。 在 JAVA 中，系統會為您處理指標。

在 JAVA 中，結構 **、等** 位和 **typedef** 複合資料型別只會透過使用類別來處理。 例如，c + + **VARIANT** 資料類型會對應至 JAVA 中的 .com.. **.com** 。

在 c + + 中，字串是字元陣列。 在 JAVA 中，字串是物件。 作用於字串的方法會將字串視為完整的物件。

COM 方法會傳回稱為 **HRESULT** 的值，這是32位的錯誤碼。 適用于 Microsoft Internet Explorer 的 JAVA 支援會定義會包裝 **HRESULT** 錯誤碼的 **ComException** 類別。

JAVA 不支援不帶正負號的資料類型，除了 **char** 之外，也就是16位不帶正負號的整數。 接受或傳回其他不帶正負號資料類型的方法，無法從 JAVA 使用。

JAVA 不支援多維陣列。 接受或傳回多維陣列的方法無法從 JAVA 使用。

JAVA 中的布林值不能轉換成0和1。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[轉換成 JAVA](translating-to-java.md)
</dt> </dl>

 

 




