---
title: COM 伺服器責任
description: COM 伺服器責任
ms.assetid: 9853bbf5-b989-45b7-8fa8-8cd2f0d48d3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86b9d3104af80a7b2dca49dbbd5b55e66a613ee7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382958"
---
# <a name="com-server-responsibilities"></a>COM 伺服器責任

用戶端若要取得物件指標，最重要的方法之一就是讓用戶端要求啟動伺服器，並建立和啟動伺服器所提供的物件實例。 這是伺服器的責任，可確保正常運作。 這有幾個重要的部分。

伺服器必須透過 [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) 或 [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) 介面的實執行類別物件的程式碼。

伺服器必須在其所在電腦上的系統登錄中登錄其 CLSID，並且可選擇將其電腦位置發佈到網路上的其他系統，以允許用戶端呼叫它，而不需要用戶端知道伺服器的位置。

伺服器主要負責安全性;亦即，在大部分的情況下，伺服器會決定是否要將其一個物件的指標提供給用戶端。

同進程伺服器應該會執行並匯出某些函數，讓用戶端進程具現化它們。

下列主題將詳細說明 COM 伺服器的職責：

-   [執行 IClassFactory](implementing-iclassfactory.md)
-   [授權和 IClassFactory2](licensing-and-iclassfactory2.md)
-   [註冊 COM 伺服器](registering-com-servers.md)
-   [跨進程伺服器執行協助程式](out-of-process-server-implementation-helpers.md)
-   [建立和優化 GUID](guid-creation-and-optimizations.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM 用戶端和伺服器](com-clients-and-servers.md)
</dt> </dl>

 

 