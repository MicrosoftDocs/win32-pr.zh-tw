---
title: 關於裝置存取 API
description: 裝置存取 API 適用于建立 Windows Store 應用程式的 c + + 開發人員，以便與 Windows 8 中的特殊裝置互動。
ms.assetid: DDF115A2-A811-450A-80F7-AAFB0EEA4037
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 213c7ecc618e4b183ee879d23db3b2c0eca35397
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "104316729"
---
# <a name="about-the-device-access-api"></a>關於裝置存取 API

裝置存取 API 適用于建立 Windows Store 應用程式的 c + + 開發人員，以便與 Windows 8 中的特殊裝置互動。 本主題說明裝置存取 API 適用的案例。 此外，也會說明裝置存取 API 如何在 Windows 8 中套用 Windows Store 應用程式的安全性規則。

- [在 Windows Store 裝置應用程式中啟用自訂裝置功能](#enabling-custom-device-functionality-in-windows-store-device-apps)

## <a name="enabling-custom-device-functionality-in-windows-store-device-apps"></a>在 Windows Store 裝置應用程式中啟用自訂裝置功能

獨立硬體廠商的開發人員 (Ihv) 和 Oem 可以建立與裝置配對的 Windows Store 應用程式，並在安裝裝置時自動取得。 此應用程式（稱為 Windows Store 裝置應用程式）可以提供獨特的裝置功能。

沒有內建類別驅動程式或 Windows 執行階段 Api 可在 Windows 8 中與裝置通訊的裝置稱為 *特製化裝置*。 這些裝置可能需要自訂驅動程式。 如需有關需要自訂驅動程式之裝置類型的詳細資訊，請參閱 Windows Store 裝置應用程式設計指南中的專用裝置。

必須與裝置的自訂驅動程式通訊之特製化裝置的 Windows Store 裝置應用程式，無法使用 Microsoft Win32 Api （例如 [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) 和 [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) ）將 IOCTLs 傳送至裝置。 Windows Store 裝置應用程式執行的受限安全性環境需要您使用裝置存取 API，才能從 Windows Store 應用程式與您的自訂驅動程式進行通訊。

自訂裝置的開發人員會限制存取核准的特殊許可權應用程式。 比方說，media player 裝置的製造商可能會想要讓使用者只能透過 IHV 提供的音樂應用程式播放音樂，並限制任何競爭者的應用程式從裝置同步媒體。 當您建立設備磁碟機時，您可以在資訊 (INF 中設定屬性) fileto 指定只有特殊許可權的應用程式才能存取裝置。 裝置本身的中繼資料會指定已核准的應用程式集的套件識別碼。 如需在裝置上設定此中繼資料的程式詳細資訊，請參閱 [內部裝置的 UWP 裝置應用程式](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) 。

## <a name="related-topics"></a>相關主題

[自訂驅動程式存取範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample)、 [適用于內部裝置的 UWP 裝置應用程式](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices)、 [硬體開發人員中心](/windows-hardware/drivers/)