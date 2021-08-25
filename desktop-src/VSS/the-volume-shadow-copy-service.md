---
description: 磁碟區陰影複製服務 (VSS) 提供系統基礎結構，以便在 Windows 型系統上執行 VSS 應用程式。
ms.assetid: 237b2729-1e9b-4d0e-9c59-990e047a0360
title: 磁碟區陰影複製服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f71e21ba0f20eaa0f3723cd0da6cb3efb89bae027678d154ab8b5b5568532ac8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866238"
---
# <a name="the-volume-shadow-copy-service"></a>磁碟區陰影複製服務

磁碟區陰影複製服務 (VSS) 提供系統基礎結構，以便在 Windows 型系統上執行 VSS 應用程式。

雖然對使用者和開發人員來說大多是透明的，但 VSS 會執行下列動作：

-   在建立和使用陰影複製時，協調提供者、寫入器和要求者的活動
-   提供預設系統提供者
-   實行任何提供者所需的低層級驅動程式功能

VSS 服務會視需要啟動；因此，若要讓 VSS 作業成功，必須啟用此服務。

 

 



