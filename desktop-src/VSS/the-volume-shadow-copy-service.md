---
description: 磁碟區陰影複製服務 (VSS) 提供系統基礎結構，以便在 Windows 系統上執行 VSS 應用程式。
ms.assetid: 237b2729-1e9b-4d0e-9c59-990e047a0360
title: 磁碟區陰影複製服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 274e1e561b702dc2e69782fa5e9c2b47e6ea6a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690479"
---
# <a name="the-volume-shadow-copy-service"></a>磁碟區陰影複製服務

磁碟區陰影複製服務 (VSS) 提供系統基礎結構，以便在 Windows 系統上執行 VSS 應用程式。

雖然對使用者和開發人員來說大多是透明的，但 VSS 會執行下列動作：

-   在建立和使用陰影複製時，協調提供者、寫入器和要求者的活動
-   提供預設系統提供者
-   實行任何提供者所需的低層級驅動程式功能

VSS 服務會視需要啟動；因此，若要讓 VSS 作業成功，必須啟用此服務。

 

 



