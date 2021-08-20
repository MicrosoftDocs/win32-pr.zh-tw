---
title: COM 用戶端和伺服器
description: COM 的重要層面是用戶端和伺服器之間的互動方式。
ms.assetid: 5d1d8613-3087-443d-8547-a767c8ba4959
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79d189b464c8e3a32ff378951067275ab29f5fbabc0b2777c2b2226d632a8bfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048656"
---
# <a name="com-clients-and-servers"></a>COM 用戶端和伺服器

COM 的重要層面是用戶端和伺服器之間的互動方式。 *Com 用戶端* 是指任何程式碼或物件取得 COM 伺服器的指標，並藉由呼叫其介面的方法來使用其服務。 *COM 伺服器* 是提供服務給用戶端的任何物件;這些服務是 COM 介面實作為的形式，可讓能夠取得伺服器物件上其中一個介面指標的任何用戶端呼叫。

有兩種主要類型的伺服器，同 *進程* 和跨 *進程*。 同進程伺服器是在動態連結程式庫 (DLL) 中執行，而跨進程伺服器則是在可執行檔 (EXE) 中執行。 跨進程伺服器可以位於本機電腦或遠端電腦上。 此外，COM 也提供一種機制，可讓同進程伺服器 (DLL) 在代理 EXE 進程中執行，以取得能夠在遠端電腦上執行該處理常式的優點。 如需詳細資訊，請參閱 [DLL 代理](dll-surrogates.md)程式。

COM 程式設計模型和結構現在已經過擴充，因此 COM 用戶端和伺服器可以跨網路一起運作，而不只是在指定的電腦內。 這可讓現有的應用程式與新的應用程式互動，並在具有適當管理的網路間彼此互動，而且可以撰寫新的應用程式來利用網路功能。

COM 用戶端應用程式不需要知道伺服器物件的封裝方式、是否封裝為 Dll 中 (的同進程物件) ，或做為 Exe)  (的本機或遠端物件。 分散式 COM 可進一步允許將物件封裝為服務應用程式，並以 Windows 的豐富管理和系統整合功能來同步處理 COM。

> [!Note]  
> 在此檔中，會使用「縮寫」 COM 作為 DCOM 的喜好設定。 這是因為 DCOM 不是分開的，它只是較長的網路的 COM。 如果所述的內容是遠端作業，則會使用 *分散式 COM* 一詞。

 

COM 的設計目的是為了讓您能夠新增可延伸到網路的位置透明度支援。 它可讓針對單一電腦所撰寫的應用程式在網路上執行，並提供擴充這些功能的功能，並新增至網路所需的安全性。  (需詳細資訊，請參閱 [COM 中的安全性](security-in-com.md)) 。

COM 會指定一種機制，讓許多不同的應用程式可以使用類別程式碼。

如需詳細資訊，請參閱下列主題：

-   [取得物件的指標](getting-a-pointer-to-an-object.md)
-   [透過類別物件建立物件](creating-an-object-through-a-class-object.md)
-   [COM 伺服器責任](com-server-responsibilities.md)
-   [持續性物件狀態](persistent-object-state.md)
-   [提供類別資訊](providing-class-information.md)
-   [物件間通訊](inter-object-communication.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[呼叫同步處理](call-synchronization.md)
</dt> <dt>

[COM 中的安全性](security-in-com.md)
</dt> </dl>

 

 




