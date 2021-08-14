---
title: 計量內容使用方式
description: 計量內容使用方式
ms.assetid: f87b5d95-a497-4356-817f-49ac3819df08
keywords:
- Windows媒體裝置管理員，計量內容使用方式
- 裝置管理員，計量內容使用方式
- 程式設計指南，計量內容使用方式
- 桌面應用程式，計量內容使用方式
- 建立 Windows 媒體裝置管理員應用程式、計量內容使用方式
- 計量內容使用方式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029bae2bcdd69f9dc58c4a64317f974538c672b1d27597fbdc1915074aff0278
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957198"
---
# <a name="metering-content-usage"></a>計量內容使用方式

使用 Windows 媒體10技術，您現在可以計量可攜式裝置上的內容使用方式。 如果 Windows 媒體10授權允許計量，則裝置可以儲存歌曲的播放次數，並透過網際網路將使用量上傳回授權簽發者。 此系統可讓內容提供者藉由精確地測量內容使用方式，來調整其特許費用。

若要計量內容，應用程式必須具有以 Windows 媒體版權管理員 10 SDK 上建的授權服務所提供的計量憑證。 只有這個相同服務所授權的內容可以進行計量。 如需有關計量運作方式以及如何建立授權計量服務的詳細資訊，請參閱 MSDN 上的[Windows Media Rights Manager SDK 檔](/previous-versions/ms986509(v=msdn.10))。 您可以藉由填寫[Windows 媒體授權頁面](https://www.microsoft.com/licensing/default)上的必要資訊來取得 SDK。

應用程式可以內建計量，或者，如果應用程式接受計量外掛程式，您可以為現有的應用程式（例如 Windows Media Player）建立 COM 外掛程式。

應用程式應該在內容使用方式會進行計量時警告使用者。 如需詳細資訊，請參閱 [隱私權聲明](privacy-statement.md)中列出的 Microsoft 網頁。

從裝置取得計量資料可能很慢。 因此，如果應用程式計量使用量，則應該經常這麼做，以防止大量資料在裝置上累積，並減緩資料傳送速率。 為了避免資料傳送速率太慢，裝置製造商可以傳送可用計量資料的子集。 應用程式應監視 [**IWMDRMDeviceApp：:P rocessmeterresponse**](iwmdrmdeviceapp-processmeterresponse.md) 所抓取的旗標，以查看是否有任何其他計量資料仍保留在裝置上。

下列步驟顯示應用程式如何測量內容的使用方式。

1.  由於計量僅適用于支援可攜式裝置 Windows 媒體 DRM 10 的裝置，因此您的應用程式應該會在某個時間點呼叫 **QueryDeviceStatus**（如 [處理應用程式中受保護的內容](handling-protected-content-in-the-application.md)所述），以確保裝置有效且為最新狀態。
2.  藉由呼叫 [**IWMDRMDeviceApp：： GenerateMeterChallenge**](iwmdrmdeviceapp-generatemeterchallenge.md)，要求來自裝置的計量資訊。
3.  將已取出的計量資料傳送至 **GenerateMeterChallenge** 所抓取之 URL 的計量服務。 傳送至服務的資料格式取決於該特定服務的腳本。 例如，某些服務可能需要以 POST 命令形式傳送的資料做為名稱/值組。 服務提供者應可讓您知道其特定的格式需求。
4.  取得計量服務的回應，並呼叫 [**IWMDRMDeviceApp：:P rocessmeterresponse**](iwmdrmdeviceapp-processmeterresponse.md)將其傳送至裝置。 這會導致裝置重設播放次數，也會傳回一個值，指出裝置上是否有更多的計量資料，應該再次呼叫 **GenerateMeterChallenge** 來取出。

如需計量的詳細資訊和範例程式碼，請參閱[Windows 媒體](/previous-versions//bb614723(v=vs.85))網站。

 

 