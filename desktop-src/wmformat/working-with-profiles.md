---
title: 使用設定檔
description: 使用設定檔
ms.assetid: e1e31632-0db7-47db-a992-f5db9d8824c1
keywords:
- Windows媒體格式 SDK，設定檔
- Windows媒體格式 SDK，IWMCodecInfo3 介面
- 設定檔，關於
- 設定檔，Windows 媒體格式 SDK
- 設定檔，IWMCodecInfo3
- IWMCodecInfo3，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68982a47b743aaa12397e937ad9bd213fbd7ac0a78b41087d01929c1d42bb622
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055428"
---
# <a name="working-with-profiles"></a>使用設定檔

本節說明如何設計、建立和修改設定檔。 每個設定檔都會描述組成檔案的資料流程，以及彼此之間的關聯性。 設定檔物件包含每個資料流程的資料流程設定資訊、無法同時傳遞的資料流程的相互排除資訊、頻寬共用資訊，以及串流優先順序資訊。

設定檔的主要用途是將資料流程設定資訊提供給寫入器物件。 寫入器會使用設定檔中的資訊，與編解碼器進行協調以壓縮輸入。 當您設定壓縮的媒體資料流程時，您會指定用來壓縮資料的編解碼器，以及編解碼器使用的設定。 您也可以建立未壓縮資料流程的設定檔。 支援數個未壓縮的資料流程類型。 雖然它們不需要編解碼器，但這些類型對串流設定有自己的需求。 如需詳細資訊，請參閱設定 [資料流程](configuring-streams.md) 和 [使用未壓縮的音訊和影片串流](using-uncompressed-audio-and-video-streams.md)。

使用其中一個 Windows 媒體編解碼器的資料流程設定資訊，必須使用 [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3)介面的方法從編解碼器取得。 針對視頻編解碼器，使用串流格式的程式與音訊編解碼器的程式不同，但在這兩種情況下，您都必須從編解碼器取得格式開始。 您永遠不應該嘗試使用其中一個 Windows 媒體編解碼器來手動設定串流，因為設定檔中的小錯誤可能會對 ASF 檔案產生深遠的影響。

建立及/或修改設定檔的基本步驟如下：

1.  建立空的設定檔，或載入現有的設定檔以進行編輯。
2.  若有需要，請根據從將用來編碼串流的編解碼器所支援的設定檔資料，設定每個資料流程。
3.  如有需要，請設定相互排除。
4.  視需要設定頻寬共用。
5.  在檔案中設定資料流程的優先順序（如有需要）。

下列各節說明建立和編輯設定檔的程式。



| 區段                                                        | 描述                                                                                        |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [設計設定檔](designing-profiles.md)                   | 說明如何設計設定檔。                                                                 |
| [建立設定檔](creating-profiles.md)                     | 說明如何建立空白的設定檔。                                                          |
| [設定資料流程](configuring-streams.md)                 | 描述如何設定資料流程，並將它們包含在設定檔中。                                  |
| [使用相互排除](using-mutual-exclusion.md)           | 描述如何建立相互排除物件，並將它們包含在設定檔中。                    |
| [使用頻寬共用](using-bandwidth-sharing.md)         | 說明如何使用設定檔中的頻寬共用。                                               |
| [使用資料流程優先順序](using-stream-prioritization.md) | 描述如何在設定檔中使用資料流程優先權。                                           |
| [正在儲存設定檔](saving-profiles.md)                         | 說明如何將自訂設定檔儲存至檔案。                                              |
| [使用系統設定檔](using-system-profiles.md)             | 描述如何使用系統設定檔，以節省建立設定檔的時間和精力。           |
| [管理封包大小](managing-packet-size.md)               | 討論如何在使用您的設定檔所建立的檔案資料流程中控制封包大小。 |



 

**注意** 舊版 Windows 媒體格式 SDK 的使用者可能習慣使用系統設定檔，而不需要修改來建立其檔案。 Windows 媒體格式9系列 SDK 或更新版本不包含任何使用 Windows Media 9 系列或更新版本編解碼器的新系統設定檔。 這是因為必須有越來越多的設定檔，才能涵蓋編解碼器現在提供的各種功能。 您仍然可以使用第8版系統設定檔作為設定檔的起點。 如需詳細資訊，請參閱 [使用系統設定檔](using-system-profiles.md)。 如需將設定檔的目標設為特定傳遞裝置之新機制的相關資訊，請參閱 [使用裝置一致性範本](working-with-device-conformance-templates.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ASF 檔案功能**](asf-file-features.md)
</dt> <dt>

[**程式設計指南**](programming-guide.md)
</dt> </dl>

 

 




