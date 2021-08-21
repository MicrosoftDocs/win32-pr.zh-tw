---
description: 邏輯感應器會提供資料，而不需視硬體裝置而定。
ms.assetid: fb0f0324-d72e-4759-9f4d-deedf8848e21
title: 關於邏輯感應器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 655bb7a6e67223bb959b155e55f6cc059ffd8280bc8c08fb00d4d88cb2c8b0a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003888"
---
# <a name="about-logical-sensors"></a>關於邏輯感應器

*邏輯感應器* 會提供資料，而不需視硬體裝置而定。 例如，邏輯感應器可以使用在資料表中查閱 IP 位址的服務，來提供使用者目前位置的相關資料。 邏輯感應器會實作為感應器驅動程式。 如需如何執行感應器驅動程式的相關資訊，請參閱 Windows 驅動程式套件。

在使用者的電腦上安裝邏輯感應器之後，您可以使用與以硬體為基礎的感應器一樣的方式來使用它。 感應器 API 會提供代表邏輯感應器的 [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) 介面，而您的程式可以透過與用於任何其他類型感應器的相同機制來要求資料。 邏輯感應器也可以使用平臺定義的感應器類別、類型、資料類型、屬性和事件。 或者，您也可以定義自訂值。

[**ILogicalSensorManager**](/previous-versions/windows/desktop/legacy/dd318934(v=vs.85))介面可讓開發人員建立邏輯感應器來管理感應器和位置平臺的連接。

> [!Note]  
> 如同其他驅動程式，安裝或卸載邏輯感應器驅動程式需要系統管理員許可權。

 

若要嘗試使用範例邏輯感應器，請參閱 [關於範例和工具](about-the-samples.md)。

## <a name="managing-logical-sensors"></a>管理邏輯感應器

[**ILogicalSensorManager**](/previous-versions/windows/desktop/legacy/dd318934(v=vs.85)) 具有下列方法：

-   [**連線**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85))
-   [**中斷連線**](/previous-versions/windows/desktop/legacy/dd374030(v=vs.85))
-   [**解除安裝**](/previous-versions/windows/desktop/legacy/dd374031(v=vs.85))

當您呼叫 [**連線**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85))時，感應器 API 會建立感應器驅動程式的實例（如果尚未存在），然後將邏輯感應器連接到平臺。 這表示邏輯感應器會與 **定位和其他感應器** 主控台中的其他感應器一起出現。 當您呼叫 [**中斷**](/previous-versions/windows/desktop/legacy/dd374030(v=vs.85))連線時，感應器 API 會中斷邏輯感應器的連線，並將其從主控台中移除。 呼叫 **中斷** 連線並不會從 **裝置管理員** 移除邏輯感應器。 因此，未來對 **連線** 的呼叫會導致連接到邏輯感應器的速度更快。

若要移除邏輯感應器，您必須呼叫 [**Uninstall**](/previous-versions/windows/desktop/legacy/dd374031(v=vs.85))。 卸載邏輯感應器會移除 **裝置管理員** 的感應器。 由於邏輯感應器裝置只存在於記憶體中，因此當使用者重新開機 Windows 時，會卸載邏輯感應器。

感應器 API 會依 *邏輯識別碼*（ **GUID**）來識別特定的邏輯感應器。 每次連接到特定的邏輯感應器時，都必須提供邏輯識別碼。 每次中斷連接或卸載特定感應器時，您必須提供您用來連線的相同邏輯識別碼。 如果您使用不同的邏輯識別碼多次連線到相同的邏輯感應器驅動程式，則會為每個新的邏輯識別碼建立個別的邏輯感應器實例。 即使您為每個邏輯識別碼呼叫「[**中斷**](/previous-versions/windows/desktop/legacy/dd374030(v=vs.85))連線」，這些個別的實例仍會保留在 **裝置管理員** 中，直到您針對每個邏輯感應器呼叫 [**卸載**](/previous-versions/windows/desktop/legacy/dd374031(v=vs.85))，或使用者重新開機 Windows。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用邏輯感應器](using-logical-sensors.md)
</dt> </dl>

 

 
