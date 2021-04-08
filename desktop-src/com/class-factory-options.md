---
title: Class Factory 選項
description: Class Factory 選項
ms.assetid: e9e33e07-7628-4c5e-965d-e12a9c1d69c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fab52ea11a0e7e20d10757eb8d6e86577afc35c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683140"
---
# <a name="class-factory-options"></a>Class Factory 選項

ActiveX 控制項（藉由使用 COM 物件）必須有相關聯的伺服器程式碼，以支援透過 [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) 來建立控制項的最小值。

這是選擇性的（非必要），此類別物件也支援 [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) 以進行授權管理。 只有在意授權的廠商才需要支援 COM 的授權機制。 換句話說，因為 **IClassFactory2** 是達成 COM 層級授權的唯一方法，所以在需要授權的控制項的類別物件上需要這個介面。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[控制項](controls.md)
</dt> </dl>

 

 