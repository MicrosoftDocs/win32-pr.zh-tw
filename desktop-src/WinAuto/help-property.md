---
title: Help 屬性
description: Help 屬性提供的資訊會告訴使用者物件的功能。
ms.assetid: 3df0cc01-cc99-42a1-9d56-591e6e00e53d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b240475d4583826e08fd6ee43b5839bdfb451d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300740"
---
# <a name="help-property"></a>Help 屬性

**Help** 屬性提供的資訊會告訴使用者物件的功能。

藉由呼叫 [**IAccessible：： get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)，即可抓取 **Help** 屬性。

此屬性包含氣球樣式資訊 (如工具提示) 中所示，可用來描述物件的用途或使用方式。 例如，顯示印表機 **的工具列按鈕的 [說明** ] 屬性可能會提供下列文字：「列印目前的檔」。

**Help** 屬性的文字在使用者介面中不一定是唯一的。

## <a name="when-to-support-the-help-property"></a>何時支援 Help 屬性

如果其他屬性提供物件用途的足夠資訊，以及物件執行的動作，則伺服器不支援 [說明 **] 屬性。** 公開系統提供之控制項的可存取物件不支援 **Help** 屬性。

 

 




