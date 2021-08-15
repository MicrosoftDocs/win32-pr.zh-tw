---
description: 本主題描述如何使用 DirectShow 基類，為 DirectShow 的篩選準則執行 DLL。
ms.assetid: d47980d1-6d0c-4b0d-a875-7b072562944a
title: Class factory 和 Factory 範本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9329a0b8cfd22a316add88664604df190ae96c765359c723aa2302c5b1fa1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118402207"
---
# <a name="class-factories-and-factory-templates"></a>Class factory 和 Factory 範本

本主題描述如何使用[DirectShow 基類](directshow-base-classes.md)，為 DirectShow 的篩選準則執行 DLL。

在用戶端建立 COM 物件的實例之前，它會使用 [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) 函數的呼叫，建立物件的 class factory 實例。 然後，用戶端會呼叫 class factory 的 **IClassFactory：： CreateInstance** 方法。 它是實際建立元件並傳回所要求介面之指標的 class factory。  ([**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 函數會在函式呼叫內合併這些步驟。 ) 

下圖顯示方法呼叫的順序。

![建立 class factory 的方法呼叫](images/classfactory.png)

[**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) 會呼叫 [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) 函式，該函式是在 DLL 中定義。 此函式會建立 class factory，並將指標傳回給 class factory 上的介面。 DirectShow 為您執行 **DllGetClassObject** ，但函式依賴您的程式碼以特定方式運作。 若要瞭解其運作方式，您必須瞭解 DirectShow 如何實行 class factory。

Class factory 是專門用來建立另一個 COM 物件的 COM 物件。 每個 class factory 都有一個它所建立的物件類型。 在 DirectShow 中，每個 class factory 都是相同 c + + 類別 **CClassFactory** 的實例。 Class factory 是透過另一個類別 [**CFactoryTemplate**](cfactorytemplate.md)來特製化，也稱為 *factory 範本*。 每個 class factory 都會保留一個指向 factory 範本的指標。 Factory 範本包含特定元件的相關資訊，例如元件的類別識別碼 (CLSID) ，以及函式的指標，該函式會建立元件。

DLL 會宣告原廠範本的全域陣列，DLL 中的每個元件都有一個。 當 [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) 建立新的 class factory 時，它會在陣列中搜尋具有相符 CLSID 的範本。 假設找到一個，它會建立一個持有相符範本指標的 class factory。 當用戶端呼叫 **IClassFactory：： CreateInstance** 時，class factory 會呼叫範本中定義的具現化函數。

下圖顯示方法呼叫的順序。

![dll 中的 class factory 範本](images/classfactory2.png)

此架構的優點是，您只能定義您的元件專屬的一些專案，例如具現化函數，而不需要執行整個 class factory。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[如何建立 DirectShow 篩選 DLL](how-to-create-a-dll.md)
</dt> </dl>

 

 
