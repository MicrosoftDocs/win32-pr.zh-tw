---
description: 為了讓傳輸通訊協定可透過 Windows 通訊端存取，它必須正確安裝在系統上，並向 Windows 通訊端註冊。
ms.assetid: 0f0b22e4-81b7-43a7-bc2f-7124fa32d925
title: 傳輸設定和安裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea980740f727e39338c7568f4cc30a961b5484df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001334"
---
# <a name="transport-configuration-and-installation"></a>傳輸設定和安裝

為了讓傳輸通訊協定可透過 Windows 通訊端存取，它必須正確安裝在系統上，並向 Windows 通訊端註冊。 藉由叫用廠商的安裝程式來安裝傳輸服務提供者時，必須將設定資訊新增至設定資料庫，以提供 Ws2 \_32.dll 有關服務提供者的必要資訊。 Ws2 \_32.dll 會針對廠商的安裝程式匯出數個安裝功能（ [**WSCInstallProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallprovider) 和 [**WSCInstallProviderAndChains**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallproviderandchains)），以提供要安裝之服務提供者的相關資訊。 例如，這項資訊包含服務提供者 DLL 的名稱和路徑，以及此提供者可支援的 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 結構清單。 Ws2 \_32.dll 也提供廠商的卸載程式的函式 [**WSCDeinstallProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscdeinstallprovider)，以從 Ws232.dll 所維護的設定資料庫中移除所有相關資訊 \_ 。 這項設定資訊的確切位置和格式對 Ws232.dll 是私 \_ 用的，而且只能由上述的函式來操作。

在64位平臺上，有類似的函式可在32位和64位目錄上運作。 這些函數包括 [**WSCInstallProvider64 \_ 32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallprovider64_32)、 [**WSCInstallProviderAndChains64 \_ 32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallproviderandchains64_32)和 [**WSCDeinstallProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscdeinstallprovider32)。

最初安裝傳輸服務提供者的順序，會控制在服務提供者介面上透過 [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols) 和 [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) 列舉的順序，或透過應用程式介面上的 [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) 來進行列舉的順序。 更重要的是，當用戶端要求根據地址系列、類型和通訊協定識別碼建立通訊端時，此順序也會控制通訊協定和服務提供者的順序。 Windows 通訊端2包含稱為 Sporder.exe 的小程式，可讓已安裝的通訊協定目錄在安裝通訊協定之後以互動方式重新排序。 Windows 通訊端2也包含輔助 DLL （Sporder.dll），可匯出重新排列通訊協定的程式性介面。 這個程式介面是由稱為 [**WSCWriteProviderOrder**](/windows/desktop/api/Sporder/nf-sporder-wscwriteproviderorder)的單一程式所組成。

## <a name="installing-layered-protocols-and-protocol-chains"></a>安裝多層式通訊協定和通訊協定鏈

每個要安裝的通訊協定所提供的 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 結構，都會指出通訊協定是基本通訊協定、分層式通訊協定或通訊協定鏈。 *ProtocolChain. ChainLen* 參數的值如下表所示。

| 值 | 意義                                           |
|-------|---------------------------------------------------|
| 0     | 多層通訊協定。                                 |
| 1     | 基本通訊協定 (或僅) 一個元件。 |
| > 1 | 通訊協定鏈。                                   |



 

通訊協定鏈的安裝只會在成功安裝所有組成元件 (基礎通訊協定和分層通訊協定) 之後才會發生。 通訊協定鏈的 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 結構會使用 *ProtocolChain* 參數來描述鏈的長度和每個元件的身分識別。 組成鏈的個別通訊協定會依序列在 ProtocolChain. ChainEntries 陣列中，並具有對應至第一個分層提供者的陣列第零個元素。 通訊協定是由 Ws232.dll 在通訊協定安裝時所指派的 *CatalogEntryID* 值來識別， \_ 並可在每個通訊協定的 **WSAPROTOCOL \_ 資訊** 結構中找到。

您應選擇通訊協定鏈 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 結構中其餘參數的值，以反映最能將通訊協定鏈視為整體的屬性和識別碼。 當選取這些值時，開發人員應該注意，只有在兩個端點都已安裝相容的通訊協定鏈，而且應用程式必須能夠辨識對應的 **WSAPROTOCOL \_ 資訊** 結構時，才會透過通訊協定鏈進行通訊。

安裝基本通訊協定時，不需要在 *ProtocolChain. ChainEntries* 陣列中建立任何專案。 它會隱含地瞭解，此鏈的唯一元件已在相同 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)結構的 *CatalogEntryID* 參數中識別。 另請注意，通訊協定鏈可能不包含相同分層通訊協定的多個實例。

 

 
