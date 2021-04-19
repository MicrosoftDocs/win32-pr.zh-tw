---
title: 控制項中的鍵盤處理
description: 控制項中的鍵盤處理
ms.assetid: 33affb3f-5d52-4ada-9751-0775b31a375e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f32610732ddbf88c6a587d5bc0fd7de1188152d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969485"
---
# <a name="keyboard-handling-in-controls"></a>控制項中的鍵盤處理

強烈建議您針對下列功能支援鍵盤處理，雖然它無法辨識到所有容器都適用。

-   支援 OLEMISC \_ ACTSLIKELABEL 和 OLEMISC \_ ACTSLIKEBUTTON 狀態位。
-   執行 DisplayAsDefault 環境屬性 (如果存在，就會傳回 **FALSE**) 。
-   執行索引標籤處理，包括定位順序。

某些容器將在傳統複合檔案案例中使用 ActiveX 控制項。 例如，試算表可能允許使用者將 ActiveX 控制項內嵌到工作表中。 在這種情況下，容器會以不同的方式進行鍵盤處理，因為鍵盤介面應該與使用者對試算表的期望保持一致。 這類產品的檔應該會通知使用者這些不同案例中的控制處理差異。 其他容器應努力正確地接受上述功能，包括助憶鍵處理。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[容器](containers.md)
</dt> </dl>

 

 




