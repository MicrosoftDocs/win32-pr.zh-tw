---
title: 感應器平臺
description: Windows 7 變更了開發人員使用感應器的方式。
ms.assetid: ed323658-dfd6-4c1b-ada2-5d68ebb56482
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7072a19ee0a746b0764850230a06de1ca72be8ca4633f1350165297f1ef4036
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118203888"
---
# <a name="sensor-platform"></a>感應器平臺

Windows 7 變更了開發人員使用感應器的方式。 它包含對感應器的原生支援，並透過新的開發平臺（用於處理感應器）擴充，包括定位感應器，例如 (GPS) 裝置的全球定位系統。

*Windows 位置* api 是以感應器平臺為基礎，這是新的 Windows 7 功能，可讓應用程式開發人員存取使用者的實體位置資訊。 *Windows 的位置* api 可以抽象化硬體、同時支援多個應用程式，並在不同的技術之間無縫切換，讓應用程式開發人員不必承擔管理這些限制的負擔。 使用 c + + 程式設計語言 (程式設計人員可以使用 *位置* api，方法是熟悉元件物件模型 (COM) ) ，或在指令碼語言中使用 COM 物件，例如 Microsoft JScript。 腳本支援可讓您輕鬆存取專案的位置資料，例如小工具。

Windows 7 提供一個穩固且便於使用的平臺，可讓您使用感應器裝置，例如環境光線感應器或溫度測計，在 Windows 應用程式中建立環境感知。 電腦可以使用內建于電腦、透過有線或無線連線連線，或是透過網路或 *網際網路* 連線的感應器。

*感應器* 和 *位置* api 提供了一種標準方式來探索感應器，並以程式設計方式存取感應器提供的資料。

*感應器* 控制台可讓使用者啟用或停用感應器、控制可能公開敏感性資料之感應器的存取、查看感應器屬性，以及變更感應器的描述。

[感應器類別延伸](/windows-hardware/drivers/sensors/about-the-sensor-class-extension)是感應器平臺驅動程式開發模型的核心部分。 它提供下列機制，在撰寫 [使用者模式驅動程式架構 () ](https://developer.microsoft.com/windows/hardware) 感應器驅動程式時，會使用這些機制：

-   與感應器平臺整合
-   安全性強制

## <a name="related-topics"></a>相關主題

<dl> <dt>

[感應器 API](../sensorsapi/portal.md)
</dt> <dt>