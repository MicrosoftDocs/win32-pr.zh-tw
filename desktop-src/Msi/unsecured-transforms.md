---
description: 未受安全轉換所述保護的轉換預設為不安全的轉換。
ms.assetid: feace6c3-7828-44d0-8d2b-482a02e8e0c0
title: 不安全的轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6743898142197d87d4e3fef5d0f48778f6261ff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975546"
---
# <a name="unsecured-transforms"></a>不安全的轉換

未受安全 [轉換](secured-transforms.md) 所述保護的轉換預設為不安全的轉換。

若要在安裝封裝時套用不安全的轉換，請在 [ [**轉換**](transforms.md) ] 屬性或命令列字串中傳遞轉換檔名稱。 請勿以 @ 或字元開頭字串， \| 或設定 [TransformsSecure 原則](transformssecure-policy.md) 或 [**TransformsSecure**](transformssecure.md) 屬性。 請注意，您無法在相同的轉換清單中結合不安全的轉換和 [安全的轉換](secured-transforms.md) 。

如果封裝是在每個使用者 [安裝內容](installation-context.md)中安裝或通告，並且具有不安全的轉換，則安裝程式會將轉換來源儲存在使用者設定檔中的應用程式資料檔案夾。 這可讓使用者在電腦之間移動時，維護其產品的自訂。

如果封裝是在每部電腦 [安裝內容](installation-context.md)中安裝或通告，並且使用不安全的轉換，則安裝程式會將轉換來源儲存在% windir% \\ installer 資料夾中。

在第一次安裝封裝期間，安裝程式會先在 [**轉換**](transforms.md) 屬性或命令列字串所提供的來源搜尋轉換。 如果無法使用此來源，則安裝程式會在 .msi 檔案旁的封裝來源搜尋轉換。

在 [維護安裝](maintenance-installation.md)期間，安裝程式會在快取位置搜尋轉換。 如果無法使用轉換的快取副本，安裝程式會在 .msi 檔案旁的封裝來源搜尋轉換。

如需詳細資訊，請參閱套用 [轉換](applying-transforms.md) 和 [來源復原](source-resiliency.md)。

 

 



