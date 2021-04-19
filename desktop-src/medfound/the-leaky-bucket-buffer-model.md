---
description: '&\# 0034; 有漏洞 bucket&\# 0034; 模型是一種方式，可建立流暢播放的緩衝需求模型。'
ms.assetid: 2f7f80d6-3abb-462f-a571-b223a1d59da6
title: '有漏洞 Bucket 緩衝區模型 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5a99932fb121808f6a49323360c47c09d0acbb
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106981754"
---
# <a name="the-leaky-bucket-buffer-model-microsoft-media-foundation"></a>有漏洞 Bucket 緩衝區模型 (Microsoft 媒體基礎) 

當您透過網路串流媒體時，此解碼器會以理論上的固定速率接收編碼的資料， (傳輸速率) 。 此解碼器會使用此資料來產生解碼的輸出。 不過，在一般情況下，此解碼器 *會以變動的速率取用* 資料，因為編碼器可以使用可變的編碼速率。

「有漏洞 bucket」模型是一種模式，可讓您建立流暢播放的緩衝需求。 在此模型中，此解碼器會維護緩衝區。 編碼的資料會從網路進入緩衝區，而從緩衝區進入至解碼器。 如果緩衝區下溢，表示解碼器從緩衝區移除資料的速度，比網路傳遞資料的速度還要快。 如果緩衝區溢位，則表示網路的傳遞速度比使用解碼器所耗用的資料還要快。

本主題說明編碼和解碼之緩衝區的「有漏洞 bucket」模型。

