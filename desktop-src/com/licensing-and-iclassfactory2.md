---
title: 授權和 IClassFactory2
description: 授權和 IClassFactory2
ms.assetid: 2bead555-8c62-4f48-a4c6-6f0942ec75f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9376d5187588ba14da434161309409bf1d189a8f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382970"
---
# <a name="licensing-and-iclassfactory2"></a>授權和 IClassFactory2

類別物件上的 [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) 介面提供 COM 的基本物件建立機制。 使用 **IClassFactory**，伺服器可以控制以機器為基礎的物件建立。 [**IClassFactory：： CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance)方法的執行可以根據機器授權的存在，來允許或禁止建立物件。 電腦授權是一種與存在於電腦上的應用程式不同的資訊，表示軟體是從有效的來源（例如廠商的安裝磁片）安裝。 如果電腦授權不存在，伺服器就不允許建立物件。 電腦授權可在使用者嘗試將軟體從一部電腦複製到另一部電腦時，防止盜版，因為授權資訊不會與軟體一起複製，而且接收該複本的電腦未獲授權。

不過，在元件軟體產業中，廠商需要更精細的授權控制層級。 除了電腦授權控制之外，廠商還必須允許某些用戶端建立元件物件，同時拒絕其他用戶端相同的功能。 當用戶端應用程式仍在開發期間，用戶端應用程式必須從元件取得授權金鑰。 用戶端應用程式會在執行時間使用授權金鑰，在未授權的電腦上建立物件。

例如，如果廠商將控制項程式庫提供給開發人員，則購買程式庫的開發人員將擁有完整的電腦授權，可讓您在開發電腦上建立物件。 然後，開發人員可以在已授權的電腦上建立用戶端應用程式，其中包含一或多個控制項。 當產生的用戶端應用程式在另一部電腦上執行時，必須在另一部電腦上建立用戶端應用程式中使用的控制項，即使該機器沒有原始廠商的控制項電腦授權。

[**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)介面提供此層級的控制。 若要允許任何指定元件以金鑰為基礎的授權，您可以在該元件的 class factory 物件上執行 **IClassFactory2** 。 **IClassFactory2** 衍生自 [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)，因此藉由執行 **IClassFactory2**，class FACTORY 物件可滿足基本的 COM 需求。

若要將授權元件併入用戶端應用程式，請在 [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)中使用下列方法：

-   [**GetLicInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-getlicinfo)方法會以描述 class factory 授權行為的資訊來填滿 [**LICINFO**](/windows/win32/api/ocidl/ns-ocidl-licinfo)結構。 例如，如果 **fRunTimeKeyAvail** 成員為 **TRUE**，class factory 可提供執行時間授權的授權金鑰。
-   [**RequestLicKey**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-requestlickey)方法會提供元件的授權金鑰。 當用戶端呼叫這個方法時，必須提供電腦授權。
-   如果授權金鑰參數 (BSTRÂ bstrKey) 有效， [**CreateInstanceLic**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-createinstancelic) 方法就會建立授權元件的實例。

> [!Note]  
> 在其類型資訊中，元件會使用已授權的屬性來標示支援透過 [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)授權的 coclass。

 

首先，您需要個別的開發工具，也就是授權元件的用戶端。 這項工具的目的是要取得執行時間授權金鑰，並將它儲存在您的用戶端應用程式中。 此工具只會在擁有該元件之電腦授權的電腦上執行。 此工具會呼叫 [**GetLicInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-getlicinfo) 和 [**RequestLicKey**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-requestlickey) 方法來取得執行時間授權金鑰，然後將授權金鑰儲存在您的用戶端應用程式中。 例如，開發工具可以建立包含 BSTR 授權金鑰 ( .h) 檔案的標頭，然後在用戶端應用程式中包含該 .h 檔案。

若要在用戶端應用程式中具現化元件，請先嘗試使用 [**IClassFactory：： CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance)直接具現化物件。 如果 **CreateInstance** 成功，則第二部機器會獲得元件的授權，而物件也可以建立。 如果 **CreateInstance** 因為傳回碼類別 \_ E \_ NOTLICENSED 而失敗，建立物件的唯一方法是將執行時間索引鍵傳遞給 [**CreateInstanceLic**](/windows/desktop/api/OCIdl/nf-ocidl-iclassfactory2-createinstancelic) 方法。 **CreateInstanceLic** 會驗證金鑰，並在索引鍵有效時建立物件。

如此一來，使用元件建立的應用程式 (例如控制項) 可以在沒有其他授權的電腦上執行，只允許包含執行時間授權的用戶端應用程式建立有問題的元件物件。

[**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)介面支援授權方案的彈性。 例如，伺服器實作項可以加密元件中的授權金鑰，以提高安全性。 伺服器實作者也可以為不同的功能提供不同的授權金鑰，以啟用或停用其物件中的功能層級。 例如，一個索引鍵可能會允許基底層級的功能，而另一個則允許基本和先進的功能，依此類推。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM 伺服器責任](com-server-responsibilities.md)
</dt> </dl>

 

 