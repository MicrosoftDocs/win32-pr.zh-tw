---
description: 在正在進行調試的進程中發生例外狀況時，系統會將例外狀況傳遞給偵錯工具，以通知偵錯工具。 這就是所謂的第一次通知。 系統接著會暫止正在進行調試之進程中的所有線程。
ms.assetid: 6fdc02ac-9c33-49a8-8614-8b0cc2bf811b
title: 用於偵錯工具的例外狀況處理函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab4542b6e1d3ad2699b3cb43d15e327d26156760980188555b1a4bf9c68e9a7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119573168"
---
# <a name="exception-handling-functions-for-debugging"></a>用於偵錯工具的例外狀況處理函式

在正在進行調試的進程中發生例外狀況時，系統會將例外狀況傳遞給偵錯工具，以通知偵錯工具。 這就是所謂的 *第一次通知*。 系統接著會暫止正在進行調試之進程中的所有線程。

如果偵錯工具未處理例外狀況，系統會嘗試找出適當的例外狀況處理常式。 如果系統找不到適當的系統，系統會再次通知偵錯工具發生例外狀況。 這就是所謂的 *最後機會通知*。 如果偵錯工具未在最後一次發生通知之後處理例外狀況，則系統會終止正在進行調試的進程。

如需詳細資訊，請參閱 [偵錯工具例外狀況處理](debugger-exception-handling.md)。

 

 



