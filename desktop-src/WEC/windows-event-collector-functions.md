---
title: Windows 事件收集器函式
description: 下列清單簡要說明 Windows 事件收集器中使用的函數。
ms.assetid: 48155df6-ba9c-4abe-ba84-6190cee95878
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c20e3bbee6226d385681c7471bb7fd3f337dfa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300028"
---
# <a name="windows-event-collector-functions"></a>Windows 事件收集器函式

下列清單簡要說明 Windows 事件收集器中使用的函數。

## <a name="in-this-section"></a>本節內容

<dl> <dt>

[**EcClose**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose)
</dt> <dd>

關閉從其他事件收集器函數接收的控制碼。

</dd> <dt>

[**EcDeleteSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecdeletesubscription)
</dt> <dd>

刪除現有的訂閱。

</dd> <dt>

[**EcEnumNextSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecenumnextsubscription)
</dt> <dd>

繼續列舉在本機電腦上註冊的訂閱。

</dd> <dt>

[**EcGetObjectArrayProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetobjectarrayproperty)
</dt> <dd>

抓取訂用帳戶之事件來源的屬性值。

</dd> <dt>

[**EcGetObjectArraySize**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetobjectarraysize)
</dt> <dd>

抓取訂用帳戶之事件來源的屬性值陣列的索引數目。

</dd> <dt>

[**EcGetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty)
</dt> <dd>

從訂用帳戶物件中抓取屬性值。

</dd> <dt>

[**EcGetSubscriptionRunTimeStatus**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionruntimestatus)
</dt> <dd>

抓取訂用帳戶或訂用帳戶本身之事件來源的執行時間狀態資訊。

</dd> <dt>

[**EcInsertObjectArrayElement**](/windows/desktop/api/Evcoll/nf-evcoll-ecinsertobjectarrayelement)
</dt> <dd>

將空的物件插入至訂用帳戶之事件來源的屬性值陣列中。

</dd> <dt>

[**EcOpenSubscriptionEnum**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscriptionenum)
</dt> <dd>

建立訂閱列舉值，以列舉本機電腦上所有已註冊的訂閱。

</dd> <dt>

[**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription)
</dt> <dd>

開啟現有的訂用帳戶，或建立新的訂用帳戶。

</dd> <dt>

[**EcSaveSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription)
</dt> <dd>

儲存訂用帳戶設定資訊。

</dd> <dt>

[**EcSetObjectArrayProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecsetobjectarrayproperty)
</dt> <dd>

針對訂用帳戶的事件來源，設定屬性值陣列中的屬性值。

</dd> <dt>

[**EcSetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecsetsubscriptionproperty)
</dt> <dd>

設定新值或更新訂用帳戶的現有值。

</dd> <dt>

[**EcRemoveObjectArrayElement**](/windows/desktop/api/Evcoll/nf-evcoll-ecremoveobjectarrayelement)
</dt> <dd>

從包含訂用帳戶之事件來源屬性值的物件陣列中移除元素。

</dd> <dt>

[**EcRetrySubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecretrysubscription)
</dt> <dd>

重試連接到未連接之訂用帳戶的事件來源。

</dd> </dl>

 

 




