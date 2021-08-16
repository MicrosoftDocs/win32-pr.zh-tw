---
description: 會話重新導向可讓應用程式在不接聽來電的情況下，將提供的會話轉移到另一個位址。
ms.assetid: b52cd5c2-fdd6-4240-b07b-b22733a89d27
title: 重新導向
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ea44aaa10bc174784822032359d68d24ba01b6f7f1dcdf0fb211554107b8b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761202"
---
# <a name="redirect"></a>重新導向

會話重新導向可讓應用程式在不接聽來電的情況下，將提供的會話轉移到另一個位址。 應用程式可以依呼叫逐一執行重新導向。 例如，應用程式可能會允許使用者根據呼叫者識別碼資訊指定不同的重新導向。 成功重新導向呼叫之後，狀態通常會轉換成閒置，而且必須釋放相關聯的資源。

重新導向與 [轉寄](forward-ovr.md) 不同之處在于，在設定轉送之後，此作業會由 TAPI、服務提供者或交換器執行，而不需要進一步參與應用程式。 重新導向與 [傳輸](transfer-ovr.md) 不同，因為重新導向不需要先接聽呼叫。

並非所有服務提供者都支援使用這項作業。

**TAPI 2.x：** 請參閱 [**lineRedirect**](/windows/win32/api/tapi/nf-tapi-lineredirect)。

 

 
