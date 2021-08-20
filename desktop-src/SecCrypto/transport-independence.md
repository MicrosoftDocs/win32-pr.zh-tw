---
description: 憑證可以透過任何傳輸機制來要求和散發。
ms.assetid: 2cbd0cdb-eefa-4434-893d-20e8b34f4cfe
title: 傳輸獨立性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e7e54ce663bbf4b79b87de45f4882ac3044554bdc0860429166fc111c2bd8a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117971883"
---
# <a name="transport-independence"></a>傳輸獨立性

憑證可以透過任何傳輸機制來要求和散發。 憑證服務會透過 HTTP、DCOM、RPC、磁片檔案或自訂傳輸，接受來自申請者的 [*憑證要求*](../secgloss/c-gly.md) 。 憑證服務會透過 HTTP、DCOM、RPC、磁片檔案或自訂傳輸，將憑證張貼到申請者。

中繼應用程式和結束模組 Dll 都支援傳輸，通常是以 C/c + + 撰寫。 中繼應用程式和結束模組會隔離憑證服務功能，而不是與任何特定傳輸通訊。

 

 
