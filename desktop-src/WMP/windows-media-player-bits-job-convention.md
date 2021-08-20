---
title: Windows Media PlayerBITS 作業慣例
description: 如果您使用背景智慧型傳送服務 (BITS) ，Windows Media Player 可以自動下載數位媒體專案，並將其新增至程式庫。
ms.assetid: 643faba7-9af2-4292-8d92-e321d7690a5b
keywords:
- 'Windows Media Player 線上商店，背景智慧型傳送服務 (個位) '
- '線上商店、背景智慧型傳送服務 (位) '
- '輸入2個線上商店，背景智慧型傳送服務 (位) '
- 背景智慧型傳送服務 (BITS)
- 'BITS (背景智慧型傳送服務) '
- Windows Media Player 線上商店，BITS 作業慣例
- 線上商店，BITS 作業慣例
- 類型2線上商店，BITS 作業慣例
- BITS 作業慣例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afa62b3d5691abe6f91afde1cda4d83525159d2708cfde80d0ae3f23259003e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117931229"
---
# <a name="windows-media-player-bits-job-convention"></a>Windows Media PlayerBITS 作業慣例

如果您使用[背景智慧型傳送服務 (BITS) ](/windows/desktop/Bits/background-intelligent-transfer-service-portal)，Windows Media Player 可以自動下載數位媒體專案，並將其新增至程式庫。 若要利用這項功能，您必須將作業新增至 BITS 傳送佇列，並呼叫 **IBackgroundCopyJob：： SetDescription**，並提供使用正確格式的描述字串。

> [!Note]  
> 本章節描述專為線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

## <a name="syntax"></a>語法

``` syntax
::WMP_JOB:1:serviceId:Provider:AlbumArtist:AlbumTitle:TrackNumber:Title:Duration:Rating
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="serviceId"></span><span id="serviceid"></span><span id="SERVICEID"></span>*serviceId*
</dt> <dd>

Windows Media Player 用來識別服務的隨機產生32位值。

</dd> <dt>

<span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>*供應商*
</dt> <dd>

提供者名稱。 此值必須符合有效的線上商店金鑰名稱。

</dd> <dt>

<span id="AlbumArtist"></span><span id="albumartist"></span><span id="ALBUMARTIST"></span>*AlbumArtist*
</dt> <dd>

專輯的主要演出者名稱。

</dd> <dt>

<span id="AlbumTitle"></span><span id="albumtitle"></span><span id="ALBUMTITLE"></span>*AlbumTitle*
</dt> <dd>

專輯的標題。

</dd> <dt>

<span id="TrackNumber"></span><span id="tracknumber"></span><span id="TRACKNUMBER"></span>*TrackNumber*
</dt> <dd>

CD 曲目編號。

</dd> <dt>

<span id="Title"></span><span id="title"></span><span id="TITLE"></span>*標題*
</dt> <dd>

內容的標題。

</dd> <dt>

<span id="Duration"></span><span id="duration"></span><span id="DURATION"></span>*時間*
</dt> <dd>

內容的持續時間。

</dd> <dt>

<span id="Rating"></span><span id="rating"></span><span id="RATING"></span>*評級*
</dt> <dd>

內容的評等。

</dd> </dl>

## <a name="remarks"></a>備註

當 Windows Media Player 10 或更新版本使用 BITS 來下載內容時，它會列舉傳送佇列中的作業，並檢查每項作業的描述字串。 如果描述字串符合預期慣例，Windows Media Player 下載內容。

您只需新增一個數位媒體檔案，即可下載至每個 BITS 作業。

使用此慣例啟動 BITS 作業之後，您必須讓 Windows Media Player 完成工作。 Windows Media Player 也會從 BITS 佇列中移除工作、將下載的檔案移至儲存已翻錄音樂的位置，然後將下載的檔案新增至程式庫。

*ServiceId* 參數必須包含非零的32位值。 建議您使用函數 [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) 來建立這個值。

您使用 **IBackgroundCopyJob：： AddFile** 的 *localName* 參數指定的檔案名必須有 .wma、.wmv、.mp3 或 .asf 副檔名。

其餘的參數是設計來包含與內容相關的中繼資料值。 您可以使用 **DownloadItem getItemInfo**，從線上商店網頁取得這些值。 您可以藉由呼叫 **DownloadManager getDownloadCollection** ，並提供 *serviceId* 作為 *collectionId* 參數，來取得正確的下載集合。

Windows Media Player 會在播放程式執行時定期檢查 BITS 佇列。 為確保 Windows Media Player 檢查 BITS 佇列中的下載工作，您應該在下列登錄子機碼中建立一個值：

**HKEY \_ 目前的 \_ 使用者 \\ 軟體 \\ Microsoft \\ MediaPlayer \\ 服務**

此值應如下所示建立。



| 名稱                | 類型      | 描述                                                                                                                                                                                                          |
|---------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **RefreshDownload** | **DWORD** | 指定 Windows Media Player 是否應該檢查 BITS 佇列中的下載作業。 如果值為零，播放程式將不會檢查 BITS 佇列。 如果此值為非零值，則播放程式必須檢查佇列。 |



 

您可以使用下列替代語法來新增 Windows Media Player 未完成的 BITS 作業，但它只會顯示狀態資訊：

``` syntax
::WMP_STATUS:1:serviceId:Provider:AlbumArtist:AlbumTitle:TrackNumber:Title:Duration:Rating
```

使用上述語法時，您必須撰寫程式碼來完成 BITS 下載、在使用者的電腦上組織內容，並視需要將內容新增至程式庫。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[CryptGenRandom](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom)
</dt> <dt>

[**DownloadItem. getItemInfo**](downloaditem-getiteminfo.md)
</dt> <dt>

[**DownloadManager.getDownloadCollection**](downloadmanager-getdownloadcollection.md)
</dt> <dt>

[**類型 2 線上商店的參考**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 