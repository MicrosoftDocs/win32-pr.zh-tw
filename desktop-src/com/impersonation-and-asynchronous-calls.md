---
title: 模擬和非同步呼叫
description: 模擬和非同步呼叫
ms.assetid: 7eaa0a66-7a80-4831-b0b6-b8eff4abd036
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0854946b619f7580173ffcbc97c9af3f2540361b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683202"
---
# <a name="impersonation-and-asynchronous-calls"></a>模擬和非同步呼叫

伺服器呼叫 [**ISynchronize：：信號**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal) 完成之後，伺服器無法模擬用戶端，即使 Begin \_ 方法尚未完成。 例如，假設用戶端呼叫 Begin \_ 方法，伺服器會立即處理呼叫，而伺服器會呼叫 **信號** 以表示它已完成處理。 即使工作仍在 Begin 方法中完成 \_ ，伺服器仍無法在呼叫 **信號** 完成之後模擬用戶端。

如果伺服器在呼叫 [**信號**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal)之前模擬用戶端，將不會從執行緒移除模擬權杖，直到伺服器呼叫 [**IServerSecurity：： RevertToSelf**](/windows/win32/api/objidlbase/nf-objidlbase-iserversecurity-reverttoself) 為止，或直到伺服器的呼叫開始傳回（以先達到者為 \_ 准）。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[委派和模擬](delegation-and-impersonation.md)
</dt> <dt>

[進行非同步呼叫](making-an-asynchronous-call.md)
</dt> </dl>

 

 