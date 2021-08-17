---
description: 經過一段時間後，TAPI、應用程式和服務提供者的線路或電話可能會有不同的版本。
ms.assetid: 36a17ae8-31db-4db9-a401-097d47aa26ad
title: TAPI 版本協商
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7cd6d816c07cb1c6c93d9cc219509f257d9a2695671b5197002171f0f819f17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119404063"
---
# <a name="tapi-version-negotiation"></a>TAPI 版本協商

經過一段時間後，TAPI、應用程式和服務提供者的線路或電話可能會有不同的版本。 新版本可能會定義新功能、資料結構的新欄位等等。 因此，版本號碼會指出如何解讀不同的資料結構。

為了讓不同的應用程式版本、TAPI 本身的版本，以及不同廠商的服務提供者版本達到最佳互通性，TAPI 為應用程式提供簡單、雙步驟的版本協商機制。 每個線路裝置的應用程式、TAPI 和服務提供者必須同意兩個不同的版本。 第一個是「基本」和「補充電話語音」的版本號碼，稱為「API 版本」。 另一個則適用于提供者專屬的延伸模組（如果有的話），而且稱為延伸模組版本。 TAPI 的基本和增補功能所使用的資料結構和資料類型的格式是由 API 版本所定義，而延伸模組版本則決定由廠商專屬的延伸模組所定義的資料結構格式。

版本協商會在兩個階段中繼續進行。 在第一個階段中，會協商 API 版本號碼，並取得與裝置上支援之任何廠商專屬延伸模組相關聯的延伸模組識別碼。 在第二個階段中，會協商延伸模組版本。 如果應用程式未使用任何 API 擴充功能，則會略過第二個階段，且服務提供者不會啟用延伸模組。 如果應用程式想要使用擴充功能，但應用程式無法辨識擴充功能識別碼 (的服務提供者延伸模組) ，則應用程式也應該略過延伸模組版本的協商。 每個廠商都有自己的一組合法 (可辨識的每一組延伸模組規格的) 版本。

[**LineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion)函式是用來協調要使用的 API 版本號碼。 它也會抓取線路裝置所支援的延伸模組識別碼，如果沒有支援延伸模組，則會傳回零。 透過此函式呼叫，應用程式會提供與相容的 API 版本範圍。 TAPI 接著會與該行的服務提供者協調，以判斷它支援的 API 版本範圍。 接下來，TAPI 會選取版本號碼 (通常（但不一定）在應用程式、DLL 和服務提供者所提供的重迭版本範圍中) 最高版本號碼。 此數位會傳回至應用程式，以及定義該行服務提供者所提供之延伸模組的延伸模組識別碼。

如果應用程式想要使用由傳回的延伸模組識別碼定義的延伸模組，則必須先呼叫 [**lineNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion) 來協商延伸模組版本。 在類似的協商階段中，應用程式會指定已同意的 API 版本，以及其支援的延伸模組版本範圍。 TAPI 會將此資訊傳遞給該行的服務提供者。 服務提供者會針對其本身檢查 API 版本和延伸模組版本範圍，並選取適當的延伸模組版本號碼（如果有的話）。

當應用程式稍後呼叫 [**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)時，它會針對對應至版本協商結果的行，傳回一組裝置功能。 這些功能包括與 API 版本一致的行裝置功能，以及與延伸模組版本一致的行裝置特定功能。 應用程式在開啟一行時，必須同時指定這兩個版本號碼。 在該時間點，應用程式、DLL 和服務提供者會使用同意的版本進行認可。 如果不使用裝置專屬的延伸模組，則應該將擴充功能版本指定為零。

在多個應用程式開啟相同線路裝置的環境中，開啟線路裝置的第一個應用程式會針對想要使用該行 (服務提供者不支援多個版本的未來應用程式，選取版本 ) 。同樣地，開啟多行裝置的應用程式可能會發現，在相同的 API 版本號碼下，能更輕鬆地操作所有線路裝置。

採用 *dwAPIVersion* 或類似參數的每個函式都必須將此參數設定為應用程式所支援的最高 api 版本，或在特定裝置上使用 [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) 或 [**phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion) 函式進行協商的 api 版本。 使用下表做為指南：



| 函數                                                     | 意義                                                                               |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)             | 使用 [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion)所傳回的版本。   |
| [**lineGetCountry**](/windows/desktop/api/Tapi/nf-tapi-linegetcountry)                     | 使用應用程式所支援的最高版本。                                     |
| [**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)                     | 使用 [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion)所傳回的版本。   |
| [**lineGetProviderList**](/windows/desktop/api/Tapi/nf-tapi-linegetproviderlist)           | 使用應用程式所支援的最高版本。                                     |
| [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)         | 使用應用程式所支援的最高版本。                                     |
| [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion)   | 使用應用程式所支援的最高版本。                                     |
| [**lineNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion)   | 使用 [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion)所傳回的版本。   |
| [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)                                 | 使用 [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion)所傳回的版本。   |
| [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress)         | 使用應用程式所支援的最高版本。                                     |
| [**lineTranslateDialog**](/windows/desktop/api/Tapi/nf-tapi-linetranslatedialog)           | 使用應用程式所支援的最高版本。                                     |
| [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)                   | 使用 [**phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion)所傳回的版本。 |
| [**phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion) | 使用應用程式所支援的最高版本。                                     |
| [**phoneNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateextversion) | 使用 [**phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion)所傳回的版本。 |
| [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen)                               | 使用 [**phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion)所傳回的版本。 |



 

> [!IMPORTANT]
> 當您協商 API 版本時，請一律將最高和最低版本號碼設定為您的應用程式可支援的版本範圍。 例如，絕對不能使用較低版本的0x00000000 或0xFFFFFFFF，因為這些值需要您的應用程式支援所有的 TAPI 版本，包括過去和未來。

 

 

 



