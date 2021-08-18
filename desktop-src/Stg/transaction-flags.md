---
title: 交易旗標
description: 物件可以在直接或交易模式中開啟。
ms.assetid: f3be52b9-957c-4ab9-8fc1-e765faae2489
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79a3f389def4bdbb9d0cabf92500b316ae354878ec5f790b44e9f01121aeb57a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886780"
---
# <a name="transaction-flags"></a>交易旗標

物件可以在直接或交易模式中開啟。 在直接模式中開啟物件時，會立即和永久變更變更。 當物件在交易模式中開啟時，會緩衝處理變更，以便在完成編輯之後，可以明確地認可或還原變更。 已認可的變更會儲存到物件，而還原的變更會被捨棄。 Direct 模式是預設的存取模式。

在父代儲存物件上不需要交易模式，就能將它用於嵌套元素上。 不過，嵌套專案的交易會在其父儲存物件的交易內進行嵌套。 因此，在對父物件所做的變更認可之前，無法認可對子物件所做的變更，而且在最上層父)  (的根儲存物件實際寫入磁片之前，都會維持未認可狀態。 換句話說，變更會往外移動：內建物件會將變更發佈至其直屬容器的交易。

 

 