-   [有漏洞 Bucket](#the-leaky-bucket)
-   [使用中的 Bucket](#the-bucket-in-use)
-   [設定 ASF 資料流程的有漏洞值區值](#setting-leaky-bucket-values-for-asf-streams)
-   [在 ASF 多工器中有漏洞 Bucket 值](#leaky-bucket-values-in-the-asf-multiplexer)
-   [更新 ASF 媒體接收器中的有漏洞 Bucket 值](#updating-leaky-bucket-values-in-the-asf-media-sink)
-   [相關主題](#related-topics)

## <a name="the-leaky-bucket"></a>有漏洞 Bucket

若要瞭解有漏洞 bucket 模型，請考慮在底部有小洞的值區。 有三個參數會定義值區：

-   容量 (B) 
-   水流出值區 (R 的速率) 
-   值區的初始飽和度 (F) 

在此比喻中，bucket 是緩衝區：

![圖例顯示緩衝區作為值區、輸入的輸入速率（輸入值區）和輸出速率（當水離開值區中的洞）](images/asf-components03.png)

如果將水 poured 到值區中，以精確的速率 *R* 進行，則值區會維持在 F，因為輸入速率等於輸出速率。 如果在 *R* 保持不變的情況下，輸入速率增加，則 bucket 會累積水。 如果輸入速率大於 *R* 長時間，則值區會溢位。 不過，輸入速率可能會因 *R* 而異，而不會溢出值區，只要平均輸入速率不超過值區的容量即可。 容量越大，輸入速率可能會在指定的時間範圍內有所差異。

在 ASF 中，有漏洞 bucket 是由三個參數所定義：

-   平均位元速率（位元組/秒），對應至輸出速率 (*R*) 
-   緩衝區視窗（以毫秒為單位），對應于 bucket 容量 (*B*) 。
-   初始緩衝區飽和度，通常設定為零。

位元速率會測量編碼資料流程中每秒的平均位數。 緩衝區視窗會測量資料的毫秒數，該位元速率可容納在緩衝區中。 位的緩衝區大小等於 R \* (B/1000) 。

ASF 承載資料可能會以不規則的時間輸入有漏洞值區，並以不規則的數量輸入值區，但必須將值區保留為固定的正位速率。 由於緩衝區視窗，承載進入值區和離開時的時間可能會有延遲。 可能發生的最大延遲為 *B* / *R*。 進入值區的承載資料是根據呈現時間，而且絕不能溢位。 除了呈現時間之外，每個承載也有傳送時間，也就是承載資料根據位元速率保留值區的時間。 傳送時間必須早于呈現時間，以確保當有漏洞 bucket 接近已滿時，每個承載會在其呈現時間之前或之後保留值區。 為了達成此目的，會將呈現時間前移 (預先) 的 *B* / *R* 值 ，而且傳送時間會從零開始著手。 傳送時間必須晚于呈現時間，因為這會指出承載的輸入值太晚，且不能包含在資料物件中。 預先的值會包含在 [ASF 標頭物件](asf-file-structure.md) 中。

對於透過網路的無問題串流，媒體內容中的壓縮資料流程必須在整個播放期間維持固定的位元速率。 ASF 有漏洞 bucket 模型可確保媒體資料會以固定的位元速率傳送到網路上。 有漏洞 bucket 的參數是在 [ASF 標頭物件](asf-file-structure.md)的擴充資料流程屬性物件中指定。 在 Microsoft 媒體基礎中，這些屬性會設定為代表資料流程之媒體類型上的屬性。

有漏洞值區值會定義在 ASF 檔案接收和基礎的 ASF 多工器物件中，以及 Windows Media 編碼器中。 這些值可能相同或不同。 例如，假設有一個串流案例，這需要比影片範例更晚傳遞音訊範例，以便在不延遲的情況下串流檔。 為了達到此目的，媒體接收器中的音訊串流有漏洞 bucket 可以設定為高於 Windows Media 音訊編碼器中所設定之值的值。

若要在編碼器中設定 B/R 值，應用程式必須設定 [**MFPKEY \_ RAVG**](mfpkey-ravgproperty.md)、 [**MFPKEY \_ BAVG**](mfpkey-bavgproperty.md)、 [**MFPKEY \_ RMAX**](mfpkey-rmaxproperty.md)和 [**MFPKEY \_ BMAX**](mfpkey-bmaxproperty.md) 屬性。 如需在編碼器中設定屬性的相關資訊，請參閱 [編碼屬性](configuring-the-encoder.md)。

## <a name="the-bucket-in-use"></a>使用中的 Bucket

編碼器的目標是要確保內容永遠不會溢出緩衝區。 編碼器會使用位元速率和緩衝區視窗值做為輔助線。 在任何時間點（等於緩衝區視窗）傳遞的實際位數，絕對不能大於緩衝區大小的兩倍。

請考慮下列範例：您有一個具有洞的3加侖值區，其中每分鐘可以有1個加侖可流動。 您將此值區放在 spigot 下，並開啟閥門，以每分鐘1加侖的費率來使用水。 當您輸入時，水會儘快流出值區，而值區中不會有額外的值。 然後，您會將流量從 spigot 增加為每分鐘2加侖。 每一分鐘，水會以這個速率流動，2加侖進入值區，1加侖流失，在值區中保留1加侖。 在3分鐘結束時，已有6加侖水進入值區，3加侖已流失，而 bucket 已滿。

在實務上，絕對不會達到理論上等於緩衝區視窗的最大資料速率。 前一個範例假設常數資料速率。 如果有相同的3加侖值區，您可以將 spigot 的流量率增加為每分鐘6加侖（一分鐘），然後將 spigot 關閉兩分鐘。 即使在 [緩衝區] 視窗的 [理論最大值] 中，放入值區的總量總數量，該量的集中程度也會造成值區溢位。 每分鐘6加侖，3加侖值區會在30秒後不久之後溢位。 因此，在任何間隔時間（等於緩衝區視窗設定）的情況下，可傳遞至緩衝區的實際最大資料量，取決於個別樣本的大小和傳遞時間。

到目前為止，這些範例只討論了解碼器所使用的緩衝區，但編碼程式也會使用有漏洞 bucket 緩衝區來建立壓縮的內容。 編碼器會進行壓縮演算法所需的任何調整，以將壓縮樣本的位元速率保留在位元速率和緩衝區視窗所描述的界限內，假設範例將會以固定速率傳遞給解碼器。 您可以將編碼器值區視為鏡像解碼器值區。 編碼器值區會以個別樣本大小所決定的變動率來填滿，並以相當於平均位元速率的固定速率來填滿。

請考慮下列透過網路連接在一起的編碼器和解碼器範例。 您可以使用每秒30個畫面格，以每秒6000位的位元速率和3秒的緩衝區視窗來編碼影片檔案， () 18000 的總緩衝區大小。 第一個範例會編碼為主要畫面格，並佔用7000位。 編碼器緩衝區現在包含7000位。 接下來的29個框架是總3000位的差異畫面格。 因此，第二個內容 (30 個畫面格) 如果沒有遺漏任何東西，就會將緩衝區飽和度放在10000位。我們知道資料流程的位元速率是每秒6000位，因此在編碼內容的第一秒放入編碼器緩衝區之後，飽和度會降至4000位。 在解碼應用程式中，此資料流程會以每秒6000位的形式傳遞至解碼器緩衝區。 在一秒後，緩衝區會包含6000位。 第一個範例包含7000位，因此在解碼器開始移除範例之前，必須先填入更多的解碼器緩衝區。

## <a name="setting-leaky-bucket-values-for-asf-streams"></a>設定 ASF 資料流程的有漏洞值區值

在檔案編碼案例中，應用程式可以在設定 [ASF 設定檔](asf-profile.md)中的資料流程時，設定有漏洞值區的值。

建立資料流程並參考資料流的 [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) 介面之後，您可以使用下列屬性來設定這些值：

-   [**MF \_ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) (平均有漏洞值區值) 
-   [**MF \_ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) (有漏洞 bucket 值的最大值) 

如需新增資料流程和取得 **IMFASFStreamConfig** 指標的詳細資訊，請參閱 [將資料流程資訊新增至 ASF 檔案接收](adding-stream-information-to-the-asf-file-sink.md)。

這些值包含下列資訊集：

-   平均位元速率：從媒體類型協商期間選取的輸出媒體類型取得平均位元速率。 使用適用于音訊串流) 的 [ [**mf \_ mt \_ 音訊 \_ 平均 \_ 位元組數 \_ \_**](mf-mt-audio-avg-bytes-per-second-attribute.md) ] 屬性 (，或針對影片串流) 使用 [ [**mf \_ mt \_ 平均 \_ 位元速率**](mf-mt-avg-bitrate-attribute.md) ] 屬性 (。
-   緩衝區視窗：如果您有編碼器的實例，並已協商輸出媒體類型，您可以稍後透過查詢 [**IWMCodecLeakyBucket**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket) 介面的編碼器，然後呼叫 [**IWMCodecLeakyBucket：： GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md) (wmcodecifaces .h，wmcodecdspuuid .lib) 來更新此值。 否則，請使用預設值3000毫秒。
-   初始緩衝區大小：設定為0。

應用程式所提供的值取決於編碼類型和資料流程的媒體類型。 例如， [常數位元速率編碼](constant-bit-rate-encoding.md) 需要預先決定的固定位元速率和緩衝區視窗。 應用程式可以藉由在資料流程上設定 [**MFPKEY \_ VIDEOWINDOW**](mfpkey-videowindowproperty.md) 編碼屬性和 [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) 屬性，來指定這些有漏洞值區的值。 指定的緩衝區視窗值是用來確定編碼的檔案具有標記在資料封包上的正確傳送時間，而且預先產生的值會出現在 ASF 標頭物件中。 設定 **mf \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1** 已足夠，因為這些指定的值會複製到 [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) 屬性中。

針對2通過編碼模式，您必須設定這兩個屬性，以指定平均值和最大值。

針對 VBR 編碼，應用程式只能在編碼階段完成之後，查詢編碼器所使用的有漏洞 bucket 值。 因此，在設定媒體接收器時，應用程式可以選擇不設定與有漏洞 bucket 相關的屬性或屬性。 編碼之後，應用程式必須查詢 [**MFPKEY \_ RAVG**](mfpkey-ravgproperty.md)、 [**MFPKEY \_ BAVG**](mfpkey-bavgproperty.md)、 [**MFPKEY \_ RMAX**](mfpkey-rmaxproperty.md)和 [**MFPKEY \_ BMAX**](mfpkey-bmaxproperty.md) 屬性的編碼器，並在媒體接收器中進行設定，讓正確的值反映在 Header 物件中。 如需有關如何更新 VBR 編碼值的程式碼範例，請參閱 [教學課程： 1-傳遞 Windows Media 編碼](tutorial--1-pass-windows-media-encoding.md)中的「更新檔案接收中的編碼屬性」。

如果您在沒有編碼的情況下，將 Windows Media 內容從來源複製到媒體接收，則必須在媒體接收器中設定有漏洞 bucket 值。

## <a name="leaky-bucket-values-in-the-asf-multiplexer"></a>在 ASF 多工器中有漏洞 Bucket 值

在媒體基礎中， [ASF](asf-multiplexer.md) 多工器會使用有漏洞 bucket 值來設定用來產生資料封包的內部有漏洞值區值。 承載包含在媒體範例中，而一系列的媒體範例構成了 ASF 資料封包。 根據有漏洞值區值和呈現時間，多工器會為每個媒體範例指派傳送時間，如此一來，透過網路傳送的封包的位元速率會以固定的位元速率 (*R*) 。

應用程式無法直接在多工器中設定有漏洞值區的值。 您必須在 ASF 媒體接收器上提供這些值，以在多工器上設定適當的值。 [**\_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md)和 [**mf \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)中設定的值會由多工器用來驗證傳送到 ASF 媒體接收器的範例是使用指定的值來產生的。

## <a name="updating-leaky-bucket-values-in-the-asf-media-sink"></a>更新 ASF 媒體接收器中的有漏洞 Bucket 值

應用程式可以藉由在媒體接收器的屬性存放區中設定 [**MFPKEY \_ ASFSTREAMSINK \_ 更正 \_ LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) 屬性，來覆寫資料流程層級有漏洞值區值 (在建立) 資料流程期間于 ASF 設定檔中設定的值。 若要取得屬性存放區的參考，請使用媒體接收器所執行的 ContentInfo 物件。 如需詳細資訊，請參閱 [設定 File 接收中的屬性](setting-properties-in-the-file-sink.md)。

**注意**  這項作業只允許用於音訊串流。

在您已設定編碼器的輸出類型之後，必須設定這個屬性。 編碼器會根據媒體類型中所設定的位速率來計算緩衝區大小，以確保產生的媒體範例永遠不會溢位緩衝區。 編碼器會在壓縮期間進行必要的調整，以將壓縮樣本的位元速率保留在位元速率和緩衝區視窗所描述的界限內。

類似于有漏洞 bucket 的資料流程設定屬性、設定平均位元速率和緩衝區大小，以及 Dword 陣列中的初始緩衝區飽和度。 如需詳細資訊，請參閱本主題中的「為 ASF 資料流程設定有漏洞值區值」一節。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎中的 ASF 支援](asf-support-in-media-foundation.md)
</dt> <dt>

[Windows Media 轉碼器](windows-media-codecs.md)
</dt> </dl>

 

 
