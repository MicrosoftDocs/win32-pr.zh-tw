---
description: WMI 提供者通常是設計來提供單一電腦上特定受管理物件的相關資訊。
ms.assetid: 9f23d599-ac37-4bfb-a3dc-0cef67e68b05
ms.tgt_platform: multiple
title: 將類別連結在一起
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89c36956d20d9390462577332e7ac7b644d4ffc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984237"
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

 

 



