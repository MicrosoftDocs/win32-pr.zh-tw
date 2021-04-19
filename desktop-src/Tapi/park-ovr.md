---
description: 公園作業可讓應用程式將會話傳送至特殊位址，在此位址將會保留到已離開為止。
ms.assetid: 6a82f03e-d8fd-4d0b-8f5d-f7934ba86759
title: 公園
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aded4657a9d337d6d9c663622a5359856e964b90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988823"
---
# <a name="park"></a>公園

公園作業可讓應用程式將會話傳送至特殊位址，在此位址將會保留到已離開為止。 從應用程式的觀點來看，這看起來很像是傳輸。 在連接另一端的合作物件中，這類似于保留。

停車場和轉移之間的差異在於，暫停的位址不是會話的連接點，而會話不會發出警示或超時。停車場與保存之間的差異在於，當公園作業完成時，會話將不再與應用程式的位址相關聯。

提供兩種形式的停車會話： *導向公園* 和 *nondirected 公園*。 在「導向通話」中，應用程式會指定要暫停呼叫的目的地位址。 使用 nondirected 公園時，服務提供者或基礎硬體會決定位址，並將其傳回給應用程式。

已暫停的會話通常會在成功暫停之後進入閒置狀態，然後應用程式應該釋放與其相關聯的資源。 如需如何進行這項作業的摘要，請參閱 [終止會話](terminate-a-session-ovr.md) 。

如果應用程式 unparks 會話，即使應用程式傳回先前的指標，也會配置新的會話資源，因此無法進行適當的發行可能會導致各種問題。

某些服務提供者可以在會話暫停一段很長的時間之後，提醒使用者。 應用程式會看到呼叫 [原因](reason-ovr.md) 設定為提醒的供應專案通話。

並非所有服務提供者都支援使用這項作業。

**TAPI 2.x：** 請參閱 [**linePark**](/windows/win32/api/tapi/nf-tapi-linepark)、 [**lineUnpark**](/windows/win32/api/tapi/nf-tapi-lineunpark)。

**TAPI 3：** 請參閱 [**ITBasicCallControl：:P arkdirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkdirect)、 [**ITBasicCallControl：:P arkindirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkindirect)、 [**ITBasicCallControl：： Unpark**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-unpark)。

 

 
