---
title: 檔和檔週邊設備
description: Windows 7 為開發人員提供了一個健全的平臺，讓您可以使用檔和整合檔週邊設備。
ms.assetid: 77d27775-eea8-4739-a1d2-05fcf6590cef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e220949d37c17b95f92ed5026166ea71043354
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023879"
---
# <a name="documents-and-document-peripherals"></a>檔和檔週邊設備

Windows 7 為開發人員提供了一個健全的平臺，讓您可以使用檔和整合檔週邊設備。 Windows Vista 引進了兩種新的檔和儲存技術： XML 檔規格 (XPS) 和開放式封裝慣例 (OPC) 。 Windows Vista 中的這些技術（僅適用于透過 Microsoft .NET Framework 的 managed 程式碼應用程式開發人員）現已在 Windows 7software 開發工具組 (SDK) 供非受控碼開發人員使用。

## <a name="open-packaging-conventions"></a>開放式封裝慣例

Windows 7 支援所有的 OPC 檔案格式，包括來自 Microsoft 以及來自協力廠商的檔案格式。 OPC 是 Office Open XML 的元件， (OOXML) 透過 *ISO/IEC 29500* 和 *ECMA-376* 定義的國際規格。 根據 *ZIP* 檔案格式，OPC 可讓應用程式將資料項目組合儲存在單一封裝檔案中。 應用程式開發人員可以使用 Windows 7 中的 *封裝* api 來建立、讀取和操作 OPC 檔案中的多個資料元素。

在 Windows 7 中使用 *封裝* api，開發人員可以建立新的封裝格式，以容納應用程式特定的資料儲存需求。

*封裝* api 也支援 *X509* 數位簽章。 開發人員可以使用數位簽章功能來簽署和驗證 OPC 套件或整個封裝的選定部分。 應用程式可以使用數位簽章來偵測其檔的額外安全性層級，以在檔案簽署之後變更 OPC 檔案的內容時偵測。  (參閱 [開放式封裝慣例總覽](/previous-versions/windows/desktop/opc/open-packaging-conventions-overview)。 ) 

## <a name="xps-documents"></a>XPS 文件

Windows 應用程式開發人員可以建立使用 Windows 7 產生 XPS 檔的應用程式。 這可讓它們與檔周邊生態系統緊密整合 (裝置，例如掃描器和印表機) ，以及使用安全的電子檔來支援發行和封存。

在舊版的 Windows 中，Microsoft Win32 開發人員不支援 XPS。 XPS 是在 Windows Vista 中引進，但 API 介面僅限於使用 managed 程式碼的 .NET 開發人員。 有了 Windows 7，Win32 開發人員就可以使用新的 XPS *檔* api 來減少使用 xps 時所需的工作量。 由於 XPS 是新 Windows 列印平臺的基礎，因此這是很大的好處。

在舊版的 Windows 中，從 Win32 應用程式對 XPS 列印路徑的存取權僅限於驅動程式轉義。 這大幅減少了不使用 managed 程式碼的開發人員列印路徑的公用程式。 針對 Win32 開發人員，新的 XPS *列印* API 可大幅減少從 XPS 列印路徑獲益所需的工作量，並免除平行列印程式碼的需要。

應用程式開發人員可以使用 XPS 檔，以高精確度、有效率且值得信賴的格式，以電子檔形式共用和封存內容。 就像 Windows Vista 一樣，Windows 7 中的列印路徑建基於 XPS 格式，以提供增強的列印功能。 Windows 7 中的 XPS 檔 Api 可讓開發人員輕鬆地建立、存取和操作 XPS 檔。  (參閱 [XPS 檔程式設計指南](/previous-versions//dd372978(v=vs.85))。 ) 

![xps 檢視器](images/windows7-devguide-xpsviewer.jpg)

Windows 應用程式開發人員可以建立使用 Windows 7 產生 XPS 檔的應用程式

 

 