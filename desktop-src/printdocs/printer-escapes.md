---
description: 16位 Windows 所提供的印表機轉義允許存取特殊裝置功能。
ms.assetid: 4bdd1d47-8cf4-4088-aec8-88193e71a828
title: 印表機轉義
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59463c4201e97c5ac1ec689a772581fab28314b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193375"
---
# <a name="printer-escapes"></a>印表機轉義

16位 Windows 所提供的印表機轉義允許存取特殊裝置功能。 這些轉義大部分都已過時，但有幾個是為了簡化16位 Windows 應用程式的移植而提供。 GDI 支援一組完整的路徑函式，可讓應用程式使用，而不是使用 esc 鍵在任何裝置上繪製路徑。 如需取代部分轉義的函式清單，請參閱 [**Escape**](/windows/desktop/api/Wingdi/nf-wingdi-escape) 函數。

在64原始印表機的轉義中，只能使用 **QUERYESCSUPPORT** 和 **傳遞** 。

另外還有一個稱為 [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape)的延伸 escape 函數。 此函式可讓應用程式存取特定裝置的功能，而不是透過 GDI 直接提供。

 

 



