---
title: Container-Specific 私用介面
description: Container-Specific 私用介面
ms.assetid: 429cf71c-9b9d-4d0b-b5de-91fbe1dde3cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25c6569a79e9f1801c6fd82543bc40408903c780
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311300"
---
# <a name="container-specific-private-interfaces"></a>Container-Specific 私用介面

某些容器會提供容器專屬的私用介面，以提供額外的功能或改善效能。 依賴這些容器特定介面的控制項，如果可能的話，就不會有這些容器特定介面的運作方式，因此控制項在不同的容器中會有作用。 例如，Visual Basic 會實作為控制項的字串格式功能提供的私用介面。 如果控制項使用這些私用格式介面，如果無法使用這些介面，就應該能夠使用預設的格式化支援來執行。 如果控制項可在沒有私用介面的情況下運作，則應該採取適當的動作 (例如警告使用者的功能已減少) 但仍繼續運作。 如果這不是一個選項，則元件類別應視需要註冊，如此一來，只有支援這項功能的容器可以裝載這些控制項。

 

 




