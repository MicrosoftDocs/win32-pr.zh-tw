---
description: 16位所提供的印表機轉義 Windows 允許存取特殊裝置功能。
ms.assetid: 4bdd1d47-8cf4-4088-aec8-88193e71a828
title: 印表機轉義
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dd8bc842e60ca0019fc523b27a4657e66a623cda4802bfdb489213b694fd432
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119711558"
---
# <a name="printer-escapes"></a>印表機轉義

16位所提供的印表機轉義 Windows 允許存取特殊裝置功能。 大部分的這些轉義已淘汰，但有幾個可簡化16位 Windows 應用程式的移植。 GDI 支援一組完整的路徑函式，可讓應用程式使用，而不是使用 esc 鍵在任何裝置上繪製路徑。 如需取代部分轉義的函式清單，請參閱 [**Escape**](/windows/desktop/api/Wingdi/nf-wingdi-escape) 函數。

在64原始印表機的轉義中，只能使用 **QUERYESCSUPPORT** 和 **傳遞** 。

另外還有一個稱為 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)的延伸 escape 函數。 此函式可讓應用程式存取特定裝置的功能，而不是透過 GDI 直接提供。

 

 



