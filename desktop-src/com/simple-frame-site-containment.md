---
title: 簡易框架網站內含專案
description: 簡易框架網站內含專案
ms.assetid: 85c3565f-f557-43af-8d36-58414d0790cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0106bc88d9f69f380590e808741e0b1a0bdc2f1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932067"
---
# <a name="simple-frame-site-containment"></a>簡易框架網站內含專案

容器控制項是可以包含其他控制項的 ActiveX 控制項。 包含選項按鈕集合的群組方塊是容器控制項的範例。 容器控制項應設定 OLEMISC \_ SIMPLEFRAME 狀態位，而且應該呼叫其容器的 [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) 執行。 支援容器控制項的 ActiveX 控制項容器必須執行 **ISimpleFrameSite**。

CATID-{157083E0-2368-11cf-87B9-00AA006C8166} CATID \_ SimpleFrameControl

## <a name="related-topics"></a>相關主題

<dl> <dt>

[元件類別](component-categories.md)
</dt> </dl>

 

 




