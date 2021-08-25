---
title: 適用于 Visual Basic .net 和 C 的介面
description: Visual Basic .net 和 C 的介面 \
ms.assetid: c66f1e03-20eb-45b1-8710-be9eae63e7ad
keywords:
- Windows Media Player，介面
- Windows Media Player行動裝置，介面
- Windows Media Player 物件模型，介面
- 物件模型，介面
- ActiveX 控制項，介面
- Windows Media Player ActiveX 控制項、介面
- Windows Media PlayerMobile ActiveX 控制項、介面
- 物件模型、介面的參考
- 介面物件模型參考
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a7024c60235b0a545463826fc8948adf3716c9c2d5b491414212d788087404b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862578"
---
# <a name="interfaces-for-visual-basic-net-and-c"></a>適用于 Visual Basic .net 和 C 的介面#

本節記載由 Windows Media Player ActiveX 控制項公開的介面。

[AxWindowsMediaPlayer 物件](axwindowsmediaplayer-object--vb-and-c.md)的數個屬性和方法是用來取出特定介面。 這些介面接著可能具有屬性和存取子方法，可供您抓取進一步的介面。

Windows Media Player 控制項會公開下列介面。



| 介面                                                      | 描述                                                                                                                                                       |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IWMPCdrom](iwmpcdrom--vb-and-c.md)                           | 存取磁片磁碟機中的 CD 或 DVD。                                                                                                                                  |
| [IWMPCdromBurn](iwmpcdromburn--vb-and-c.md)                   | 提供用來管理建立音訊 Cd 的屬性和方法。                                                                                                     |
| [IWMPCdromCollection](iwmpcdromcollection--vb-and-c.md)       | 存取 CD 或 DVD 光碟機的集合。                                                                                                                        |
| [IWMPCdromRip](iwmpcdromrip--vb-and-c.md)                     | 提供屬性和方法來管理從音訊 CD 複製或 *翻錄* 的曲目。                                                                         |
| [IWMPClosedCaption](iwmpclosedcaption--vb-and-c.md)           | 提供一種方式，可包含包含數位媒體檔案的標題。                                                                                                     |
| [IWMPClosedCaption2](iwmpclosedcaption2--vb-and-c.md)         | 提供其他隱藏式輔助字幕屬性和方法。                                                                                                     |
| [IWMPControls](iwmpcontrols--vb-and-c.md)                     | 代表 Windows Media Player 的傳輸控制項，例如播放、停止和暫停。                                                                         |
| [IWMPControls2](iwmpcontrols2--vb-and-c.md)                   | 提供額外的控制方法，以在下一個或上一個框架凍結播放。                                                                           |
| [IWMPControls3](iwmpcontrols3--vb-and-c.md)                   | 提供其他控制項屬性和方法，以供選取及支援音訊語言。                                                                      |
| [IWMPDVD](iwmpdvd--vb-and-c.md)                               | 提供使用 Dvd 的屬性和方法。                                                                                                            |
| [IWMPError](iwmperror--vb-and-c.md)                           | 存取 [IWMPErrorItem](iwmperroritem--vb-and-c.md) 介面的集合，以取得錯誤資訊。                                                |
| [IWMPErrorItem](iwmperroritem--vb-and-c.md)                   | 提供錯誤資訊的存取。                                                                                                                             |
| [IWMPErrorItem2](iwmperroritem2--vb-and-c.md)                 | 提供可取得錯誤條件程式碼的其他錯誤專案屬性。                                                                                   |
| **IWMPFolderMonitorServices**                                  | 不支援 .NET 程式設計。                                                                                                                               |
| [IWMPLibrary](iwmplibrary--vb-and-c.md)                       | 代表程式庫。                                                                                                                                             |
| [IWMPLibraryServices](iwmplibraryservices--vb-and-c.md)       | 提供列舉程式庫的方法。                                                                                                                          |
| **IWMPLibrarySharingServices**                                 | 不支援 .NET 程式設計。                                                                                                                               |
| [IWMPMedia](iwmpmedia--vb-and-c.md)                           | 提供一種方式來設定和取出媒體專案的屬性。                                                                                                |
| [IWMPMedia2](iwmpmedia2--vb-and-c.md)                         | 提供其他媒體專案屬性的存取權。                                                                                                             |
| [IWMPMedia3](iwmpmedia3--vb-and-c.md)                         | 提供其他方法來存取媒體專案的屬性。                                                                                             |
| [IWMPMediaCollection](iwmpmediacollection--vb-and-c.md)       | 提供可用於組織大型媒體專案集合的方法。                                                                                  |
| [IWMPMediaCollection2](iwmpmediacollection2--vb-and-c.md)     | 提供補充 **IWMPMediaCollection** 介面的方法。                                                                                           |
| [IWMPMetadataPicture](iwmpmetadatapicture--vb-and-c.md)       | 提供屬性，以取得以 **WM/圖片** 中繼資料屬性工作表示之數位媒體檔案中包含之影像的相關資訊。         |
| [IWMPMetadataText](iwmpmetadatatext--vb-and-c.md)             | 提供屬性，以取得複雜文字中繼資料屬性的相關資訊。                                                                            |
| [IWMPNetwork](iwmpnetwork--vb-and-c.md)                       | 提供屬性和方法來存取與網路連接品質相關的統計資料，以及指定和取出網路 proxy 設定。     |
| **IWMPPlayerApplication**                                      | 不支援 .NET 程式設計。                                                                                                                               |
| **IWMPPlayerServices**                                         | 不支援 .NET 程式設計。                                                                                                                               |
| **IWMPPlayerServices2**                                        | 不支援 .NET 程式設計。                                                                                                                               |
| [IWMPPlaylist](iwmpplaylist--vb-and-c.md)                     | 提供屬性和方法來組織、管理和操作播放清單中的媒體專案。                                                                    |
| [IWMPPlaylistArray](iwmpplaylistarray--vb-and-c.md)           | 依索引編號存取 [IWMPPlaylist](iwmpplaylist--vb-and-c.md) 介面的集合。                                                                   |
| [IWMPPlaylistCollection](iwmpplaylistcollection--vb-and-c.md) | 提供在集合中操作 [IWMPPlaylist](iwmpplaylist--vb-and-c.md) 和 [IWMPPlaylistArray](iwmpplaylistarray--vb-and-c.md) 介面的方法。 |
| [IWMPQuery](iwmpquery--vb-and-c.md)                           | 表示複合查詢。                                                                                                                                      |
| [IWMPSettings](iwmpsettings--vb-and-c.md)                     | 提供屬性和方法，以取得或設定 Windows Media Player 設定的值。                                                                      |
| [IWMPSettings2](iwmpsettings2--vb-and-c.md)                   | 提供可補充 **IWMPSettings** 介面的屬性和方法。                                                                                  |
| [IWMPStringCollection](iwmpstringcollection--vb-and-c.md)     | 提供屬性和方法，以依索引編號存取字串集合。                                                                           |
| [IWMPStringCollection2](iwmpstringcollection2--vb-and-c.md)   | 提供補充 **IWMPStringCollection** 介面的方法。                                                                                          |
| **IWMPSyncDevice**                                             | 不支援 .NET 程式設計。                                                                                                                               |
| **IWMPSyncDevice2**                                            | 不支援 .NET 程式設計。                                                                                                                               |
| **IWMPSyncServices**                                           | 不支援 .NET 程式設計。                                                                                                                               |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Visual Basic .net 和 C 的物件模型參考#**](object-model-reference-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 




