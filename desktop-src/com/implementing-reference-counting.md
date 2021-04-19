---
title: 正在執行參考計數
description: 正在執行參考計數
ms.assetid: d4fd98c9-afa4-4c5c-a3c9-44d34881cbdb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0d4dfe2b0faf2fc6557d1b089e33ae6ce4b98cb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106996567"
---
# <a name="implementing-reference-counting"></a>正在執行參考計數

參考計數需要在實作項類別的部分，以及使用該類別之物件的用戶端上進行工作。 當您執行類別時，您必須將 [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) 和 [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 方法實作為 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) 介面的一部分。 這兩種方法具有下列簡單的實作為：

-   [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) 會遞增物件的內部參考計數。
-   [**發行**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 會先遞減物件的內部參考計數，然後檢查參考計數是否已下降到零。 如果有的話，這表示沒有人使用此物件，因此釋放函式會 **解除** 分配物件。

大部分物件的常見實作為方法之一，就是只執行這些方法的其中一項 (，以及在所有介面之間共用的 [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))) ，因此是套用至整個物件的參考計數。 不過，從用戶端的觀點來看，參考計數是嚴格且清楚的每個介面指標的概念，因此，利用這項功能的物件可以根據目前現存的介面指標，動態地建立、終結、載入或卸載部分功能。 這些堆疊稱為「卸載 *介面*」。

只要用戶端呼叫方法 (或 API 函式) ，例如會傳回新介面指標的 [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))，呼叫的方法就會負責透過傳回的指標遞增參考計數。 例如，當用戶端第一次建立物件時，它會接收指向物件的介面指標，而從用戶端的觀點來看，它的參考計數是一個。 如果用戶端接著在介面指標上呼叫 [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) ，參考計數就會變成二。 用戶端 [**必須呼叫介面**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 指標上的兩次，以卸載其對物件的所有參考。

例如，當用戶端在新介面或相同介面的第一個指標上呼叫 [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) 時，每個介面指標的參考計數會是嚴格的。 在上述任一情況下，用戶端都必須呼叫每個指標一次的 [**發行**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 。 當系統要求相同的介面多次時，COM 不需要物件傳回相同的指標。  (唯一的例外狀況是對 [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)的查詢，該查詢會識別 COM 的物件。 ) 這可讓物件的執行有效率地管理資源。

執行緒安全也是執行 [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) 和 [**發行**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)的重要問題。 如需詳細資訊，請參閱 [進程、執行緒和單元](processes--threads--and-apartments.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[透過參考計數來管理物件存留期](managing-object-lifetimes-through-reference-counting.md)
</dt> </dl>

 

 