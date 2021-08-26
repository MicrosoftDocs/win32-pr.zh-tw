---
description: 設定完成位
ms.assetid: badd3b5a-ce6f-4be7-9dd8-a3b17344b185
title: 設定完成位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ad2d9a9dc06caa623d3f7c58d51aec389b40a1f3315ae09a21052bdf6e2ae3a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070248"
---
# <a name="setting-the-done-bit"></a>設定完成位

COM + 會根據內容屬性的狀態（完成位）停用 JIT 啟動的物件，如下所示：

-   當完成位設定為 True 時，COM + 會在目前的方法呼叫傳回時停用物件。
-   當完成位設定為 False 時，當目前的方法呼叫傳回時，物件會保持作用中狀態。

根據預設，當建立物件並初始化其內容時，完成位會設為 False。  (任何 JIT 啟動的物件都是在它自己的內容中建立的，因此它會有自己的完成位來設定 ) 。不過，您可以使用自動完成屬性，以每個方法為基礎變更此預設設定。 您可以透過下列方式設定完成位：

-   使用 [ **ICoNtextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate)
-   使用 [ **IObjectCoNtext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext)
-   使用自動完成屬性

## <a name="using-icontextstate"></a>使用 ICoNtextState

您可以使用 [**ICoNtextState：： SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) 將完成位設定為 True 或 False。

您可以使用 [**ICoNtextState：： GetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-getdeactivateonreturn) 從物件內容取得完成位的目前狀態。

## <a name="using-iobjectcontext"></a>使用 IObjectCoNtext

您可以在 [**IObjectCoNtext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) 上使用下列方法來設定完成位，同時設定在交易中用來投票的一致位：

-   [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) 會通知您已完成，而且您會投票以認可目前的交易。 它會將完成位和一致的位設定為 True。
-   [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) 表示您已完成，並 dooms 目前的交易。 它會將完成的位設定為 True，並將一致的位設定為 False。
-   [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit) 表示您未完成，但您已投票認可交易。 它會將完成的位設定為 False，並將一致的位設定為 True。
-   [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit) 信號表示您未完成，而且您目前未對交易進行投票，通常是因為狀態不一致。 它會將完成位和一致的位設定為 False。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 即時啟用概念](com--just-in-time-activation-concepts.md)
</dt> <dt>

[啟用元件的 JIT 啟用](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[物件共用和 COM + JIT 啟用](object-pooling-and-com--jit-activation.md)
</dt> <dt>

[交易和 COM + JIT 啟用](transactions-and-com--jit-activation.md)
</dt> </dl>

 

 



