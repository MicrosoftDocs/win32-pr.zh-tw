---
title: '具有多個值的屬性 (Windows Media Format 11 SDK) '
description: 深入瞭解 Windows Media Format 11 SDK 中具有多個值的屬性。 某些媒體專案屬性可以有多個值。
ms.assetid: 2e65c5d0-6f5e-45a4-8e13-9e49da007145
keywords:
- Windows Media Format SDK，屬性
- Advanced Systems Format (ASF) 、屬性
- ASF (Advanced 系統格式) ，屬性
- 屬性，多個值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9466cd3f993cc1b12f27bc162e5188e6d45404b
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262690"
---
# <a name="attributes-with-multiple-values-windows-media-format-11-sdk"></a>具有多個值的屬性 (Windows Media Format 11 SDK) 

某些預先定義的屬性可以有多個指派的值。 例如，「 **演出者** 」是可以有多個值的屬性。 您可以呼叫 [**IWMHeaderInfo3：： AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) 多次，以依您的需求新增多個 **演出者** 值。 如果您對不支援多個值的屬性進行多個 **AddAttribute** 呼叫，方法可能會傳回錯誤碼，或直接忽略您的要求。

下表列出支援多個值的屬性。 某些屬性只能在 ASF 檔案中有多個值，而其他屬性在 ASF 和 MP3 檔案中可以有多個值。



| 屬性                                                 | 支援多個值 |
|-----------------------------------------------------------|-----------------------------|
| [**作者**](author.md)                                  | ASF、MP3                    |
| [**WM/AlbumArtist**](wm-albumartist.md)                  | ASF                         |
| [**WM/AlbumCoverURL**](wm-albumcoverurl.md)              | ASF                         |
| [**WM/類別**](wm-category.md)                        | ASF                         |
| [**WM/編輯器**](wm-composer.md)                        | ASF、MP3                    |
| [**WM/導體**](wm-conductor.md)                      | ASF                         |
| [**WM/Director**](wm-director.md)                        | ASF                         |
| [**WM/內容類型**](wm-genre.md)                              | ASF                         |
| [**WM/GenreID**](wm-genreid.md)                          | ASF                         |
| [**WM/語言**](wm-language.md)                        | ASF、MP3                    |
| [**WM/歌詞 \_ 內容**](wm-lyrics-synchronised.md) | ASF、MP3                    |
| [**WM/情緒**](wm-mood.md)                                | ASF、MP3                    |
| [**WM/圖片**](wmpicture.md)                           | ASF、MP3                    |
| [**WM/生產者**](wm-producer.md)                        | ASF                         |
| [**WM/PromotionURL**](wm-promotionurl.md)                | ASF                         |
| [**WM/UserWebURL**](wm-userweburl.md)                    | ASF、MP3                    |
| [**WM/Writer**](wm-writer.md)                            | ASF、MP3                    |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**屬性**](attributes.md)
</dt> </dl>

 

 




