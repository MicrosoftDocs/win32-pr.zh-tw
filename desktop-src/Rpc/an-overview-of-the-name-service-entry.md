---
title: 名稱服務專案的總覽
description: 名稱服務專案包含三個不同的區段。
ms.assetid: 3059a9a9-174d-4d04-8565-e4558f17f465
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2d7982cef018ec91435c647000031ae42a25e2e2bb315a20623ac75e610197e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073558"
---
# <a name="an-overview-of-the-name-service-entry"></a>名稱服務專案的總覽

名稱服務專案包含三個不同的區段。 第一個區段適用于 (UUID + version) 的介面，第二個區段包含物件 Uuid，第三個區段則用於系結控制碼。 您可以提供專案的名稱，以做為識別的方式。

當呼叫 [**RpcNsBindingExport**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta)時，伺服器會指定要在其中放置匯出資訊的專案名稱。 接著會將這個新匯出的介面新增至名稱服務專案的介面區段。 名稱服務專案中已經存在的任何介面也會維持不變。 針對物件 Uuid 和系結控制碼，會遵循相同的程式。

用戶端會呼叫 [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina) (或 [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)) 來搜尋適當的系結控制碼。 專案名稱、介面控制碼和物件 UUID 會解壓縮。 這些專案會限制傳回系結控制碼的專案。 如果專案符合搜尋準則，則會從 [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext)傳回該專案中的所有系結控制碼。

 

 




