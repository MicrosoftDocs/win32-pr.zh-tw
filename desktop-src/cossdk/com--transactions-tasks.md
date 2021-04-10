---
description: COM + 交易工作
ms.assetid: fe4374f1-2452-4316-be57-b866c438404d
title: COM + 交易工作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70aaebd3e788e1ff12e86b7831979f055367fea7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111037"
---
# <a name="com-transactions-tasks"></a>COM + 交易工作

雖然 COM + 中的自動交易處理可讓您在建立及設定想要參與自動交易的物件時，花更高生產力的開發時間，但您可以執行一些程式設計工作，以針對您的應用程式需求量身打造交易行為。

下列主題討論與交易處理相關的特定程式設計選項。



| 主題                                                                                             | 描述                                                                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [設定交易屬性](setting-the-transaction-attribute.md)<br/>             | 描述如何設定交易對象的交易屬性值。<br/>         |
| [設定交易隔離等級](setting-the-transaction-isolation-level.md)<br/> | 描述如何設定交易對象的交易隔離等級。<br/>     |
| [設定交易超時](setting-the-transaction-time-out.md)<br/>               | 說明如何設定交易的逾時間隔。<br/>                          |
| [設定一致且完成的旗標](setting-the-consistent-and-done-flags.md)<br/>     | 顯示如何使用「一致」和「完成」旗標來控制交易的結果。<br/> |
| [建立 BYOT 物件](creating-byot-objects.md)<br/>                                     | 描述如何建立物件，讓您可以將自己的交易 (BYOT) 。<br/>           |



 

> [!Note]  
> 一般來說，任何更新持續狀態的元件都應該支援交易。 將兩個或多個物件的作業結合成單一工作的元件，應該使用交易來簡化錯誤復原。 此外，若要釋放資源（例如資料庫連接），COM + 中的交易應該盡可能簡短。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 交易概念](com--transactions-concepts.md)
</dt> </dl>

 

 




