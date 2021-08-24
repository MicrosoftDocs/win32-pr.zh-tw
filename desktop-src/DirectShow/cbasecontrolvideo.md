---
description: CBaseControlVideo 類別會執行 IBasicVideo 介面，並控制一般影片視窗的影片屬性。 一般而言，CBaseControlVideo 物件是影片轉譯器，可將影片繪製到顯示器上的視窗中。
ms.assetid: 16fc1b0a-e5b5-4f33-ac2b-5acff61bab81
title: CBaseControlVideo 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3d8e6f7c881cc62f9124a58cb168bb3b2123d5f8e3c99b1d86b6aed0f87e2aaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697940"
---
# <a name="cbasecontrolvideo-class"></a>CBaseControlVideo 類別

![cbasecontrolvideo 類別階層](images/wctrl02.png)

**CBaseControlVideo** 類別會執行 [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo)介面，並控制一般影片視窗的影片屬性。 一般而言， **CBaseControlVideo** 物件是影片轉譯器，可將影片繪製到顯示器上的視窗中。

許多 **CBaseControlVideo** 成員函式只需要影片轉譯器連接至篩選圖形。 如果未連接，成員函式會傳回 **VFW \_ E \_ 未 \_ 連接**。 在影片轉譯器上設定的屬性會在連續連接和中斷連接之間保存。 所有應用程式都應該確保它們在開始簡報之前重設轉譯器屬性。

使用影片時，應用程式可以選取要使用的影片部分。 這個部分是 **CBaseControlVideo** 物件所控制的來源矩形。 **CBaseControlVideo** 可讓您的應用程式設定和取出來源矩形。 **CBaseControlVideo** 使用的所有矩形都採用寬度和高度值，而不是右值和底部值。 若未設定任何來源矩形，來源矩形的屬性會傳回完整的原生影片大小。



