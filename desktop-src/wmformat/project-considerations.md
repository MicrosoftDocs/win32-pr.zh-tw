---
title: 專案考慮
description: 專案考慮
ms.assetid: aebe2886-0af0-443a-a5be-651f11936639
keywords:
- Windows Media Format SDK，專案考慮
- Advanced Systems Format (ASF) 、專案考慮
- ASF (Advanced Systems Format) ，專案考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1682e8008569c9b230b2c2f53f394326669d022
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104184059"
---
# <a name="project-considerations"></a>專案考慮

您必須確保終端使用者可以正確地執行您使用 Windows Media Format SDK 建立的應用程式。 本節說明散發應用程式、副檔名和軟體轉散發時，必須考慮的兩件事。

您必須針對使用您的應用程式所建立的任何檔案，使用正確的副檔名。 使用適當的副檔名，讓使用者更容易辨識 ASF 檔案，並在解碼檔案時防止混淆。

您必須提供執行應用程式所需的任何可轉散發套件。 如果沒有正確的可轉散發套件，使用者將無法使用您的應用程式。

下列各節詳細說明副檔名和軟體重新發佈。



| 區段                                                                      | 描述                                                                                                     |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [檔案名延伸指導方針](file-name-extension-guidelines.md)         | 提供有關您的程式所建立之 ASF 檔案所應使用之副檔名的資訊。     |
| [軟體轉散發](software-redistribution.md)                       | 說明 Windows Media Format SDK 的可轉散發套件，以及如何將它們包含在您的應用程式中。 |
| [註冊應用程式相依性](registering-application-dependency.md) | 說明如何註冊您的應用程式，使其相依于 Windows Media Format SDK 執行時間。          |



 

 

 




