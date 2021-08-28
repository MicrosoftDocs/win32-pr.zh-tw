---
description: 64位封裝包含部分或全部64位 Windows Installer 元件。
ms.assetid: 615a5534-7c9e-4240-9a23-35f224122d0e
title: 64位 Windows Installer 套件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 540ef7afc5c70eeba2bb24eb376eae8e52b8e55cec2c8622ccdcf18a804b6f91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119559538"
---
# <a name="64-bit-windows-installer-packages"></a>64位 Windows Installer 套件

64位封裝包含部分或全部64位[Windows Installer](windows-installer-components.md)元件。 下列清單會識別每個64位 Windows Installer 套件的需求：

-   只有當封裝在 Intel64 (Itanium) 處理器上執行時，才必須在 [ [**範本摘要**](template-summary.md) ] 屬性的 [平臺] 欄位中輸入 "Intel64" 值。
-   只有當封裝在 x64 處理器上執行時，才必須在 [ [**範本摘要**](template-summary.md) ] 屬性的 [平臺] 欄位中輸入值 "x64"。
-   只有當封裝在 Arm64 處理器上執行時，才必須在 [**範本摘要**](template-summary.md) 屬性的 [platform] 欄位中輸入 "Arm64" 值。
-   [[**頁面計數摘要**](page-count-summary.md)] 屬性必須設定為整數200或更大，因為 Windows Installer 2.0 是能夠安裝64位元件的最小版本。 Arm64 平臺的套件需要500或更高的值。
-   封裝中的每個64位 Windows Installer 元件都必須在 [元件資料表](component-table.md)的 [屬性] 資料行中包含 **msidbComponentAttributes64bit** 位。

如需詳細資訊，請參閱[64 位作業系統上的 Windows Installer](windows-installer-on-64-bit-operating-systems.md)和[32 位 Windows Installer 套件](32-bit-windows-installer-packages.md)。

 

 



