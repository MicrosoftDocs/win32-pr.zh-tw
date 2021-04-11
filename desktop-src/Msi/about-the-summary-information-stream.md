---
description: 摘要資訊資料流程包含可透過 Microsoft Windows 檔案總管查看之封裝的相關資訊。
ms.assetid: b909955f-ddd6-4cf1-8e86-fcf89be80b41
title: 關於摘要資訊資料流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ab931d7f9b6dd726fc6df3d7b805f4cc5c25caa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115393"
---
# <a name="about-the-summary-information-stream"></a>關於摘要資訊資料流程

摘要資訊資料流程包含可透過 Microsoft Windows 檔案總管查看之封裝的相關資訊。 這項資訊可透過 **IStream** 介面進行存取。 這是由作者提供，以提供每個屬性的值。

摘要資訊資料流程會使用 COM 來提供資料庫的結構化儲存體。 COM 支援透過 **IStream** 介面存取結構化儲存體的概念。 結構化儲存體可支援屬性集的概念，做為將幾乎任何資訊序列化的彈性方法。 COM 規格定義了單一標準屬性集，也就是用來填入可從 Windows 檔案總管查看的屬性工作表的摘要資訊。 因此，當使用者以滑鼠右鍵按一下安裝程式資料庫或轉換，然後選取 [ [屬性](about-properties.md)] 時，就可以看到儲存在摘要資訊資料流程中的資訊。

如需摘要屬性集的清單，請參閱 [摘要資訊資料流程屬性集](summary-information-stream-property-set.md)。

如需與資料庫、轉換和修補程式搭配使用之摘要資訊屬性的簡短說明，請參閱 [摘要屬性描述](summary-property-descriptions.md)。

 

 



