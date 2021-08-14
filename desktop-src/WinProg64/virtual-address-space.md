---
title: 64位 Windows) 的虛擬位址空間 (程式設計指南
description: 根據預設，64位的 Microsoft Windows 架構應用程式具有數 tb 的使用者模式位址空間。
ms.assetid: c5c4af39-727e-46e1-821e-8342c555bf4c
keywords:
- 64位 Windows 程式設計指南64位 Windows 程式設計，虛擬位址空間
- 虛擬位址空間 64-位 Windows 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb2e673befb66c45501558effb37f3d04ee1a99199010f8cca89abb2cb31c6d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113368"
---
# <a name="virtual-address-space-programming-guide-for-64-bit-windows"></a>64位 Windows) 的虛擬位址空間 (程式設計指南

根據預設，64位的 Microsoft Windows 架構應用程式具有數 tb 的使用者模式位址空間。 如需精確的值，請參閱[Windows 和 Windows 伺服器版本的記憶體限制](/windows/desktop/Memory/memory-limits-for-windows-releases)。 不過，應用程式可以指定系統應配置低於 2 gb 的應用程式記憶體。 如果下列條件成立，則這項功能對64位應用程式很有説明：

-   2 GB 的位址空間已足夠。
-   程式碼有許多指標截斷警告。
-   指標和整數可任意混合。
-   程式碼具有使用32位資料類型的多型。

所有指標仍然是64位指標，但系統可確保每個記憶體配置都會低於 2 GB 的限制，因此，如果應用程式截斷指標，則不會遺失任何重要資料。 指標可以截斷為32位值，然後藉由符號延伸或零延伸來延伸至64位值。

若要指定此記憶體限制，請使用 **/LARGEADDRESSAWARE： NO** 連結器選項。 請注意，ARM64 二進位檔會忽略 **/LARGEADDRESSAWARE： NO** 。 不過，請注意，使用此選項時可能會發生問題。 如果您建立的 DLL 會使用這個選項，而且 DLL 是由未使用此選項的應用程式所呼叫，DLL 可能會截斷32位較高的64位指標。 這可能會導致應用程式失敗，而不會出現任何警告。

 

 
