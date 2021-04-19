---
description: 為了讓命名空間提供者能夠透過 Windows 通訊端存取，它必須正確安裝在系統上，並向 Windows 通訊端註冊。
ms.assetid: c73baf62-b862-476c-b381-be00699e78ca
title: 名稱解析設定和安裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423e0ca7c9c5290a040a17e0f1ded2a97a1aed15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998237"
---
# <a name="name-resolution-configuration-and-installation"></a>名稱解析設定和安裝

為了讓命名空間提供者能夠透過 Windows 通訊端存取，它必須正確安裝在系統上，並向 Windows 通訊端註冊。 藉由叫用廠商的安裝程式來安裝命名空間提供者時，必須將設定資訊新增至設定資料庫，以提供 Ws2 \_32.dll 有關服務提供者的必要資訊。 Ws2 \_32.dll 會匯出 [**WSCInstallNameSpace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace) ，供廠商的安裝程式使用。 此函式是用來提供要安裝之服務提供者的相關資訊。 此資訊包括：

-   提供者名稱—表示在主控台中顯示之提供者的字串。
-   提供者版本-此提供者的版本。
-   提供者路徑-提供者 DLL 的路徑名稱。
-   命名空間：提供者所支援的命名空間。
-   提供者 GUID-代表此提供者/命名空間組合的唯一廠商提供數位。 這會用來做為此提供者的所有後續參考，以及卸載的索引鍵。 這些值是使用 Uuidgen.exe 公用程式所建立。
-   儲存所有旗標—此旗標指出這個命名空間提供者是否將負責保留所有服務類別的所有服務類別架構資訊。 如果有這類提供者，Ws2 \_32.dll 就不需要查詢每個個別的命名空間提供者來取得這項資訊。

在 Windows Vista 和更新版本上，提供了增強的 [**WSCInstallNameSpaceEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex32) 函式，可讓命名空間提供者傳遞特定于命名空間的額外資料 blob。

在64位平臺上，會提供類似的 [**WSCInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace32) 和 [**WSCInstallNameSpaceEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex32) 功能，以在32位目錄中安裝命名空間。

Ws2 \_32.dll 也提供一個函式 [**WSCUnInstallNameSpace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscuninstallnamespace)，供廠商的卸載程式從設定資料庫移除所有相關資訊。 這項設定資訊的確切位置和格式對 Ws232.dll 是私 \_ 用的，而且只能由上述的函式來操作。

在64位平臺上，會提供類似的 [**WSCInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace32) 函式來卸載32位目錄中的命名空間。

在任何時間點，都會將命名空間提供者視為使用中或非作用中，並透過 [**WSCEnableNSProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider) 和 [**WSCEnableNSProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider32) 函式來控制此設定。 當使用 [**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa)、 [**WSAEnumNameSpaceProvidersEx**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersexa)、 [**WSCEnumNameSpaceProviders32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumnamespaceproviders32)和) [**WSCEnumNameSpaceProvidersEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumnamespaceprovidersex32) 函式來列舉 (時，仍會繼續顯示非作用中的命名空間提供者，但是 Ws2 \_32.dll 不會將任何查詢或服務註冊作業路由傳送給這些提供者。 如果有多個已安裝的命名空間提供者可以支援指定的命名空間，這項功能就很有用。

當單一 API 函式中參考多個命名空間提供者時，不會指定將查詢和註冊作業路由傳送至命名空間提供者的順序。 順序與命名空間提供者的安裝順序無關。 有兩種方式可以控制要使用哪一個命名空間提供者來解析名稱查詢。 首先， [**WSCEnableNSProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider) 和 [**WSCEnableNSProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider32) 函數可用來以整個電腦的持續方式來啟用和停用命名空間。 第二，應用程式可以藉由指定提供者的識別 GUID 作為查詢的一部分，將個別查詢導向至特定的提供者。

 

 