| 受保護的資料成員                                                                   | 描述                                                                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| m \_ pFilter                                                                               | 擁有媒體篩選器的指標。                                                              |
| m \_ pInterfaceLock                                                                        | 外部定義的重要區段。                                                            |
| m \_ pPin                                                                                  | 控制連接的媒體類型。                                                      |
| 成員函數                                                                         | 描述                                                                                     |
| [**CBaseControlVideo**](cbasecontrolvideo-cbasecontrolvideo.md)                         | 結構 **CBaseControlVideo** 物件。                                                      |
| [**CopyImage**](cbasecontrolvideo-copyimage.md)                                         | 建立影片影像的記憶體複本。                                                         |
| [**GetImageSize**](cbasecontrolvideo-getimagesize.md)                                   | 捕獲影片影像大小資訊。                                                         |
| [**SetControlVideoPin**](cbasecontrolvideo-setcontrolvideopin.md)                       | 設定此物件應該同步處理的 pin。                                         |
| 可覆寫的成員函式                                                             | 描述                                                                                     |
| [**CheckSourceRect**](cbasecontrolvideo-checksourcerect.md)                             | 判斷來源矩形是否有效。                                                      |
| [**CheckTargetRect**](cbasecontrolvideo-checktargetrect.md)                             | 判斷目標矩形是否有效。                                                      |
| [**GetSourceRect**](cbasecontrolvideo-getsourcerect.md)                                 | 抓取目前的來源影片矩形 (純虛擬) 。                                    |
| [**GetStaticImage**](cbasecontrolvideo-getstaticimage.md)                               | 傳回記憶體緩衝區中的目前映射 (純虛擬) 。                                    |
| [**GetTargetRect**](cbasecontrolvideo-gettargetrect.md)                                 | 抓取目前的目標影片矩形 (純虛擬) 。                                    |
| [**GetVideoFormat**](cbasecontrolvideo-getvideoformat.md)                               | 抓取包含影片格式的 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 結構。 |
| [**IsDefaultSourceRect**](cbasecontrolvideo-isdefaultsourcerect.md)                     | 判斷轉譯器是否使用預設的來源矩形 (純虛擬) 。                |
| [**IsDefaultTargetRect**](cbasecontrolvideo-isdefaulttargetrect.md)                     | 判斷轉譯器是否使用預設的目標矩形 (純虛擬) 。                |
| [**OnUpdateRectangles**](cbasecontrolvideo-onupdaterectangles.md)                       | 在來源或目標矩形變更時呼叫。                                             |
| [**OnVideoSizeChange**](cbasecontrolvideo-onvideosizechange.md)                         | 將 EC \_ 影片 \_ 大小 \_ 變更為應用程式。                                             |
| [**SetDefaultSourceRect**](cbasecontrolvideo-setdefaultsourcerect.md)                   | 將預設的來源影片矩形設定 (純虛擬) 。                                         |
| [**SetDefaultTargetRect**](cbasecontrolvideo-setdefaulttargetrect.md)                   | 將預設目標的影片矩形設定 (純虛擬) 。                                         |
| [**SetSourceRect**](cbasecontrolvideo-setsourcerect.md)                                 | 將目前的來源影片矩形設定 (純虛擬) 。                                         |
| [**SetTargetRect**](cbasecontrolvideo-settargetrect.md)                                 | 將目前的目標矩形設定 (純虛擬) 。                                               |
| IBasicVideo 方法                                                                      | 描述                                                                                     |
| [**取得 \_ AvgTimePerFrame**](cbasecontrolvideo-get-avgtimeperframe.md)                    | 抓取每個框架大約的平均時間。                                                |
| [**取得 \_ BitErrorRate**](cbasecontrolvideo-get-biterrorrate.md)                          | 抓取近似的位錯誤率。                                                        |
| [**取得 \_ 位元速率**](cbasecontrolvideo-get-bitrate.md)                                    | 抓取影片的近似位速度。                                                |
| [**GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md)                             | 抓取目前影像的記憶體呈現。                                              |
| [**取得 \_ DestinationHeight**](cbasecontrolvideo-get-destinationheight.md)                | 抓取目前的目的地矩形高度。                                           |
| [**取得 \_ DestinationLeft**](cbasecontrolvideo-get-destinationleft.md)                    | 抓取目前的目的地矩形左座標。                                  |
| [**GetDestinationPosition**](cbasecontrolvideo-getdestinationposition.md)               | 抓取目前的目的地位置。                                                     |
| [**取得 \_ DestinationTop**](cbasecontrolvideo-get-destinationtop.md)                      | 抓取目前的目的地矩形的上方座標。                                   |
| [**取得 \_ DestinationWidth**](cbasecontrolvideo-get-destinationwidth.md)                  | 抓取目前的目的地矩形寬度。                                            |
| [**取得 \_ SourceHeight**](cbasecontrolvideo-get-sourceheight.md)                          | 抓取目前來源矩形的高度。                                                |
| [**取得 \_ SourceLeft**](cbasecontrolvideo-get-sourceleft.md)                              | 抓取目前來源矩形的左座標。                                       |
| [**GetSourcePosition**](cbasecontrolvideo-getsourceposition.md)                         | 抓取目前的來源位置。                                                          |
| [**取得 \_ SourceTop**](cbasecontrolvideo-get-sourcetop.md)                                | 抓取目前來源矩形的上方座標。                                        |
| [**取得 \_ SourceWidth**](cbasecontrolvideo-get-sourcewidth.md)                            | 抓取目前來源矩形的寬度。                                                 |
| [**取得 \_ VideoHeight**](cbasecontrolvideo-get-videoheight.md)                            | 抓取原生影片高度。                                                              |
| [**GetVideoPaletteEntries**](cbasecontrolvideo-getvideopaletteentries.md)               | 抓取影片的元件專案範圍。                                             |
| [**GetVideoSize**](cbasecontrolvideo-getvideosize.md)                                   | 抓取原生影片的寬度和高度。                                             |
| [**取得 \_ VideoWidth**](cbasecontrolvideo-get-videowidth.md)                              | 抓取原生影片寬度。                                                               |
| [**IsUsingDefaultDestination**](cbasecontrolvideo-isusingdefaultdestination.md)         | 判斷轉譯器是否使用預設的目的地視窗。                             |
| [**IsUsingDefaultSource**](cbasecontrolvideo-isusingdefaultsource.md)                   | 判斷轉譯器是否使用預設來源視窗。                                  |
| [**put \_ DestinationHeight**](cbasecontrolvideo-put-destinationheight.md)                | 設定目的地矩形的高度。                                                        |
| [**put \_ DestinationLeft**](cbasecontrolvideo-put-destinationleft.md)                    | 設定目的地矩形的左座標。                                               |
| [**put \_ DestinationTop**](cbasecontrolvideo-put-destinationtop.md)                      | 設定目的地矩形的上方座標。                                                |
| [**put \_ DestinationWidth**](cbasecontrolvideo-put-destinationwidth.md)                  | 設定目的地矩形的寬度。                                                         |
| [**put \_ SourceHeight**](cbasecontrolvideo-put-sourceheight.md)                          | 設定來源矩形的高度。                                                             |
| [**put \_ SourceLeft**](cbasecontrolvideo-put-sourceleft.md)                              | 設定來源矩形的左座標。                                                    |
| [**put \_ SourceTop**](cbasecontrolvideo-put-sourcetop.md)                                | 設定來源矩形的上方座標。                                                     |
| [**put \_ SourceWidth**](cbasecontrolvideo-put-sourcewidth.md)                            | 設定來源矩形的寬度。                                                              |
| [**SetDefaultDestinationPosition**](cbasecontrolvideo-setdefaultdestinationposition.md) | 再次設定預設的目的地位置。                                                    |
| [**SetDefaultSourcePosition**](cbasecontrolvideo-setdefaultsourceposition.md)           | 再次設定預設來源位置。                                                         |
| [**SetDestinationPosition**](cbasecontrolvideo-setdestinationposition.md)               | 設定目的地矩形的位置。                                                        |
| [**SetSourcePosition**](cbasecontrolvideo-setsourceposition.md)                         | 設定來源矩形的位置。                                                             |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[DirectShow基類](directshow-base-classes.md)
</dt> </dl>

 

 



