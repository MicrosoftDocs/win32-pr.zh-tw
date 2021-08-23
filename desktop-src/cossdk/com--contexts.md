---
description: 針對在 COM + 應用程式內執行的已設定元件，內容是提供 COM + 服務的基礎。
ms.assetid: 62a0bef2-c3c2-4a60-a5d1-6c038958e13e
title: COM + 內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71c48e2fb9a118bff5fe4d6590ff859f0f053ab29687d4f4a2a070d44af37b25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119730648"
---
# <a name="com-contexts"></a>COM + 內容

針對在 COM + 應用程式內執行的已設定 *元件，內容* 是提供 com + 服務的基礎。 在 COM + 中，內容會定義為一組與一或多個 COM 物件相關聯的執行時間屬性，而這些物件是用來提供這些物件的服務。

在 COM + 中，每個 COM 物件會在執行 (也就是在其啟動和停用) 之間，以及每個內容都在一個 COM 單元內，精確地與一個內容相關聯。 多個物件可在相同的內容中執行，而多個內容可以位於同一個單元內。 當物件啟動時初始化、內容屬性，例如資訊安全內容屬性，代表物件的執行時間需求。

> [!Note]  
> 如果未設定的元件不使用 COM + 服務，則內容大部分都會被忽略。

 

COM + 會使用內容屬性作為提供執行時間服務的基礎。 這些屬性會保存狀態，以決定執行環境如何針對內容中的物件執行服務。 在某些情況下，您可以直接與物件的內容屬性互動，以指出與提供給物件之服務相關的一些狀態。 例如，當參與自動交易的物件對交易的結果投票時，您會這麼做。

如需這些概念的 COM 基礎詳細討論，請參閱 [進程、執行緒和單元](/windows/desktop/com/processes--threads--and-apartments)。

## <a name="programmatic-interaction-with-context-properties"></a>以程式設計方式與內容屬性互動

每個內容都有相關聯的 [**ObjectCoNtext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) 物件，此物件會持續追蹤其屬性。 您可以藉由呼叫 [**GetObjectCoNtext**](/windows/desktop/api/ComSvcs/nf-comsvcs-getobjectcontext)函數來存取 **ObjectCoNtext** 。 存取 **ObjectCoNtext** 之後，您可以在其公開的 [**IObjectCoNtext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) 介面上呼叫方法，以操作內容屬性。

例如，呼叫 [**IObjectCoNtext：： SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) 的效果，是將交易一致性位設定為「一致」，並在與物件相關聯的內容上將 [JIT 啟用](com--just-in-time-activation.md) 完成的位設定為「完成」。 「一致」表示您投票認可交易的 COM +，而「完成」表示您的物件已準備好在方法傳回時停用。

除了 [**IObjectCoNtext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)之外，其他提供內容屬性存取權的特殊介面為 [**IObjectCoNtextInfo**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontextinfo)、 [**ICoNtextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)和 [**IObjectCoNtextActivity**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontextactivity)。 在特定範圍內， [**ISecurityCallCoNtext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext) 也會存取內容屬性。 您可以使用 [**IGetSecurityCallCoNtext：： GetSecurityCallCoNtext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext) 來取得 **ISecurityCallCoNtext**。

## <a name="understanding-activation-and-interception"></a>瞭解啟用與攔截

一般來說，您只需要將內容考慮到它代表一些屬性的範圍，其中一些可設定或取得，可用來為您的元件提供 COM + 服務。 不過，在某些情況下，您可能需要更詳細地考慮下列兩個內容相關的 facet：

-   [內容啟用](context-activation.md)，或在適當的內容中初始化物件。
-   [攔截](interception-of-cross-context-calls.md)，或 com + 在內容界限之間執行的呼叫。

## <a name="relation-to-mts-context-wrappers"></a>與 MTS 內容包裝函式的關聯

內容有效取代了 MTS 內容包裝函式。 他們所提供的目的（藉由陷印建立要求來提供自動服務）現在是 COM + 的整合功能。 因此，您不再需要使用 [**SafeRef**](/windows/desktop/api/ComSvcs/nf-comsvcs-saferef) 函數。 在 MTS 中， **SafeRef** 是用來取得物件的參考，該物件可在其內容包裝函式之外傳遞。 在 COM + 中，這是不必要的; (**這個** 指標) 工作的一般物件參考。

 

 
