---
description: Tablet PC 畫筆可以有一個以上的一端可以與數位板互動。
ms.assetid: c1aa0d65-cfea-4720-ad09-7add724e03c7
title: 使用一個畫筆的多重功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8313e6a13cb48900e0c0d31c2e1e590e07df6c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320928"
---
# <a name="multiple-functionality-with-one-pen"></a>使用一個畫筆的多重功能

Tablet PC 畫筆可以有一個以上的一端可以與數位板互動。 如果畫筆的兩端都可以產生事件，則可以使用一端來配置筆墨、選取和點，而另一端也可以用於其他功能（例如清除）。

若要執行這類功能，您的應用程式必須能夠判斷正在使用畫筆的哪一端，以及變更游標的外觀。 它可以藉由在資料 [**指標**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件上尋找 [**反向**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted)屬性的狀態來完成這項作業。

如需使用畫筆背面進行清除的特定詳細資訊，請參閱 [使用畫筆來清除筆墨](erasing-ink-with-the-pen.md)。 此外， [筆跡清除範例](ink-erasing-sample.md) 會示範如何使用畫筆的背面來清除筆墨。

 

 



