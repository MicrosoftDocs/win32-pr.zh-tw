---
title: 註冊 COM 伺服器
description: 註冊 COM 伺服器
ms.assetid: aaa09a1b-deb8-424f-a911-ae22d39919d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefaa47d159d776a3c931ca48de0dd3161c29913
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104093336"
---
# <a name="registering-com-servers"></a>註冊 COM 伺服器

在程式碼中定義類別之後 (確定它會 [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) 或 [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)) 並指派 CLSID 給它，您必須將資訊放在登錄中，以允許 COM （要求用戶端具有 CLSID）建立其物件的實例。 這項資訊會告訴系統，指定的 CLSID，也就是該類別的 DLL 或 EXE 程式碼所在的位置，以及其啟動方式。

在登錄中註冊類別的方法不止一種。 此外，還有其他方法可在執行的系統中「註冊」類別，讓系統知道正在執行的物件目前在系統中。

如需有關註冊的詳細資訊，請參閱下列主題：

-   [在安裝時註冊類別](registering-a-class-at-installation.md)
-   [註冊正在執行的 EXE 伺服器](registering-a-running-exe-server.md)
-   [在 ROT 中註冊物件](registering-objects-in-the-rot.md)
-   [自我註冊](self-registration.md)
-   [安裝為服務應用程式](installing-as-a-service-application.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM 伺服器責任](com-server-responsibilities.md)
</dt> </dl>

 

 