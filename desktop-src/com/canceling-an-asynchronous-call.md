---
title: 取消非同步呼叫
description: 如果呼叫物件實 ICancelMethodCalls 介面，用戶端可以取消正在進行中的非同步呼叫。
ms.assetid: 30a162f2-ce16-4ee6-8002-59216ac0e59a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42d2751400d631c62c19f68f2cab841c0845b432df676abe60befed1f231e103
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737112"
---
# <a name="canceling-an-asynchronous-call"></a>取消非同步呼叫

如果呼叫物件實 [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) 介面，用戶端可以取消正在進行中的非同步呼叫。 針對使用標準封送處理的物件， **ICancelMethodCalls** 一律可用於封送處理呼叫。 針對使用自訂封送處理的物件，或對相同單元內的伺服器物件進行呼叫的物件，只有在呼叫物件執行 **ICancelMethodCalls** 時，才能使用此功能。

用戶端可以隨時取消呼叫，從 \_ 呼叫 Begin 方法到完成方法傳回為止 \_ 。 如果用戶端在呼叫完成方法之前取消呼叫 \_ ，則必須呼叫完成 \_ 方法來清除呼叫物件的狀態。 在用戶端完成之前，呼叫物件上任何 Begin 方法的任何呼叫 \_ 都會傳回 \_ 擱置中的 RPC E \_ 呼叫 \_ 。

**取消非同步呼叫**

1.  查詢 [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls)的呼叫物件。

2.  呼叫 [**ICancelMethodCalls：： Cancel**](/windows/win32/api/objidlbase/nf-objidlbase-icancelmethodcalls-cancel)，然後呼叫 [**release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 以釋放步驟1中 [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) 呼叫所取得的指標。

3.  如果用戶端尚未 \_ 呼叫完成方法，請立即呼叫。

不保證伺服器實際上已停止執行呼叫。 如果用戶端的進一步工作取決於呼叫可能或未變更的某些伺服器狀態，用戶端應該在繼續之前判斷該狀態。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[進行非同步呼叫](making-an-asynchronous-call.md)
</dt> </dl>

 

 