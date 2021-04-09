---
description: 經過一段時間後，TAPI 應用程式、TAPI 和服務提供者可能會有不同的版本。
ms.assetid: 39b16328-931e-4d75-a6ec-1edc97f1a287
title: 版本交涉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beffff7ceeb90ccf419e138986562ca90f83c204
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945030"
---
# <a name="version-negotiation"></a>版本交涉

經過一段時間後，TAPI 應用程式、TAPI 和服務提供者可能會有不同的版本。 TAPI 應用程式的最佳互通性需要知道應用程式的 TAPI 版本，也需要知道 TAPI DLL、TAPISVR 和服務提供者版本。

無法進行適當的版本協商可能會導致嚴重的問題。 例如，某些大量使用的結構會將資料成員從某個版本新增至下一個版本。 如果結構大小不符合應用程式或 TAPI 預期的大小，則結果的範圍是從記憶體流失到間歇性的 AVs。

如需詳細資訊，請參閱 [TAPI 版本](./tapi-versioning.md)設定。

**TAPI 2.x：** 在 [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa)期間，應用程式會與 TAPI 和 TAPISVR 協調。 應用程式會針對應用程式可能會使用的每一行呼叫 [**lineNegotiateAPIVersion**](/windows/win32/api/tapi/nf-tapi-linenegotiateapiversion) ，以對服務提供者執行裝置的協商。

**TAPI 3.x：** 不需要執行版本協商;不過，您可以使用 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 來判斷介面是否可在其版本上使用。

 

 
