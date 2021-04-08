---
title: DLL 伺服器需求
description: 雖然大部分的 Dll 都可以在代理中執行，但是某些 Dll 無法執行。
ms.assetid: f89dabe6-f65f-4d90-ad0e-c680d4b08ba5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae82aa44771d398d80169c56976df7b0e209ea6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022102"
---
# <a name="dll-server-requirements"></a>DLL 伺服器需求

雖然大部分的 Dll 都可以在代理中執行，但是某些 Dll 無法執行。

如果您想要使用系統提供的代理，DLL 必須有良好的行為。 例如，呼叫從用戶端註冊回呼之方法的 DLL，會嘗試叫用這些回呼，如同它所接收的函式指標是否為其位址空間中的指示（不是如此）。 同樣地，使用預期用戶端存取之全域變數的 DLL 無法運作。 一般情況下，無法正確封送處理的參數將會使 DLL 伺服器無法在用戶端進程之外執行。 在許多情況下，您可以撰寫明確設計來彌補「不良」行為的自訂代理。  (需詳細資訊，請參閱 [撰寫自訂代理](writing-a-custom-surrogate.md)。 ) 

如果 DLL 伺服器使用自訂介面，您必須確定這些介面可使用封送處理常式代碼。 例如，您可以建立並註冊 proxy DLL，或是提供並註冊類型程式庫，讓伺服器能夠在代理程式中執行時正常運作。

DLL 伺服器只會載入至在適當的安全性內容中執行的代理程式。 DLL 伺服器代理的安全性內容是以與 EXE 伺服器相同的方式來決定。 除非在伺服器的 [AppID](appid-clsid.md)登錄區段中設定了 **RunAs** 值（決定安全性內容），否則 DLL 伺服器代理會在與用戶端相同的安全性內容中執行。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DLL 代理](dll-surrogates.md)
</dt> </dl>

 

 




