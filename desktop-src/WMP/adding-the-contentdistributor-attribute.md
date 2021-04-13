---
title: 加入 ContentDistributor 屬性
description: 加入 ContentDistributor 屬性
ms.assetid: b4ba5c9b-f28f-4275-bd39-c0ad1080d122
keywords:
- Windows Media Player 線上商店，加入 ContentDistributor 屬性
- 線上商店，加入 ContentDistributor 屬性
- 輸入1個線上商店，加入 ContentDistributor 屬性
- 輸入2個線上商店，加入 ContentDistributor 屬性
- Windows Media Player 線上商店，ContentDistributor 屬性
- 線上商店、ContentDistributor 屬性
- 輸入1個線上商店，ContentDistributor 屬性
- 類型2線上商店，ContentDistributor 屬性
- 加入 ContentDistributor 屬性
- ContentDistributor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1636c002affbcf1235283a22f7eb060c75f24a81
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300928"
---
# <a name="adding-the-contentdistributor-attribute"></a>加入 ContentDistributor 屬性

當使用者嘗試播放線上商店內容或將內容複寫到 CD 或裝置時，Windows Media Player 會呼叫 COM 物件中的特定方法。 若要這樣做，播放程式需要一種方式來區別您的內容與其他線上商店提供者的內容。 藉由將您的線上商店金鑰名稱新增為 **ContentDistributor** (的值，這是 Windows MEDIA Format SDK 屬性的別名（名為 **WM/ContentDistributor**) Attribute）至 windows media 內容，您可以確定播放程式可以識別與您的服務相關聯的內容。

為 **ContentDistributor** 新增值也可確保 Windows Media Player 將會在程式庫中為您提供的內容建立節點。 請參閱連結 [庫整合](library-integration.md)。

您可以透過兩種方式來指定此值：

-   使用 Windows Media Player 物件模型。 當您這樣做時，Windows Media Player 會將您指定的值加入至程式庫資料庫。 最後，播放玩家也會將屬性值寫入數位媒體檔案。
-   使用 Windows Media Format SDK 以程式設計方式新增 **WM/ContentDistributor** 屬性。 當您這樣做時，Windows Media Player 會在將數位媒體檔案新增至程式庫時，讀取屬性值並將它新增至資料庫。

建立您的線上商店 COM 物件時，您為 **ContentDistributor** 設定的檔案屬性值以及指派給 yourproject。中常數 kszContentDistributorID 的值必須完全相符。 回想一下，當您使用專案嚮導建立專案時，您已為 COM 物件指定此常數值。 您可以手動變更此值。 請務必使用可唯一識別服務的字串。

## <a name="using-the-windows-media-player-object-model"></a>使用 Windows Media Player 物件模型

若要使用 Windows Media Player 物件模型指定 **ContentDistributor** 的值，請使用 [setItemInfo](media-setiteminfo.md) 方法。 下列程式碼範例會針對目前播放的媒體專案，指定 **ContentDistributor** 的 "Proseware" 值：


```C++
// Retrieve the current media item.
var theMedia = Player.currentMedia;

//Test whether the media item was retrieved.
if(theMedia)
{
    // Set the ContentDistributor value.
    theMedia.setItemInfo("ContentDistributor", "Proseware");
}
```



## <a name="using-the-windows-media-format-sdk"></a>使用 Windows Media Format SDK

Windows Media Player SDK 包含名為 SetContentDistributor 的範例 c + + 檔案，其示範如何使用 Windows Media Format 9 系列 SDK 來新增 **WM/ContentDistributor** 屬性。 您可以在安裝 SDK 的名稱為 Metadata 的資料夾中找到這個範例檔案。 若要使用此程式碼，您必須遵循下列步驟：

1.  安裝 Windows Media Format 9 系列 SDK 並設定執行時間，如檔中所述。
2.  在 Visual Studio 中建立新的空白 c + + 專案，並將名為 SetContentDistributor 的範例檔案新增至專案。
3.  將 Windows Media Format 9 系列 SDK Lib 資料夾的路徑新增至您的檔案路徑清單。 從 [工具]  功能表選擇 [選項] 。
4.  在 [ **選項** ] 對話方塊中，按一下 [ **專案**]，然後按一下 [ **VC + + 目錄**]。
5.  在 [ **顯示目錄** ] 下拉式清單方塊中，按一下 [連結 **庫** 檔案]。
6.  使用按鈕將路徑新增至清單方塊。
7.  開啟專案的 [屬性頁] 對話方塊。 選擇 [設定 **屬性**]、[ **連結器**]，然後 **輸入**。 在 [ **其他** 相依性] 文字方塊中輸入 "wmvcore"。

範例程式碼會建立命令列程式。 您在執行程式時提供的引數會指定要修改之數位媒體檔案的路徑，以及 **ContentDistributor** 屬性值的字串。 程式碼會使用 **IWMHeaderInfo：： SetAttribute** ，將屬性新增至您指定的檔案。 您可以使用此範例，或使用它作為您自己的程式的起點。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Type 1 和 Type 2 線上商店的一般資訊**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




