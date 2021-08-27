---
title: 非同步呼叫期間的用戶端安全性
description: 非同步呼叫期間的用戶端安全性
ms.assetid: 26d1f2c2-cb08-49f1-8beb-b99b029f0d8c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c4c25e17712d0164938f3de9895d1e6b02582f2d86cba9957297e23aa4e7f1c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071038"
---
# <a name="client-security-during-an-asynchronous-call"></a>非同步呼叫期間的用戶端安全性

MIDL 針對使用標準封送處理的物件所建立的 proxy 管理員會執行 [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) 介面。 用戶端可以藉由在呼叫物件上查詢 **IClientSecurity** ，以及取得或變更安全性設定，來管理封送呼叫的安全性。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[進行非同步呼叫](making-an-asynchronous-call.md)
</dt> </dl>

 

 




