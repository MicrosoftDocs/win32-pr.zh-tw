---
title: MCI 命令字串和訊息
description: MCI 命令字串和訊息
ms.assetid: eb60c96b-e89e-4673-a8e0-98fabe4af7ca
keywords:
- MCI 命令字串，關於
- MCI 命令訊息，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107a317442280b8fb4c7afe7832205b1c7128513
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842300"
---
# <a name="mci-command-strings-and-messages"></a>MCI 命令字串和訊息

MCI 支援 [命令字串](command-strings.md) 和 [命令訊息](command-messages.md)。 您可以在 MCI 應用程式中使用字串或訊息，或兩者。

-   *命令訊息介面* 包含常數和結構。 使用 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函式，將訊息傳送至 MCI 裝置。
-   *命令字串介面* 提供命令訊息的文字版本。 使用 [**mciSendString**](/previous-versions//dd757161(v=vs.85)) 函式將字串傳送至 MCI 裝置。 命令字串會複製命令訊息的功能。 作業系統會先將命令字串轉換成命令訊息，然後再將它們傳送至 MCI 驅動程式進行處理。

取得資訊的命令訊息會以結構的形式來進行，在 C 應用程式中很容易解讀。 這些結構可以包含裝置許多不同層面的資訊。 取得資訊的命令字串會以字串形式來進行，而且一次只能取出一個字串。 您的應用程式必須剖析或測試每個字串才能加以解讀。 在某些情況下，您可能會發現命令訊息比命令字串更容易使用，但命令字串很容易記住和實行。 某些 MCI 應用程式會在傳回值不會使用時使用命令字串 (除了用來驗證從裝置取得資訊時的成功) 和命令訊息。

當您討論到命令時，此總覽會使用命令的字串形式，後面接著訊息格式（以括弧括住）。

 

 