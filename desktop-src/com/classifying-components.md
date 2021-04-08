---
title: 分類元件
description: 分類元件
ms.assetid: 4d805532-96c9-400d-b78a-f8d0d9bdbf83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53ea1547c219a44262fdeaf7edb02f65c7a3aac6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840500"
---
# <a name="classifying-components"></a>分類元件

當用戶端能夠流覽登錄中的 Clsid 清單並選取要使用的元件時，載入登錄中的每個元件，並針對其支援的介面進行查詢，會相當耗時。 若要在建立元件的實例之前，判斷元件是否支援所需的介面，已開發將元件分類為類別的方法。

元件類別是一組已指派 GUID 名為 CATID 的介面。 在元件類別中執行所有介面的元件，會自行註冊為該元件類別目錄的成員。 然後可以從登錄中選取屬於特定元件類別目錄的元件。 藉由將本身註冊為元件類別目錄的成員，元件會保證它支援元件類別中的所有成員介面。

元件可以是許多類別的成員。 它不限於元件類別中的支援介面。 除了元件類別中的介面之外，它還可以支援任何介面。

相較于標準註冊的元件，開發人員必須撰寫程式碼以手動方式註冊物件，但元件類別會將大部分的工作自動化。 [**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister)介面的六個方法會定義元件類別，並註冊可執行或需要它們的物件。 [元件類別管理員](the-component-categories-manager.md)物件會執行這個介面。 如需使用元件類別的詳細資訊，請參閱 **ICatRegister** 和 [**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[註冊 COM 應用程式](registering-com-applications.md)
</dt> </dl>

 

 




