---
description: 回應作業是應用程式對提供之通訊會話的典型回應。 如果成功，此作業會導致會話轉換為線上狀態。
ms.assetid: 34ac0b34-1d1b-4657-a737-27a4ed9326af
title: 回答
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e08081b32b7ba3a3a24cde3ec37c1a6118582cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513476"
---
# <a name="answer"></a>回答

回應作業是應用程式對提供之通訊會話的典型回應。 如果成功，此作業會導致會話轉換為線上狀態。

在某些電話語音環境中 (像是 ISDN) ，其中使用者警示與電話供應專案不同，因此應用程式可以選擇在接聽或 [拒絕 (卸載](drop-ovr.md)) 或重新 [導向](redirect-ovr.md)供應 *專案呼叫之前*[接受](accept-ovr.md)呼叫。

如果會話已在使用中時，針對新的會話執行回應作業，則對現有作用中會話的影響會視服務提供者的功能而定。 第一個呼叫可能不受影響，它可以自動卸載，也可以自動放置在保存上。 TAPI 會傳送關於這兩個呼叫的適當事件通知。

在橋接的情況下，如果呼叫已連線但處於作用中狀態，則可以使用「回應」操作來聯結。

如果服務提供者支援，則應用程式可以選擇在解答時傳送使用者資訊。

**TAPI 2.x：** 請參閱 [**lineAnswer**](/windows/win32/api/tapi/nf-tapi-lineanswer)。

**TAPI 3.x：** 請參閱 [**ITBasicCallControl：：解答**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-answer)。

 

 
