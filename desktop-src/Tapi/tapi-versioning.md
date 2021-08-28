---
description: 瞭解 TAPI 版本控制。 經過一段時間，可能會產生不同版本的 TAPI、應用程式和服務提供者。
ms.assetid: 35fea8f9-307e-4429-b4ec-ffb5c62c2610
title: TAPI 版本控制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f940cead427f843bb7cf3a3a89e1747344a8ffa2ddb8fff5a2b30db0b5a7f2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872888"
---
# <a name="tapi-versioning"></a>TAPI 版本控制

經過一段時間，可能會產生不同版本的 TAPI、應用程式和服務提供者。 這些新版本可以建立新的定義，例如新功能、資料結構中的新成員，以及新的位欄位。 因此需要版本號碼來指出如何解讀各種資料結構。

為了讓不同的應用程式版本、TAPI 本身的版本，以及不同廠商的服務提供者版本獲得最佳互通性，Microsoft 電話語音為應用程式提供了一個簡單的版本協商機制。 有兩個不同的版本，TAPI 和電話語音服務提供者必須針對每一行裝置同意。 第一個是與 TAPI 協商的版本，以及電話語音服務提供者 (TSP) 基本和補充電話語音，稱為 TAPI 介面版本。 另一個則適用于提供者專屬的延伸模組（如果有的話），而且稱為延伸模組版本。 TAPI 的基本和增補功能所使用的資料結構和資料類型的格式是由 TAPI 版本所定義，而延伸模組版本則決定由供應商專屬的延伸模組所定義的資料結構格式。

[**LineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion)函式會協商 TAPI 版本，而 [**LINENEGOTIATEEXTVERSION**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion)會協商 TSP 延伸模組版本。 單一 TSP 可以處理一個以上的版本，而如果使用較舊的 TSP，應用程式必須「切換回」使用較舊的版本。 在 **lineNegotiateAPIVersion** 中， *dwApiVersion* 參數預設為根據版本的值，如下所示。



| TAPI 版本 | 預設值 |
|--------------|---------------|
| 1.3          | 0x00010003    |
| 1.4          | 0x00010004    |
| 2.0          | 0x00020000    |
| 2.1          | 0x00020001    |
| 2.2          | 0x00020002    |



 

但是，只要 TSP 本身使用的是比應用程式更新的版本，TAPI 就能讓這項作業更容易。 如果 TSP 的確很新，則 TAPI 能夠將 "down" 轉譯為應用程式的版本。 例如，TAPI 2.0 Tsp 不需要特別能夠處理 TAPI 1.4 版。 如果執行 TAPI 1.4 應用程式，TAPI 會將所有 TAPI 2.0 結構和訊息轉換成 TAPI 1.4 對等專案，或盡可能接近。 如果 TAPI 1.4 中沒有接近近似值，則所有 TAPI 2.0 特定的資訊都將遺失。

延伸模組版本的精確意義是提供者特有的。 若要使用支援擴充功能的 TSP，請參閱提供者的檔。

TAPI 有許多版本。 雖然這些版本大多涉及變更 TAPI 和電話語音服務提供者介面 (TSPI) 檔集，但每個版本都有其他含意，也就是架構差異、作業系統變化、可轉散發套件和 TSP 開發問題。



| TAPI 版本        | 散發                                                   |
|---------------------|----------------------------------------------------------------|
| 1.0 –1。2           | 不應再使用的 Beta 版。              |
| [1.4](tapi-1-4.md) | 隨附于 Windows 95。                                        |
| [1.5](tapi-1-5.md) | 隨附于 Windows CE 1.0。                                    |
| [2.0](tapi-2-0.md) | 隨附于 Windows NT 4.0 SP3。                           |
| [2.1](tapi-2-1.md) | 隨附于 Windows NT 4.0 加裝 SP4 和 Windows 98。            |
| [2.2](tapi-2-2.md) | 包含在 Windows Server 2003、Windows XP 和 Windows 2000 中。 |



 

 

 



