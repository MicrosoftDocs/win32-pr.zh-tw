---
description: 在某些環境中，使用者並不會自動收到供應專案來電的警示，例如透過響鈴或透過其電腦螢幕上的訊息。
ms.assetid: 50684e2a-0799-458b-9402-0958e35026d7
title: 接受
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1240159d1b4b7b8e3e4f2fe58e666e8625d3eee81ab38651f8d98c93d22b20ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118872699"
---
# <a name="accept"></a>接受

在某些環境中，使用者並不會自動收到供應專案來電的警示，例如透過響鈴或透過其電腦螢幕上的訊息。 接受作業會開始發出警示的程式， (通常會響鈴) ，而 [回應](answer-ovr.md) 作業會在之後進行。 應用程式可能會卸載會話 [、將它](drop-ovr.md) 重新 [導向](redirect-ovr.md) 或接受。

如果目前的服務提供者支援，則應用程式可以選擇在接受時傳送使用者的資訊。 不保證網路會將這項資訊傳遞給呼叫方。

並非所有服務提供者都支援使用這項作業。

**TAPI 2.x：** 請參閱 [**lineAccept**](/windows/win32/api/tapi/nf-tapi-lineaccept)。

 

 
