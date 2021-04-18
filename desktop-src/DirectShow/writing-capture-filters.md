---
description: 寫入捕獲篩選器
ms.assetid: 7dfd1009-da09-49dc-a200-3d7a9f1c70c1
title: 寫入捕獲篩選器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de1a64de2b56dbc0728432307036fc46387f539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989458"
---
# <a name="writing-capture-filters"></a>寫入捕獲篩選器

不建議為 DirectShow 撰寫音訊或影片捕獲篩選。 相反地，DirectShow 會使用包裝函式篩選和 [系統裝置列舉](system-device-enumerator.md)值，為音訊和影片捕獲裝置提供自動支援。 如需有關如何執行設備磁碟機的詳細資訊，請參閱 Windows 驅動程式套件 (WDK) 檔。

這一節僅適用于需要從不尋常的硬體裝置捕獲某種自訂資料的開發人員。

本文包含下列各節：

-   [捕獲篩選準則的 Pin 需求](pin-requirements-for-capture-filters.md)
-   [ (選用) 來執行預覽 Pin ](implementing-a-preview-pin--optional.md)
-   [在 Capture 篩選器中產生資料](producing-data-in-a-capture-filter.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[撰寫 DirectShow 篩選器](writing-directshow-filters.md)
</dt> </dl>

 

 



