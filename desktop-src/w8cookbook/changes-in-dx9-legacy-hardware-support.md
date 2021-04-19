---
title: DX9 舊版硬體支援的變更
description: DX9 舊版硬體支援的變更
ms.assetid: 25C7DFC7-58F4-4F6D-8D26-6DBA92424A0B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc1ae5c4b15a2019450cc5b209f34561d8ec672d
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "106966893"
---
# <a name="changes-in-dx9-legacy-hardware-support"></a>DX9 舊版硬體支援的變更

## <a name="platform"></a>平台

**用戶端** – Windows 8 


## <a name="description"></a>Description

Intel 和 AMD/ATI 不再支援其 DX9 圖形元件，也不會更新這些裝置的驅動程式以進行 Windows 8。 此外，這些裝置不會涵蓋 Windows 8 的現成討論。 這些裝置的最後一個驅動程式是在 WU 和 OEM/IHV 網站上提供的驅動程式;來自 Vista 的許多日期，而這些最終版本驅動程式當中有許多是 Windows 8 的問題。 此外，nVidia 最近也指出，它們不支援 DX9 (Vista 和舊版) mobile (筆記本) 部分進行 Windows 8。 它們會繼續支援其桌面 DX9 元件。

這些驅動程式/元件組合全都位於 Internet Explorer 9 軟體回復清單上。 這表示基於效能或穩定性的原因，Internet Explorer 9 在這些裝置上使用軟體轉譯。 這是很好的指示，Windows Store 應用程式的使用體驗對這些驅動程式和元件並不滿意。

## <a name="manifestation"></a>表現

因為這些裝置沒有任何現成的支援，所以具有這些元件的許多使用者將會在 Microsoft 基本顯示器驅動程式上執行。 這是以變形為基礎的 WDDM 1.2 軟體 GPU，其實比這個類別的部分部分更快，例如 Intel GMA500 系列) 。 它支援 aero 玻璃和 DWM，並且可以執行 Windows Store 應用程式。

不過，它有一些重要的限制：

-   它不支援多個監視器或投影
-   它不支援睡眠，但支援休眠
-   它通常不允許變更螢幕解析度

## <a name="mitigation"></a>降低

測試之後，如果您發現使用者體驗無法接受，您可以選擇設定其產品的硬體需求，以排除這些較舊的 DX9 Intel 和 AMD 元件。 您也可以選擇對客戶發出警示，讓他們在這些部分上可能會有無法接受的體驗。

## <a name="tests"></a>測試

評估這些裝置的效能和體驗：

-   最終可用驅動程式版本的體驗為何？
-   MSBDD 上的體驗為何？

 

 




