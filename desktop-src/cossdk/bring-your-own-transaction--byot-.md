---
description: '整合您自己的交易 (BYOT) '
ms.assetid: 492875cb-52a7-484f-810e-bd838373b603
title: '整合您自己的交易 (BYOT) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89b6177471d1c56956bba5fafd4f728a6295b29afcc6873495ddb690d2e59c12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118308661"
---
# <a name="bring-your-own-transaction-byot"></a>整合您自己的交易 (BYOT) 

BYOT 可讓您使用或繼承外部交易來建立元件。 也就是說，尚未有相關聯交易的元件可以取得交易。 目前，MTS 交易為自動;元件實例是否存在於交易中，會在建立時決定。 元件的交易屬性和其建立者會決定哪些交易與指定的實例相關聯。 在所有情況下，MTS 都會控制交易存留期。 COM + 會將此延伸至，以允許將任意預先存在的 DTC 或 TIP 交易設定為新元件內容的交易屬性。 這可讓設定的元件與存留期由 TP 監視器、OTS 或 DBMS 控制的交易相關聯。

> [!Note]  
> BYOT 交易必須謹慎使用。 在某些情況下，它們可能會導致跨越多個同步處理網域的交易（也就是，它們允許具有交易的平行處理，進而造成鎖死狀況）。 自動交易（而不是 BYOT 交易）是商務元件撰寫者慣用的程式設計模型。

 

BYOT 交易的介面包含 [**ICreateWithTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) 介面和 [**ICreateWithTipTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex) 介面。 **ICreateWithTransactionEx** 介面會建立在手動交易中登記的物件。 **ICreateWithTipTransactionEx** 介面會使用交易網際網路通訊協定 (提示) ，建立在手動交易內登錄的物件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[繼承手動交易](inheriting-manual-transactions.md)
</dt> </dl>

 

 



