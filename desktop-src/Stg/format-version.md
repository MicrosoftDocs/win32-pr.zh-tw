---
title: 格式版本
description: 格式版本值是用來指出此資料流程格式版本的文字資料類型。
ms.assetid: 38362a45-4f49-4a85-aabe-452ff32c2812
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 503019a3bfe3224e4137ac3bfd43fadbe1e15a3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104507984"
---
# <a name="format-version"></a>格式版本

格式版本值是用來指出此資料流程格式版本的 **文字** 資料類型。 它可能是零或一。 讀取屬性集時，應該檢查格式版本指標。 如果不是零或1，則資料流程會寫入至不同的規格，而且無法由根據此規格開發的程式碼讀取。

格式為第1版的屬性集會相當於版本0，具有下列新增專案：

-   區分 **大小寫的屬性名稱**。 屬性名稱會儲存在保留的字典屬性（ [PROPERTY ID 0](/windows/desktop/Stg/reserved-property-identifiers)）中。 在第1版的屬性集中，這些名稱可能會區分大小寫。 區分大小寫是由保留行為屬性（ [PROPERTY ID 0x80000003](/windows/desktop/Stg/reserved-property-identifiers)）所決定。
-   **長屬性名稱**。 與版本0屬性集不同的第1版屬性集不受限於屬性名稱的長度。 如需屬性名稱的詳細資訊，請參閱 [屬性識別碼 0](/windows/desktop/Stg/reserved-property-identifiers) 。
-   **屬性類型**。 第1版屬性集可以保留所有可保存在版本0屬性集中的屬性類型，再加上一些其他類型。 如需這些類型的詳細資訊，請參閱 [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 結構。

 

 