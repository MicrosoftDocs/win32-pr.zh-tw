---
description: 沒有元件的 COM + 服務
ms.assetid: 5ef67411-334b-476e-b9b7-3677b24ab7df
title: 沒有元件的 COM + 服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b395186875c37fb42e5011ee0486aa6de86ffe62b73c8ea1a54c09e82a27c588
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119638448"
---
# <a name="com-services-without-components"></a>沒有元件的 COM + 服務

使用 COM + 1.5，您可以使用 COM + 所提供的服務，而不需要建立元件來包含呼叫這些服務的方法。 這可大幅獲益于通常不使用元件，但想要使用 COM + 服務（例如交易或 COM + 追蹤器）的開發人員。 藉由使用沒有元件的 COM + 服務，開發人員可以避免建立元件的額外負荷，而此元件只會用來存取所需的 COM + 服務。

例如，腳本環境傳統上是 COM + 服務的最大取用者，但因為服務需要在 COM + 元件內配套，所以永遠不能有效率地使用這些服務。 這項組合需求會提高效能成本，因為腳本環境所需的資料的通訊和重復資料也會與元件互動。 使用沒有元件的服務，就會將這類成本降至最低。

下表所述的主題提供有關使用 COM + 服務而不含元件的背景和工作資訊。 這項功能適用于關心效能的 advanced Visual C++ 開發人員。



| 主題                                                                                                 | 描述                                                                                    |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [沒有元件概念的 COM + 服務](com--services-without-components-concepts.md)<br/> | 概要說明如何使用不含元件的 COM + 服務。<br/>                     |
| [沒有元件工作的 COM + 服務](com--services-without-components-tasks.md)<br/>       | 提供指示，說明如何使用 COM + 來建立及使用不含元件的服務。<br/> |



 

 

 




