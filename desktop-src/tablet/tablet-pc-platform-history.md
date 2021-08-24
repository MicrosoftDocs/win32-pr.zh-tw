---
description: 本節說明 Tablet PC 技術的版本歷程記錄。
ms.assetid: 69eb161a-2330-456f-b7b8-234cf02c8b58
title: Tablet PC 平臺歷程記錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78cbcecd8ee02f56a4d89b2ca9d14217da277525dd3548adec7282d6744d1d24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119843048"
---
# <a name="tablet-pc-platform-history"></a>Tablet PC 平臺歷程記錄

本節說明 Tablet PC 技術的版本歷程記錄。

## <a name="platform-description"></a>平臺描述

Tablet PC 技術元件可讓您開發針對 Tablet PC 硬體設計的應用程式。

這些元件可以用來建立在 Windows XP Tablet PC Edition 2005、Windows Vista、Windows 7、Windows Server 2008 R2 和其他某些舊版作業系統上執行的應用程式。

Windows Presentation Foundation 也支援 Tablet PC 應用程式的開發。

## <a name="version-history"></a>版本歷程記錄

### <a name="tablet-platform-in-windows-7-and-windows-server-2008-r2"></a>Windows 7 和 Windows Server 2008 R2 中的平板電腦平臺

Windows 7 引進了其他語言支援、數學輸入控制項和自訂字典。 Windows 作業系統也已新增[Windows Touch](../wintouch/windows-touch-portal.md)功能。

WindowsServer 2008 R2 引進了其他語言、自訂字典和伺服器端辨識的支援。

下列功能可增強平板電腦功能，並讓開發人員提供新的應用程式，以支援使用者的實際案例。

-   數學輸入控制項允許從 Windows 7 中的手寫文字輸入數學公式和函數。
-   為了改進文字辨識，Windows 7 和 Windows Server 2008 R2 支援自訂字典，讓系統管理員可以直接啟用單字清單的支援。
-   Windows觸控除了支援移動、縮放和旋轉的手勢辨識 API 之外，還支援多個觸控來源的輸入。
-   WindowsServer 2008 R2 支援表單輸入的伺服器端識別，也支援伺服器端辨識的自訂字典。 藉由新增這些功能，開發人員和系統管理員可以建立和自訂功能強大的應用程式，以支援從伺服器端進行手寫辨識。

### <a name="tablet-platform-in-windows-vista"></a>Windows Vista 中的平板電腦平臺

Tablet PC 技術二進位檔已在 Windows Vista 中更新。 更新的 Tablet PC 技術包含新的筆墨分析 Api，以及手寫筆輸入 Api 的 COM 版本。 針對舊版 Tablet PC 技術所撰寫的應用程式，會在 Windows Vista 中執行，而不需要修改。

從 Windows Vista 版本開始，Tablet PC 技術元件僅提供 Windows SDK 的一部分。 如需詳細資訊，請參閱 [TABLET PC 開發的新功能](what-s-new-in-tablet-pc-development.md)。

### <a name="version-17"></a>版本1。7

Tablet PC 開發工具組1.7 擴充了版本1.5 提供的開發功能，並在 Web 上新增手寫筆輸入 Api 和筆墨支援。

在過去，1.5 版的功能是在不同的二進位檔中，但在 Tablet PC 開發工具組1.7 中，所有功能都放在一個單一二進位檔中。

### <a name="version-15"></a>1.5 版

版本1.5 的開發工具組已取代版本1.1。 它提供了畫筆輸入面板 Api 和分隔物件。

> [!Note]  
> 如果您安裝 Tablet PC 開發工具組1.5 版，在安裝之後，您必須在編譯和執行之前，在針對舊版 Tablet PC SDK 所撰寫的應用程式中重新建立 Microsoft ink 元件的參考。

 

### <a name="version-11"></a>1.1 版

版本1.1 的開發工具組已取代版本1.0。 版本1.1 版本僅由檔集的更新所組成;開發工具組的1.1 版與 Windows XP Tablet PC Edition 的隨附版本之間沒有變更平臺二進位檔。 因此，針對1.1 版開發工具組開發的應用程式不需要在安裝于 Tablet Pc 時，轉散發任何元件來使用平臺功能。

> [!Note]  
> 散佈至非 Tablet PC 作業系統的應用程式可以使用 Tablet PC 平臺功能的子集。 這些應用程式必須包含隨附于版本1.1 開發工具組及其設定的轉散發合併模組。

 

### <a name="version-10"></a>版本 1.0

1.1 版已取代開發工具組的1.0 版。

 

 
