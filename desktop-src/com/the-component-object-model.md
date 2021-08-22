---
title: 元件物件模型
description: 元件物件模型
ms.assetid: f5f66603-466c-496b-be29-89a8ed9361dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07ad81adeaf41670468dd41bbf344a3fd7358c14f4b3cbeb2e482812a083ecfb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462338"
---
# <a name="the-component-object-model"></a>元件物件模型

Microsoft 元件物件模型 (COM) 是一種與平臺無關、分散式、物件導向的系統，可用來建立可互動的二進位軟體元件。 COM 是 Microsoft 的 OLE (複合檔案的基礎技術，) ，ActiveX (具備網際網路功能的元件) 和其他專案。

若要瞭解 COM (以及所有以 COM 為基礎的技術) ，請務必瞭解這不是物件導向的語言，而是標準的。 COM 也不會指定應用程式的結構。語言、結構和執行的詳細資料會留給應用程式開發人員。 相反地，COM 會指定一個物件模型和程式設計需求，讓 COM 物件 (也稱為 COM 元件，或有時候只是) 與其他物件互動的 *物件* 。 這些物件可以在單一進程內、在其他進程中，甚至可以在遠端電腦上。 您可以使用不同的語言來撰寫這些語言，而且它們的結構可能相當不同，這就是為什麼 COM 稱為 *二進位標準*;在程式轉換為二進位機器碼之後套用的標準。

COM 的唯一語言需求是以可以建立指標結構的語言來產生程式碼，而且可以明確或隱含地透過指標呼叫函式。 以物件為導向的語言（例如 c + + 和 Smalltalk）提供的程式設計機制可簡化 COM 物件的執行，但 C、JAVA 和 VBScript 等語言可以用來建立和使用 COM 物件。

COM 會定義 COM 物件的基本性質。 一般情況下，軟體物件是由一組資料和運算元據的函式所組成。 COM 物件是指透過一或多組相關的函式，以獨佔方式來存取物件資料的物件。 這些函式集合稱為 *介面*，介面的函式稱為 *方法*。 此外，COM 要求取得介面方法之存取權的唯一方法是透過介面指標。

除了指定基本的二進位物件標準之外，COM 也會定義特定的基本介面，以提供所有以 COM 為基礎的技術通用的函式，並提供少量的函式，讓所有元件都需要這些功能。 COM 也會定義物件如何透過分散式環境一起運作，並已新增安全性功能來協助提供系統和元件的完整性。

本節中的下列主題描述與設計 COM 物件相關的基本 COM 問題：

-   [COM 物件和介面](com-objects-and-interfaces.md)
-   [使用和執行 IUnknown](using-and-implementing-iunknown.md)
-   [重複使用物件](reusing-objects.md)
-   [COM 程式庫](the-com-library.md)
-   [管理記憶體配置](managing-memory-allocation.md)

 

 




