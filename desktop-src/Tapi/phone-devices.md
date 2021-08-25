---
description: 電話的裝置支援是互補的，而不是基本的，因此服務提供者不需要支援電話裝置。
ms.assetid: 4d9f3b32-20d0-4550-9b3d-db97df8ea289
title: 電話設備
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d11aa269e17d74fbaf74c701c954ced734ef33900198a7c9e30a044f5ebd32e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873278"
---
# <a name="phone-devices"></a>電話設備

電話的裝置支援是互補的，而不是基本的，因此服務提供者不需要支援電話裝置。

就像線路裝置類別是實體線路裝置的抽象概念，phone 裝置類別代表與裝置無關的電話組抽象概念。 TAPI 會將線路和電話裝置視為彼此獨立的裝置。 換句話說，您可以在不使用相關行的情況下，使用電話 (裝置) ，也可以在不使用電話的情況下使用線路 (裝置) 。

完全採用此獨立性的服務提供者可提供這些裝置的使用，這些裝置不是由傳統的電話語音通訊協定所定義。 例如，使用者可以使用桌上型電腦電話的話筒作為語音錄製或播放的波形音訊裝置，可能不會因為切換電話正在使用中而不知道。 在這種情況下，將本機電話聽筒不需要自動傳送 offhook 信號至交換器。

這種獨立性也可讓應用程式以與來電無關的方式來撥打局域電話。 服務提供者的功能受限於用來將交換器、電話和電腦互連的硬體和軟體功能。

TAPI 包含可取得裝置功能的函式，可讓用戶端判斷是否支援這類使用模型。

本節說明電話裝置，並說明如何使用 TAPI 電話功能來存取這些裝置。

-   [電話裝置](phone-device-elements.md)
-   [初始化和關閉](initialization-and-shutdown.md)

 

 



