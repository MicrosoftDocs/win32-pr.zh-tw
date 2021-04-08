---
title: 在應用程式中新增驅動程式
description: 在應用程式中新增驅動程式
ms.assetid: cd9bd0a8-652b-440b-a197-81e20a9d71f1
keywords:
- 音訊壓縮管理員 (的) ，新增驅動程式
- " (音效壓縮管理員) 、新增驅動程式"
- 進行中的範例，新增驅動程式
- 新增驅動程式
- acmDriverAdd 函式
- 全域驅動程式
- 本機驅動程式
- 音訊壓縮管理員 (的) 、全球驅動程式
- " (音效壓縮管理員) 、全球驅動程式"
- 音訊壓縮管理員 (的) 、本機驅動程式
- " (音效壓縮管理員) 的本機驅動程式"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 000bf7bded89b778f271599d5ce0f8d7f7bd5f72
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021464"
---
# <a name="adding-drivers-within-an-application"></a>在應用程式中新增驅動程式

如果您需要您的應用程式在內部執行自己的壓縮常式，應用程式可以藉由呼叫 [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) 函式，將驅動程式新增至執行程式。 應用程式會藉由提供符合 [**acmDriverProc**](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc) 原型的函式來執行驅動程式。 應用程式新增驅動程式之後，應用程式就可以透過執行程式來使用驅動程式，因為它會使用任何其他驅動程式。

進行的處理常式會將驅動程式視為全域或本機。 應用程式會指定是否應在呼叫 **acmDriverAdd** 時，將驅動程式新增為全域或本機。 全域和本機驅動程式之間有兩個差異：

-   新增為全域驅動程式的驅動程式不會與其他應用程式共用。
-   應用程式可以藉由呼叫 [**acmDriverPriority**](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority) 函式，直接改變全域驅動程式 (的優先順序，而不是本機驅動程式) 。 當您在尋找適當的驅動程式來提供函式呼叫的執行時，會進行優先的搜尋。 [進行中] 會在優先順序高於全域驅動程式時，提供本機驅動程式。 最近新增的本機驅動程式具有最高優先順序。

 

 




