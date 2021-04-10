---
title: 選擇建立可存取物件的時機
description: 伺服器開發人員可以在建立容器時建立容器內所有可存取的物件，也可以動態建立可存取的物件。
ms.assetid: 26c8bb4b-19ec-4fd5-b758-30cb6a513818
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 987b40527c178c40101288b0192c38d9a9b06040
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021740"
---
# <a name="choosing-when-to-create-accessible-objects"></a>選擇建立可存取物件的時機

伺服器開發人員可以在建立容器時建立容器內所有可存取的物件，也可以動態建立可存取的物件。

例如，假設有幾個自訂控制項的對話方塊。 當對話方塊出現時，伺服器會為所有自訂控制項建立可存取的物件。 但是，如果其中一個控制項是自訂下拉式方塊，則伺服器會等待，直到使用者選取它來為下拉式方塊包含的專案建立可存取物件為止。

藉由讓父系動態建立可存取的物件，應用程式會使用較少的記憶體，而不是事先建立所有可能的可存取物件。

 

 




