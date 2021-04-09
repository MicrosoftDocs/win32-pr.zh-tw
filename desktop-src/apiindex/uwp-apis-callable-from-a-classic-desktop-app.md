---
description: 一般規則是桌面應用程式可以呼叫 Windows 執行階段 (WinRT) API。 不過，某些 Api （包括 XAML UI Api）要求呼叫應用程式必須有套件身分識別。
ms.assetid: F3808C28-72DE-49B5-A389-EB085EFC02CC
title: 從桌面應用程式呼叫的 WinRT Api
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9083fbfb16391c626f49b79176fed7a81068c028
ms.sourcegitcommit: 0c786b1682063d0cae0fc43180945183fa2c7981
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/24/2020
ms.locfileid: "104024319"
---
# <a name="calling-winrt-apis-from-a-desktop-app"></a>從桌面應用程式呼叫 WinRT Api

一般規則是桌面應用程式可以呼叫 WinRT API。 不過，某些 Api （包括 XAML UI Api）要求呼叫應用程式必須有套件身分識別。 UWP 應用程式具有妥善定義的應用程式模型，且具有套件身分識別。 其他類型的桌面應用程式都沒有妥善定義的應用程式模型，也沒有套件身分識別。 因此，如果 API 需要套件身分識別，WPF、Windows Forms 或 Win32 應用程式就無法呼叫它，除非應用程式 [封裝在 MSIX 套件中](/windows/msix/desktop/desktop-to-uwp-root)。

## <a name="the-dualapipartition-attribute"></a>DualApiPartition 屬性

當您想要從桌面應用程式呼叫特定的 WinRT 時，這就是要遵循的流程。 此程式會回答問題，指出是否允許從桌面應用程式呼叫 API。 首先，請造訪 [Windows 執行階段 apps 的 WINDOWS API 參考](/uwp/)、找出您感興趣之類別或成員 API 的參考主題，並檢查 [**DualApiPartition**](/uwp/api/Windows.Foundation.Metadata.DualApiPartitionAttribute) 屬性是否列在 [屬性] 區段中。

## <a name="if-the-dualapipartition-attribute-is-listed"></a>如果已列出 DualApiPartition 屬性

如果列出 DualApiPartition 屬性，則 API 不需要呼叫應用程式具有套件身分識別，且可從任何傳統型應用程式呼叫 API。 [**Geolocator**](/uwp/api/Windows.Devices.Geolocation.Geolocator) 是一個範例;應用程式不需要唯一識別，即可執行位置工作。

## <a name="if-the-dualapipartition-attribute-is-not-listed"></a>如果未列出 DualApiPartition 屬性

如果未列出 DualApiPartition 屬性，則 API 會要求呼叫應用程式必須有套件身分識別。 因此，除非應用程式已轉換成 UWP 應用程式，否則不允許 WPF、Windows Forms 或 Win32 應用程式呼叫 API。 例如，您可以使用 [...][**按鈕**](/uwp/api/Windows.UI.Xaml.Controls.Button)。
