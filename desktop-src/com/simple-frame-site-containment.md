---
title: 簡易框架網站內含專案
description: 簡易框架網站內含專案
ms.assetid: 85c3565f-f557-43af-8d36-58414d0790cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d356d6cc4993702ac571a800ad2abbfe378e8a8fe06ddc80225d81f0fe21a36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129852"
---
# <a name="simple-frame-site-containment"></a>簡易框架網站內含專案

容器控制項是可以包含其他控制項的 ActiveX 控制項。 包含選項按鈕集合的群組方塊是容器控制項的範例。 容器控制項應設定 OLEMISC \_ SIMPLEFRAME 狀態位，而且應該呼叫其容器的 [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) 執行。 支援容器控制項的 ActiveX 控制項容器必須執行 **ISimpleFrameSite**。

CATID-{157083E0-2368-11cf-87B9-00AA006C8166} CATID \_ SimpleFrameControl

## <a name="related-topics"></a>相關主題

<dl> <dt>

[元件類別](component-categories.md)
</dt> </dl>

 

 




