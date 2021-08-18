---
description: WMI 提供者通常是設計來提供單一電腦上特定受管理物件的相關資訊。
ms.assetid: 9f23d599-ac37-4bfb-a3dc-0cef67e68b05
ms.tgt_platform: multiple
title: 將類別連結在一起
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da48ab6b816eece1184915026ca32ed152b896f0555ca6c546d0b8ed4d6a7640
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131220"
---
# <a name="linking-classes-together"></a>將類別連結在一起

WMI 提供者通常是設計來提供單一電腦上特定受管理物件的相關資訊。 如果有一個通用屬性可作為索引鍵來唯一識別所有不同的來源實例，則請使用 [View 提供者](view-provider.md) 將不同類別、命名空間或電腦的屬性合併為單一類別。

您必須先 [註冊 View Provider](registering-the-view-provider.md)。 註冊之後，您可以建立下列類型的 view 類別：

-   [聯結視圖](creating-a-new-instance-from-old-properties.md)

    由通用屬性值連接之不同類別的實例。

-   [相關檢視](associating-instances-between-namespaces.md)

    跨命名空間界限的現有關聯類別的視圖。

-   [聯集視圖](creating-a-union-view-class.md)

    一或多個實例的聯集。

 

 



