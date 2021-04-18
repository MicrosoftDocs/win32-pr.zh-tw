---
description: 網路提供者是一種 DLL，可讓 Windows 作業系統與其他種類的網路（例如 Novell）進行互動。 它是 Windows WNet 驅動程式的用戶端。
ms.assetid: d316f159-4fe3-4b78-9efc-177906875918
title: 網路提供者 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc68184f60639a603614cbaf71631a2521012cf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978074"
---
# <a name="network-provider-api"></a>網路提供者 API

網路提供者是一種 DLL，可讓 Windows 作業系統與其他種類的網路（例如 Novell）進行互動。 它是 Windows WNet 驅動程式的用戶端。 網路提供者會執行網路特定的動作，例如建立連線，並公開 Windows 的通用介面。 此介面稱為網路提供者 API，並由網路提供者所執行的函式所組成。 您可以建立網路提供者 DLL 來支援新的網路通訊協定。

由於每個網路都會透過其提供者公開通用介面，因此 Windows 可以與數種網路類型互動，而不需要知道其網路特定的執行詳細資料。

[*多個提供者路由器*](../secgloss/m-gly.md) (MPR) 處理與系統上所有不同網路提供者的通訊，並向使用者呈現整合的網路。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[網路提供者](network-providers.md)
</dt> <dt>

[認證管理員](credential-manager.md)
</dt> <dt>

[多個提供者路由器](multiple-provider-router.md)
</dt> <dt>

[網路提供者所執行的函式](functions-implemented-by-network-providers.md)
</dt> <dt>

[認證管理 API](credential-management-api.md)
</dt> <dt>

[連接通知 API](connection-notification-api.md)
</dt> </dl>

 

 
