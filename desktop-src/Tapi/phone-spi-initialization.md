---
description: 在 TSPI 所定義的電話裝置抽象中，TAPI 和服務提供者必須先進行基本初始化。
ms.assetid: cd8bb328-fbd0-409c-8471-34ad4c2c8d93
title: Phone SPI 初始化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d0c54e313c2be3846aeb604217f5324ec0d8a8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984620"
---
# <a name="phone-spi-initialization"></a>Phone SPI 初始化

在 TSPI 所定義的電話裝置抽象中，TAPI 和服務提供者必須先進行基本初始化。 這兩個基本初始化是針對介面的線條和電話部分，以相同的一組步驟來完成。 這些步驟的第一個步驟是介面版本協商。 TAPI 藉由呼叫 [**TSPI \_ lineNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) 函式來執行這項工作。 此函式通常用來代表個別線路裝置進行協商;相同服務提供者內的不同線路裝置可能會根據不同的介面版本運作。 TAPI 會傳遞特殊的保留裝置識別碼值（ [**初始化 \_ 協調**](initialize-negotiation.md)），表示它正在協商影響整個服務提供者的初始化函式的整體介面版本，這兩者都適用于線路和行動電話。

此協商的結果會傳遞至後續的程式，直到手機裝置開啟為止。 屆時，手機裝置會認可至特定的介面版本。 這個介面版本在關閉電話之前是隱含的，而且不需要傳遞至在開啟的電話上操作的後續函式。

在整體介面版本協商之後，TAPI 會呼叫 [**TSPI \_ providerInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit) 函式。 此函式會初始化服務提供者，同時提供後續作業所需的參數。 這些參數包括下列各項：

-   *dwPermanentProviderID*：指定要初始化之服務提供者的永久識別碼，此識別碼在此系統的服務提供者內是唯一的。
-   *dwLineDeviceIDBase*：指定此服務提供者所支援之線路裝置的最低裝置識別碼。
-   *dwPhoneDeviceIDBase*：指定此服務提供者所支援之電話裝置的最低裝置識別碼。 電話語音電話裝置類別的裝置是由從零開始的整數所識別。 此範圍的識別碼在全系列電話裝置之間是連續的。 由於可能有多個服務提供者在單一系統中管理電話裝置，因此每個服務提供者都會取得總範圍的連續部分。 此參數會告知服務提供者其範圍部分的最小值。 服務提供者（而不是 TAPI）負責將此變數範圍對應至本身的內部裝置識別碼。 這可讓服務提供者廠商有足夠的彈性，可在裝置專屬的延伸模組中使用裝置識別碼（如有需要）。 因為服務提供者知道哪些裝置識別碼會出現在 TAPI 定義的參數和資料結構中，所以它可以在裝置專屬的擴充參數和資料結構中使用一致的裝置識別碼。
-   *dwNumLines*：指定此服務提供者支援的行裝置數目。
-   *dwNumPhones*：指定此服務提供者支援的電話裝置數目。
-   *lpfnCompletionProc*：指定服務提供者呼叫的程式，以報告線路和手機裝置上所有非同步作業程式的完成。

在 [**TSPI \_ providerInit**](/windows/win32/api/tspi/nf-tspi-tspi_providerinit)之後，就可以執行一般作業，例如開啟電話。

 

 
