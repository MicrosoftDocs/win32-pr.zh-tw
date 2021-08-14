---
title: COM 類別物件和 Clsid
description: COM 伺服器會實作為 COM 類別。
ms.assetid: 0073acdf-38a8-4f1a-aa26-379456a95fca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8a6bcd00f886d3a754a44658e669189d28fd2fa121248b667ba2a3928b626f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118550622"
---
# <a name="com-class-objects-and-clsids"></a>COM 類別物件和 Clsid

COM 伺服器會實作為 COM 類別。 *COM 類別* 是在每次與指定物件互動時，執行程式碼中的一組介面。 C + + 類別和 COM 類別之間有一個重要的差異：在 c + + 中，類別是型別，而 COM 類別只是物件的定義，而且沒有任何型別，不過 c + + 程式設計人員可以使用 c + + 類別來執行它。 COM 的設計目的是要讓不同的應用程式使用類別，包括不知道該特定類別是否存在而撰寫的應用程式。 因此，指定物件類型的類別程式碼存在於動態連結程式庫 (DLL) 或其他可執行檔應用程式 (EXE) 中。

每個 COM 類別都是由 *CLSID*（伺服器必須註冊的唯一128位 GUID）所識別。 COM 會在用戶端要求時使用此 CLSID，將特定資料與包含可執行類別之程式碼的 DLL 或 EXE 產生關聯，進而建立物件的實例。

針對相同電腦上的用戶端和伺服器，伺服器的 CLSID 是用戶端的所有需求。 在每部電腦上，COM 會維護一個資料庫 (它會使用 Microsoft Windows 和 Macintosh 平臺上的系統登錄) 系統上所安裝伺服器的所有 clsid。 這是每個 CLSID 和 DLL 或 EXE （裝載該 CLSID 的程式碼）的位置之間的對應。 當用戶端想要建立 COM 類別的實例並使用其服務時，COM 會參考此資料庫，因此用戶端永遠不需要知道程式碼在電腦上的絕對位置。

若為分散式系統，COM 會提供登錄專案，讓遠端伺服器自行註冊以供用戶端使用。 雖然應用程式只需要知道伺服器的 CLSID，因為它們可以依賴登錄找出伺服器，但是 COM 可讓用戶端覆寫登錄專案並指定伺服器位置，以充分利用網路。  (參閱 [尋找遠端物件](locating-a-remote-object.md)。 ) 

建立類別實例的基本方法是透過 COM *類別物件*。 這只是一個中繼物件，可支援建立指定類別之新實例的通用功能。 大部分用來從 CLSID 建立物件的類別物件都支援 [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) 介面，也就是包含重要 [**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) 方法的介面。 您可以針對每個您提供要具現化的物件類別，執行 **IClassFactory** 介面。  (如需有關如何執行 **IClassFactory** 的詳細資訊，請參閱實 [IClassFactory](implementing-iclassfactory.md)。 ) 

> [!Note]  
> 支援某些其他自訂類別 factory 介面的伺服器，並不需要特別支援 [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) 。 不過，呼叫 [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) 以外的啟用函式 (例如 [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)) 需要伺服器支援 **IClassFactory**。

 

當用戶端想要建立伺服器物件的實例時，它會在 [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject)的呼叫中使用所需的物件 CLSID。  (此呼叫可以是直接或隱含的，透過其中一個物件建立協助程式函式。 ) 此函式會尋找與 CLSID 相關聯的程式碼，並建立類別物件，並提供所要求介面的指標。  (**CoGetClassObject** 會採用指定用戶端所需介面指標的 *riid* 參數。 ) 

> [!Note]  
> COM 只有幾個函式，許多其他函式都已建立。 其中最重要的可能是 [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject)，其基礎是所有實例建立功能。

 

使用這個指標，呼叫端就可以建立物件的實例，並取得物件上所要求介面的指標。 這通常是初始化介面，用來啟始物件 (將它置於執行中狀態) ，讓用戶端可以使用它想要的物件來執行任何工作。 使用 COM 的基本函數時，用戶端也必須小心釋放所有物件指標。

啟用物件實例的另一個機制是透過類別標記。 類別標記系結至其所建立之類別的類別物件。 如需詳細資訊，請參閱 [類別的名字](class-monikers.md)。

COM 提供數個協助程式函數，可減少建立物件實例的工作。 這些會在 [實例建立](instance-creation-helper-functions.md)協助程式函式中描述。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[透過類別物件建立物件](creating-an-object-through-a-class-object.md)
</dt> </dl>

 

 