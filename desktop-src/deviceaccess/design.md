---
title: 自訂裝置的設計考慮
description: 本主題說明可協助您判斷裝置是否需要自訂驅動程式的設計考慮。
ms.assetid: 8AADE304-4841-41E2-968B-DFCB5B954FF1
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: f503ae556009f3b4b9b88d9f895936218f402fc6
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "103684212"
---
# <a name="design-considerations-for-custom-devices"></a>自訂裝置的設計考慮

本主題說明可協助您判斷裝置是否需要自訂驅動程式的設計考慮。

- [判斷要執行的驅動程式類型](#determining-the-type-of-driver-to-implement)
- [安全性考量](#security-considerations)
- [相關主題](#related-topics)

## <a name="determining-the-type-of-driver-to-implement"></a>判斷要執行的驅動程式類型

下表說明您應該如何開發裝置的自訂驅動程式，並使用裝置存取 API 來與它通訊，以及您應該改用 Windows 提供的裝置堆疊。

| 若要支援 | 實作 |
|:---|:---|
| 知名的裝置，包括： <ul><li>Sensor</li><li>Location</li><li>網路攝影機</li><li>鄰近</li><li>短訊息服務 (SMS) </li><li>行動寬頻</li></ul><br/> | 對於許多類型的知名裝置，您不需要自訂驅動程式，因為 Windows 包含 Api 和類別延伸設備磁碟機介面 (DDIs) 管理驅動程式和 Windows 之間的通訊。 感應器、位置和 Windows 可攜式裝置 (WPD) 裝置是具有這項支援之裝置類別的一些範例。 如果您建立的驅動程式會使用其中一個 Windows 提供的 DDIs 來傳送和接收資料和命令，則您的 Windows Store 應用程式不需要使用裝置存取 API 來進行訊息代理程式存取，或將輸入/輸出 (i/o) 控制程式代碼直接傳送到驅動程式。 <br/> 當 Windows Store 應用程式使用適用于其裝置類別的 Windows 執行階段 API 來要求已知裝置的存取權時，Windows 8 會根據裝置的類型來處理裝置存取。 應用程式一律會存取某些知名的裝置類型 (例如加速計) ，而不會顯示任何個人識別資訊。 其他類型的知名裝置必須在應用程式資訊清單中宣告，應用程式才能存取它們。 使用者必須授與許可權，應用程式才能存取可顯示機密資訊的裝置，例如位置、網路攝影機和麥克風裝置，或可能需要支付使用者的費用，例如行動寬頻裝置。 <br/> |
| 執行 MTP 服務的 WPD 裝置。<br/> | 您可以使用 MTP 類別驅動程式，也可以使用 WPD 的 DDI 來建立驅動程式。<br/> Windows 8 提供 MTP 裝置服務的支援。而且，應用程式可以使用 [Windows. 便攜](/uwp/api/Windows.Devices.Portable) Windows 執行階段 API、可攜式裝置元件物件模型 (COM) API 或 WPD 自動化來存取裝置。 您的應用程式不需要使用裝置存取 API。<br/> |
| 沒有 Windows 提供的類別擴充或類別驅動程式的裝置。<br/>  | 在此情況下，請參閱適用于專用裝置之 [內部裝置的 UWP 裝置應用程式](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) ，以判斷您是否必須使用裝置存取 API 來執行自訂的驅動程式存取。<br/> |

## <a name="security-considerations"></a>安全性考量

下列文章提供撰寫安全 c + + 程式碼的指引：

- [C + + 的安全性最佳作法](/cpp/security/security-best-practices-for-cpp)
- [適用于應用程式的模式 & 實務安全性指引]/previous-versions/msp-n-p/ff650760 (v = pandp. 10) ) 

## <a name="related-topics"></a>相關主題

[自訂驅動程式存取範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample)、 [適用于內部裝置的 UWP 裝置應用程式](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices)、 [硬體開發人員中心](/windows-hardware/drivers/)
