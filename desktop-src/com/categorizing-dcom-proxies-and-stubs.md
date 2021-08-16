---
title: 分類 DCOM proxy 和存根
description: 分類 DCOM proxy 和存根
ms.assetid: f5d117d6-6c2c-4beb-8869-1581a5b1846f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f45f61d89e31316975685d3e603a93d30559546c86abc3b63e8e7e8a0c83ff1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118310865"
---
# <a name="categorizing-dcom-proxies-and-stubs"></a>分類 DCOM proxy 和存根

DCOM 會藉由建立包含 Clsid 的 OBJREFs 來封送處理物件的參考。 這些 Clsid 很容易受到安全性攻擊，因為封送處理期間可以載入任意 Dll。 不過，在 \_ \_ 呼叫 CoInitializeSecurity 時，不能指定 EOAC 的自訂 \_ 封送處理旗標 (請參閱 [**EOLE \_ 驗證 \_ 功能**](/windows/win32/api/objidlbase/ne-objidlbase-eole_authentication_capabilities)) 。 [](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 設定此旗標可在使用 DCOM 時協助保護伺服器安全性，因為這樣可以減少執行任意 Dll 的機會。 當設定這個旗標時，伺服器只允許封送處理 ole32.dll、comadmin.dll、comsvcs.dll 或 es.dll 中所執行的 Clsid，或是執行 CATID \_ 封送處理器分類識別碼的 clsid。

CATID \_ 封送處理器是元件類別目錄 GUID，可以與已自訂封送處理的 CLSID 相關聯。 當 EOAC \_ 沒有透過 \_ \_ [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)設定自訂封送處理時，允許使用此 CLSID 進行自訂的介面進行封送處理。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[元件類別](component-categories.md)
</dt> </dl>

 

 