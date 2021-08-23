---
description: 當您使用 CreateProcess 函數建立處理常式時，可以指定進程使用安全性屬性結構，繼承 mutex、事件、信號或計時器物件的控制碼 \_ 。
ms.assetid: 36491a5c-7599-4f69-ab76-d3a62261a151
title: 物件繼承
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab6d2380ac0012e0f1005df2dfc4b820bee82a7974f3ca03d856c7df9fb8446
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661378"
---
# <a name="object-inheritance"></a>物件繼承

當您使用 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) 函數建立處理常式時，可以指定進程使用 [**安全性 \_ 屬性**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) 結構，繼承 mutex、事件、信號或計時器物件的控制碼。 進程繼承的控制碼具有與原始控制碼相同的物件存取權。 繼承的控制碼會出現在所建立之進程的控制碼資料表中，但是您必須將控制碼值傳達給已建立的進程。 若要這麼做，您可以在呼叫 **CreateProcess** 時將值指定為命令列引數。 然後，建立的進程會使用 [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) 函式來抓取命令列字串，並將控制碼引數轉換成可用的控制碼。 如需詳細資訊，請參閱[繼承](../procthread/inheritance.md)。

 

 
