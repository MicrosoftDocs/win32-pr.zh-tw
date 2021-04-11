---
title: QueryInterface 委派
description: QueryInterface 委派
ms.assetid: c5c1b584-9ca3-4dc4-a769-0142e5d8790a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e062f3d063d4f23c941182d80170cec0a680c6f3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104093359"
---
# <a name="delegation-of-queryinterface"></a>QueryInterface 委派

需要存取 proxy 管理員上部分內部介面的處理常式，必須經過 [**IInternalUnknown**](/windows/win32/api/objidlbase/nn-objidlbase-iinternalunknown) 介面。 這可防止處理常式盲目地委派和公開 aggregatee 在匯總之外的內部介面。 這些介面包括 [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) 和 [**IMultiQI**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi)。 如果處理常式想要公開 **IClientSecurity** 或 **IMultiQI**，則應該自行執行。

在 [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity)的案例中，如果用戶端嘗試在處理常式公開的介面上設定安全性，則處理常式應該在基礎網路介面 proxy 上設定安全性。

在 [**IMultiQI**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi)的情況下，處理常式應該填入它所知道的介面，然後將呼叫轉送至 proxy 管理員以取得其餘的介面。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[輕量 Client-Side 處理常式](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 