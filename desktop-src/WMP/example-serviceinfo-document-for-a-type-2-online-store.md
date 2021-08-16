---
title: Type 2 線上商店的範例 ServiceInfo 檔
description: Type 2 線上商店的範例 ServiceInfo 檔
ms.assetid: d9bbce89-15b4-495f-8995-24dda99a4f40
keywords:
- Windows Media Player 線上商店，範例 ServiceInfo 檔
- 線上商店，範例 ServiceInfo 檔
- 類型2線上商店，範例 ServiceInfo 檔
- Windows Media Player 線上商店，ServiceInfo 檔
- 線上商店，ServiceInfo 檔
- 輸入2個線上商店、ServiceInfo 檔
- Windows Media Player 線上商店，程式碼範例
- 線上商店，程式碼範例
- 類型2線上商店，程式碼範例
- 範例 ServiceInfo 檔
- ServiceInfo 檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7962f7548f8c880e60320d3a7fb071e2a076ffafdac9a56b4cf6d8aa41b5d60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650118"
---
# <a name="example-serviceinfo-document-for-a-type-2-online-store"></a>Type 2 線上商店的範例 ServiceInfo 檔

下列程式碼範例顯示完整的 ServiceInfo.xml 檔。 您可以使用這個 XML 做為您自己的 ServiceInfo 檔的起點。


```C++
<?xml version="1.0" encoding="utf-8" ?>
<ServiceInfo Version="1.00" Key="Proseware">
    <FriendlyName>Proseware Service</FriendlyName>
    <Image 
        MenuURL = "https://www.proseware.com/service/images/menuicon.jpg"
        ServiceLargeURL = "https://www.proseware.com/service/images/30x30.jpg" />
    <Color
        MediaPlayer = "#FF8040"
        MediaPlayerText = "#FFFFFF"/>
    <ServiceTask1
        URL = "https://www.proseware.com/service/html/Music.asp">
        <ButtonText>Proseware\nMusic</ButtonText>
        <ButtonTip>Proseware Music Store</ButtonTip>
    </ServiceTask1>
    <ServiceTask2
        URL = "https://www.proseware.com/service/html/Video.asp">
        <ButtonText>Proseware\nVideo</ButtonText>
        <ButtonTip>Proseware Video</ButtonTip>
    </ServiceTask2>
    <ServiceTask3
        URL = "https://www.proseware.com/service/html/Radio.asp">
        <ButtonText>Proseware\nRadio</ButtonText>
        <ButtonTip>Proseware Radio</ButtonTip>
    </ServiceTask3>
    <Navigate
        BaseURL = "https://www.proseware.com/service/html/navigate.asp">
    </Navigate>
    <InfoCenter
        URL = "https://www.proseware.com/service/html/InfoCenter.asp"/>
    <AlbumInfo
        URL = "https://www.proseware.com/service/html/AlbumInfo.asp"/>
    <BuyCD
        MediaPlayerURL = "https://www.proseware.com/service/html/BuyCDMediaPlayer.asp"
        MediaCenterURL = "https://www.proseware.com/service/html/BuyCDMediaCenter.asp"
        BrowserURL = "https://www.proseware.com/service/html/BuyCDBrowser.asp"/>
    <DownloadStatus
        URL = "https://www.proseware.com/service/html/Music_Download.htm"/>
    <HTMLView
        BaseURL = "https://www.proseware.com/"/>
</ServiceInfo>

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Type 2 線上商店的程式設計指南**](programming-guide-for-type-2-online-stores.md)
</dt> <dt>

[**適用于 Type 2 線上商店的 ServiceInfo 檔**](serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**ServiceInfo 檔**](serviceinfo-document.md)
</dt> </dl>

 

 




