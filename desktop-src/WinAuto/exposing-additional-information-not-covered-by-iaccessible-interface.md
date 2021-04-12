---
title: 公開 IAccessible 介面未涵蓋的其他資訊
description: 根據其產品而定，除了 Microsoft Active Accessibility 支援之外，伺服器開發人員可能還需要公開資訊或功能。
ms.assetid: c45009ca-6be3-4645-9097-36671a41dfce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3834c60de8f18fd5ec0719919a1cd79e22f451e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316027"
---
# <a name="exposing-additional-information-not-covered-by-iaccessible-interface"></a>公開 IAccessible 介面未涵蓋的其他資訊

根據其產品而定，除了 Microsoft Active Accessibility 支援之外，伺服器開發人員可能還需要公開資訊或功能。 如果是這種情況，請與 (用戶端) 的輔助技術廠商合作，以確保他們新增功能的支援。

請勿嘗試擴充 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面。 一旦發行介面之後，就無法變更它們。 若要公開其他資訊，請使用自訂介面，並使用下列其中一種技術來公開它：

-   [使用 OBJID \_ NATIVEOM 來公開視窗的原生物件模型介面](using-objid-nativeom-to-expose-a-native-object-model-interface-for-a-window.md)
-   [使用 QueryService 公開 IAccessible 物件的原生物件模型介面](using-queryservice-to-expose-a-native-object-model-interface-for-an-iaccessible-object.md)

請注意， [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面的目標是要有伺服器和用戶端所使用的妥善定義介面。 公開自訂介面之前，請務必透過 **IAccessible** 公開盡可能多的資訊。

您無法使用 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 來公開自訂介面。 使用 **IServiceProvider：： QueryService** ，如下列程式所述。

 

 