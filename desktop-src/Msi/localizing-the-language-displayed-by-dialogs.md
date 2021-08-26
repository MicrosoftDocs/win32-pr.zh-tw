---
description: Windows Installer 服務會在所有對話方塊中使用目前使用者的語言，直到開啟 Windows Installer 封裝為止。
ms.assetid: c9902990-7a26-48fd-96ac-4d5a749e34be
title: 將對話方塊所顯示的語言當地語系化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72142ce0f479379ebc929807294e6bbab7699738ee41e70be87e8e65f57c1ea3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043178"
---
# <a name="localizing-the-language-displayed-by-dialogs"></a>將對話方塊所顯示的語言當地語系化

Windows Installer 服務會在所有對話方塊中使用目前使用者的語言，直到開啟 Windows Installer 封裝為止。 Windows Installer 使用 **GetUserDefaultUILanguage** 來決定這一點。 開啟 Windows Installer 套件時，安裝程式會使用 [[**範本摘要**](template-summary.md)] 屬性所指定的封裝語言來顯示對話方塊。

如需當地語系化 Windows Installer 套件語言的詳細資訊，另請參閱[當地語系化範例](a-localization-example.md)。

 

 



