---
description: 設定一致且完成的旗標
ms.assetid: d9b6096d-f93c-4f8e-a4d9-ea8309b35f0f
title: 設定一致且完成的旗標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd45d457828a222ce7f4ccbdc0080001b0f0b55f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468097"
---
# <a name="setting-the-consistent-and-done-flags"></a>設定一致且完成的旗標

您可以在 [**IObjectCoNtext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) 或 [**ICoNtextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) 介面上叫用方法，以設定一致和完成的旗標。 這兩個介面所使用的策略有很大的差異。 **IObjectCoNtext** 有四種方法可將一致和完成的旗標系結在唯一組合中，而 **ICoNtextState** 有兩種方法可讓您個別設定每個旗標。 **IObjectCoNtext** 的方法也會透過 [**ObjectCoNtext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext)物件公開。

針對每個旗標的獨立控制， [**ICoNtextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) 會提供方法將一致旗標設定為 True 或 false，以及將完成旗標設為 True 或 false 的方法。 這些方法分別為 [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) 和 [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn)。 **ICoNtextState** 介面也包含可取得每個旗標目前值的方法。

當您將 [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) 方法值設定為 TxCommit 時，com + 會確認交易是否存在。 如果 COM + 未偵測到交易，則會產生您可以在記錄檔中捕捉的錯誤。 例如，假設有人不慎將您元件的交易屬性設定為不受支援，但您預期會將它設定為 Required。 藉由設定 **SetMyTransactionVote** = TxCommit，您可以識別衝突並採取動作。

下表說明可用於設定一致和完成旗標的方法呼叫。



| 一致的旗標  | 完成旗標        | IObjectCoNtext 方法                                            | ICoNtextState 方法                                                                                                                                                                                    |
|------------------|------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 是<br/>  | 否<br/> | [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit)<br/>   | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = TxCommit <br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = False<br/> |
| False<br/> | False<br/> | [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit)<br/> | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = TxAbort <br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = False<br/>  |
| False<br/> | True<br/>  | [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)<br/>           | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = TxAbort <br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = True<br/>   |
| True<br/>  | True<br/>  | [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete)<br/>     | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = TxCommit <br/>[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = True              |



 

> [!Note]  
> 在方法層級設定的自動完成屬性，可能會影響一致和完成旗標的設定方式。 如需有關自動完成屬性的詳細資訊，請參閱為 [方法啟用自動完成](enabling-auto-done-for-a-method.md) 和 [設定完成位](setting-the-done-bit.md)。

 

 

 




