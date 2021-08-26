---
title: 容器控制項
description: 容器控制項
ms.assetid: 4fa59272-54b6-4da9-a7f5-e1b4eab7fa80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82048c02c6aa1db020a030f9a5a2fc92f0c5fc08914c930a315a97b31a88c120
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896438"
---
# <a name="container-controls"></a>容器控制項

如上所述，容器控制項是以視覺方式包含其他控制項的 ActiveX 控制項。 ActiveX controls 架構會指定要啟用容器控制項的 [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)介面。 雖然無法保證行為，但容器也可支援容器控制項，但不支援 **ISimpleFrameSite**。 基於這個理由，SimpleFrameSite 控制項的元件類別是必要的，因此需要此介面的完整功能。

若要在不執行 [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)的情況下支援容器控制項，ActiveX 控制容器必須：

-   隨時啟動所有控制項。
-   將包含的控制項重設為包含控制項的 hWnd。
-   維持容器控制項的父系。

 

 




