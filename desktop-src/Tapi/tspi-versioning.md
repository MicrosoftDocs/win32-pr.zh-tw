---
description: 瞭解 TSPI 版本控制。 經過一段時間，可能會產生不同版本的 TAPI、應用程式和服務提供者。
ms.assetid: 994fad0e-5958-4d93-8952-9db2bbe01f44
title: TSPI 版本控制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e0a0663a1fcc685df8643c634ec627f669aafe8
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989233"
---
# <a name="tspi-versioning"></a>TSPI 版本控制

經過一段時間，可能會產生不同版本的 TAPI、應用程式和服務提供者。 這些新版本可以建立新的定義，例如新功能、資料結構中的新成員，以及新的位欄位。 因此需要版本號碼來指出如何解讀各種資料結構。

為了讓不同的應用程式版本、TAPI 本身的版本，以及不同廠商的服務提供者版本獲得最佳互通性，Microsoft 電話語音為應用程式提供了一個簡單的版本協商機制。 有兩個不同的版本需要由 TAPI 和每一行裝置的電話語音服務提供者來同意。 第一個是基本和補充電話語音 SPI 的版本號碼，稱為 *TSPI 介面版本*。 另一個則適用于提供者專屬的延伸模組（如果有的話），而且稱為 *延伸模組版本*。 TSPI 的基本和補充功能所使用的資料結構和資料類型的格式是由 TSPI 版本所定義，而延伸模組版本則決定由廠商專屬的延伸模組所定義的資料結構格式。

這兩種版本的版本協商是由兩個不同的程式處理：使用 [**TSPI \_ lineNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) 來協商 TSPI 介面版本，而使用 [**TSPI \_ lineNegotiateExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiateextversion) 來協商延伸模組版本。 如果不需要延伸模組，可以略過延伸模組版本協商。 如果這些範圍在協商期間輸入，服務提供者必須傳回範圍中重迭部分的值，以作為協商的結果。 通常，這應該是最大的可能值。 如果範圍不重迭，則這兩個合作物件不相容，且函數會傳回錯誤。

協商的結果只會指出服務提供者願意以特定版本號碼操作，但不會認可服務提供者。 例如，在協商可能的版本之後，TAPI 可以重新協商以判斷理想的版本。 只有在使用 [**TSPI \_ lineOpen**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen) 和繼續生存開啟行時，才會認可 TSPI 介面版本，直到裝置關閉為止。 呼叫 [**TSPI \_ lineSelectExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_lineselectextversion) 函式時，會認可延伸模組版本，並繼續生存直到選取擴充功能版本零來取消選取專案為止。

延伸模組版本選擇可能會發生多次，包括延伸模組版本生效。 因為服務提供者會認可至擴充功能版本，所以其支援版本範圍會縮減為該延伸模組的版本。 例如，假設服務提供者通常與延伸模組版本1.0 至5.5 相容。 當呼叫端嘗試協調範圍1.0 到5.5 之間的版本時，如果版本3.0 有效，則協商會傳回3.0。

因為 TAPI 會協商版本，所以您可以將服務提供者升級為新版的介面，而不需要同時升級該 TAPI。 同樣地，TAPI 也可以升級，但仍可使用您較舊的服務提供者。

 

 
