---
description: 交易和 COM + JIT 啟用
ms.assetid: f7fad383-4081-4a49-aa03-59861fcefc97
title: 交易和 COM + JIT 啟用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281691ebc9c8d5c654ea6ff0c3035d7e285f62c5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847507"
---
# <a name="transactions-and-com-jit-activation"></a>交易和 COM + JIT 啟用

COM + JIT 啟用會緊密地系結至自動交易。 當您將元件設定為需要交易或需要新的交易時，JIT 啟用也會自動啟用。 這兩項功能自然地搭配使用。 交易式 JIT 啟用的元件會共用下列特性：

-   無 國籍。 您不會保存可能違反交易隔離的狀態，也不會保留物件停用時遺失的狀態。

-   快速使用。 在自動交易中執行工作的物件標準使用模式是執行一些小型工作單位、投票和結束。

    > [!Note]  
    > 您在 COM + 交易中投票的方式以及 JIT 啟用的信號 doneness，也會緊密系結在一起。 如需詳細資訊，請參閱 [設定完成位](setting-the-done-bit.md)。

     

-   重複使用。 當交易式工作適當地細分時，用戶端會使用相同的物件來執行不可部分完成的工作。

-   在認可或中止時停用。 在 COM + 中，交易認可或中止時，會停用交易界限內的所有物件。

搭配 COM + 交易元件，JIT 啟用可將通道保持開啟狀態，因為用戶端持有交易對象的長期參考。 做進一步的增強功能，您可以選擇將交易對象集區化，以重複使用其保留的資源、加快物件重新啟用時間，以及密切地管理為指定物件使用記憶體資源的方式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 即時啟用概念](com--just-in-time-activation-concepts.md)
</dt> <dt>

[啟用元件的 JIT 啟用](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[物件共用和 COM + JIT 啟用](object-pooling-and-com--jit-activation.md)
</dt> </dl>

 

 



