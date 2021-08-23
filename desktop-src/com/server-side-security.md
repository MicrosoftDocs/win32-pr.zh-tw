---
title: Server-Side 安全性
description: Server-Side 安全性
ms.assetid: 6c1d210e-daf0-490a-a6b9-65d99b9e1d7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc7349b318361cfd27969817ec6be9d16accacd29dce625f572a51a7b3bc8082
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611008"
---
# <a name="server-side-security"></a>Server-Side 安全性

伺服器可以使用 [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity)的方法來取得呼叫端的安全性資訊，或模擬呼叫者。 使用標準封送處理時，在目前呼叫的內容物件上，COM 會提供 **IServerSecurity** 的實作為。 不過，某些自訂封送處理介面可能沒有這個介面。

當呼叫抵達伺服器時，伺服器可以呼叫 [**CoGetCallCoNtext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) 來取得 [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) 介面的指標。 使用這個指標時，伺服器可以呼叫 **IServerSecurity** 方法，找出用戶端的驗證設定，以及模擬用戶端（如有需要）。 **IServerSecurity** 物件在所有的執行緒中都是有效的，直到 **IServerSecurity** 所表示的呼叫完成為止。 如需模擬的詳細資訊， [請參閱模擬](impersonation.md) 和 [掩蓋](cloaking.md)。

您也可以使用依賴呼叫內容物件之 [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) 介面實作為的下列 helper 函數：

-   [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket)
-   [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)
-   [**CoRevertToSelf**](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM 中的安全性](security-in-com.md)
</dt> </dl>

 

 