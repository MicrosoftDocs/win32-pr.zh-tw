---
description: 下列清單提供 Windows GDI + 所支援之屬性專案的描述。
ms.assetid: fc95aa3f-8381-430d-8cbf-6d23816a738d
title: 屬性專案描述
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc2a627ec809bb4f7d7299c522fd0e9d3e1cc05
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/27/2021
ms.locfileid: "105636120"
---
# <a name="property-item-descriptions"></a>屬性專案描述

下列清單提供 Windows GDI + 所支援之屬性專案的描述。 描述很簡單且一般，因此適用于各種不同的影像檔案格式。 如需特定檔案格式如何使用屬性專案的詳細說明，請參閱該檔案格式的規格。 如需詳細描述中繼資料之多個檔案規格和其他檔的連結，請參閱 [影像檔案格式規格](-gdiplus-constant-image-file-format-specifications.md)。

 (EXIF) 格式的交換影像檔是日本的電子產業開發關聯 (JEIDA) standard，1998年6月修改為2.1 版。 EXIF 規格的部分是與 JEIDA 的許可權一起使用。

## <a name="propertytaggpsver"></a>PropertyTagGpsVer

全球定位系統的版本 (GPS) IFD，指定為2.0.0.0。 當 PropertyTagGpsIFD 標記存在時，此標記是必要的。 當版本為2.0.0.0 時，標記值為0x02000000。



| 屬性資訊 | 值 |
|-------|---------------------|
| 標籤   | 0x0000              |
| 類型  | PropertyTagTypeByte |
| Count | 4                   |



 

## <a name="propertytaggpslatituderef"></a>PropertyTagGpsLatitudeRef

以 Null 結束的字元字串，指定緯度為北方或南部。 `N` 指定北美洲緯度，並 `S` 指定南部緯度。



| 屬性資訊 | 值 |
|-------|--------------------------------------------|
| 標籤   | 0x0001                                     |
| 類型  | PropertyTagTypeASCII                       |
| Count | 2 (一個字元加上 Null 結束字元)  |



 

## <a name="propertytaggpslatitude"></a>PropertyTagGpsLatitude

緯度。 緯度表示為三個值，分別提供度數、分和秒。 當表示度、分和秒時，格式為 dd/1、mm/1、ss/1。 使用度和分鐘時，例如分數的分鐘數最多可達兩位數，格式為 dd/1、mmmm/100、0/1。



| 屬性資訊 | 值 |
|-------|-------------------------|
| 標籤   | 0x0002                  |
| 類型  | PropertyTagTypeRational |
| 計數 | 3                       |



 

## <a name="propertytaggpslongituderef"></a>PropertyTagGpsLongitudeRef

以 Null 結束的字元字串，指定經度是東或西經度。 `E` 指定東部經度，並 `W` 指定 west 經度。



| 屬性資訊 | 值 |
|-------|--------------------------------------------|
| 標籤   | 0x0003                                     |
| 類型  | PropertyTagTypeASCII                       |
| Count | 2 (一個字元加上 Null 結束字元)  |



 

## <a name="propertytaggpslongitude"></a>PropertyTagGpsLongitude

經度。 經度表示為三個值，分別提供度數、分和秒。 當表示度、分和秒時，格式為 ddd/1、mm/1、ss/1。 使用度和分鐘時，例如分數的分鐘數最多可達兩位數，格式為 ddd/1、mmmm/100、0/1。



| 屬性資訊 | 值 |
|-------|-------------------------|
| 標籤   | 0x0004                  |
| 類型  | PropertyTagTypeRational |
| 計數 | 3                       |



 

## <a name="propertytaggpsaltituderef"></a>PropertyTagGpsAltitudeRef

參考高度，以計量為單位。



| 屬性資訊 | 值 |
|-------|---------------------|
| 標籤   | 0x0005              |
| 類型  | PropertyTagTypeByte |
| Count | 1                   |



 

## <a name="propertytaggpsaltitude"></a>PropertyTagGpsAltitude

高度（以量為單位），以 PropertyTagGpsAltitudeRef 所指定的參考高度為基礎。



| 屬性資訊 | 值 |
|-------|-------------------------|
| 標籤   | 0x0006                  |
| 類型  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytaggpsgpstime"></a>PropertyTagGpsGpsTime

國際標準時間 (UTC) 的時間。 此值會以三個指定小時、分和秒的有理數表示。



| 屬性資訊 | 值 |
|-------|-------------------------|
| 標籤   | 0x0007                  |
| 類型  | PropertyTagTypeRational |
| 計數 | 3                       |



 

## <a name="propertytaggpsgpssatellites"></a>PropertyTagGpsGpsSatellites

以 Null 結束的字元字串，指定用於測量的 GPS 附屬元件。 此標記可用來指定識別碼、提高許可權的角度、azimuth、SNR，以及有關每個附屬的其他資訊。 未指定格式。 如果 GPS 接收者無法進行度量，則必須將標記的值設定為 **Null**。



| 屬性資訊 | 值 |
|-------|----------------------------------------------------|
| 標籤   | 0x0008                                             |
| 類型  | PropertyTagTypeASCII                               |
| Count | 字串的長度，包括 Null 結束字元 |



 

## <a name="propertytaggpsgpsstatus"></a>PropertyTagGpsGpsStatus

以 Null 結束的字元字串，這個字串會指定記錄影像時 GPS 接收器的狀態。 `A` 表示正在進行測量， `V` 表示測量是互通性。



| 屬性資訊 | 值 |
|-------|--------------------------------------------|
| 標籤   | 0x0009                                     |
| 類型  | PropertyTagTypeASCII                       |
| Count | 2 (一個字元加上 Null 結束字元)  |



 

## <a name="propertytaggpsgpsmeasuremode"></a>PropertyTagGpsGpsMeasureMode

以 Null 結束的字元字串，指定 GPS 測量模式。 `2` 指定2D 測量，並 `3` 指定立體度量。



| 屬性資訊 | 值 |
|-------|--------------------------------------------|
| 標籤   | 0x000A                                     |
| 類型  | PropertyTagTypeASCII                       |
| Count | 2 (一個字元加上 Null 結束字元)  |



 

## <a name="propertytaggpsgpsdop"></a>PropertyTagGpsGpsDop

GPS DOP (精確度) 的資料程度。 HDOP 值是在2D 測量期間寫入，而 PDOP 值則是在立體測量期間寫入。



| 屬性資訊 | 值 |
|-------|-------------------------|
| 標籤   | 0x000B                  |
| 類型  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytaggpsspeedref"></a>PropertyTagGpsSpeedRef

以 Null 結束的字元字串，指定用來表示移動 GPS 接收器速度的單位。 `K`、 `M` 和 `N` 分別代表每小時公里、每小時英里和節點。



| 屬性資訊 | 值 |
|-------|--------------------------------------------|
| 標籤   | 0x000C                                     |
| 類型  | PropertyTagTypeASCII                       |
| Count | 2 (一個字元加上 Null 結束字元)  |



 

## <a name="propertytaggpsspeed"></a>PropertyTagGpsSpeed

GPS 接收器移動的速度。



| 屬性資訊 | 值 |
|-------|-------------------------|
| 標籤   | 0x000D                  |
| 類型  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytaggpstrackref"></a>PropertyTagGpsTrackRef

以 Null 結束的字元字串，指定用來提供 GPS 接收器移動方向的參考。 `T` 指定 true 方向，並 `M` 指定磁性方向。



| 屬性資訊 | 值 |
|-------|--------------------------------------------|
| 標籤   | 0x000E                                     |
| 類型  | PropertyTagTypeASCII                       |
| Count | 2 (一個字元加上 Null 結束字元)  |



 

## <a name="propertytaggpstrack"></a>PropertyTagGpsTrack

GPS 接收器移動的方向。 值的範圍是從0.00 到359.99。



| 屬性資訊 | 值 |
|-------|-------------------------|
| 標籤   | 0x000F                  |
| 類型  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytaggpsimgdirref"></a>PropertyTagGpsImgDirRef

以 Null 結束的字元字串，指定在捕獲影像時的參考。 `T` 指定 true 方向，並 `M` 指定磁性方向。



| 屬性資訊 | 值 |
|-------|--------------------------------------------|
| 標籤   | 0x0010                                     |
| 類型  | PropertyTagTypeASCII                       |
| Count | 2 (一個字元加上 Null 結束字元)  |



 

## <a name="propertytaggpsimgdir"></a>PropertyTagGpsImgDir

影像在捕獲時的方向。 值的範圍是從0.00 到359.99。



| 屬性資訊 | 值 |
|-------|-------------------------|
| 標籤   | 0x0011                  |
| 類型  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytaggpsmapdatum"></a>PropertyTagGpsMapDatum

以 Null 結束的字元字串，指定 GPS 接收器所使用的 geodetic 調查資料。 如果問卷資料僅限日本，則此標記的值為 `TOKYO` 或 `WGS-84` 。



| 屬性資訊 | 值 |
|-------|----------------------------------------------------|
| 標籤   | 0x0012                                             |
| 類型  | PropertyTagTypeASCII                               |
| Count | 字串的長度，包括 Null 結束字元 |



 

## <a name="propertytaggpsdestlatref"></a>PropertyTagGpsDestLatRef

以 Null 結束的字元字串，這個字串會指定目的點的緯度是北或南緯度。 `N` 指定北美洲緯度，並 `S` 指定南部緯度。



| 屬性資訊 | 值 |
|-------|--------------------------------------------|
| 標籤   | 0x0013                                     |
| 類型  | PropertyTagTypeASCII                       |
| Count | 2 (一個字元加上 Null 結束字元)  |



 

## <a name="propertytaggpsdestlat"></a>PropertyTagGpsDestLat

目的地點的緯度。 緯度表示為三個值，分別提供度數、分和秒。 當表示度、分和秒時，格式為 dd/1、mm/1、ss/1。 使用度和分鐘時，例如分數的分鐘數最多可達兩位數，格式為 dd/1、mmmm/100、0/1。



| 屬性資訊 | 值 |
|-------|-------------------------|
| 標籤   | 0x0014                  |
| 類型  | PropertyTagTypeRational |
| 計數 | 3                       |



 

## <a name="propertytaggpsdestlongref"></a>PropertyTagGpsDestLongRef

以 Null 結束的字元字串，這個字串會指定目的點的經度是東或西經度。 `E` 指定東部經度，並 `W` 指定 west 經度。



| 屬性資訊 | 值 |
|-------|--------------------------------------------|
| 標籤   | 0x0015                                     |
| 類型  | PropertyTagTypeASCII                       |
| Count | 2 (一個字元加上 Null 結束字元)  |



 

## <a name="propertytaggpsdestlong"></a>PropertyTagGpsDestLong

目的地點的經度。 經度會表示為三個值，分別提供度數、分和秒。 當表示度、分和秒時，格式為 ddd/1、mm/1、ss/1。 使用度和分鐘時，例如分數的分鐘數最多可達兩位數，格式為 ddd/1、mmmm/100、0/1。



| 屬性資訊 | 值 |
|-------|-------------------------|
| 標籤   | 0x0016                  |
| 類型  | PropertyTagTypeRational |
| 計數 | 3                       |



 

## <a name="propertytaggpsdestbearref"></a>PropertyTagGpsDestBearRef

以 Null 結束的字元字串，指定用來為目的點提供關聯的參考。 `T` 指定 true 方向，並 `M` 指定磁性方向。



| 屬性資訊 | 值 |
|-------|--------------------------------------------|
| 標籤   | 0x0017                                     |
| 類型  | PropertyTagTypeASCII                       |
| Count | 2 (一個字元加上 Null 結束字元)  |



 

## <a name="propertytaggpsdestbear"></a>PropertyTagGpsDestBear

與目的地點有關。 值的範圍是從0.00 到359.99。



| 屬性資訊 | 值 |
|-------|-------------------------|
| 標籤   | 0x0018                  |
| 類型  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytaggpsdestdistref"></a>PropertyTagGpsDestDistRef

以 Null 結束的字元字串，指定用來表示與目的地點距離的單位。 K、M 和 N 分別代表公里、英里和節點。



| 屬性資訊 | 值 |
|-------|--------------------------------------------|
| 標籤   | 0x0019                                     |
| 類型  | PropertyTagTypeASCII                       |
| Count | 2 (一個字元加上 Null 結束字元)  |



 

## <a name="propertytaggpsdestdist"></a>PropertyTagGpsDestDist

與目的地點之間的距離。



| 屬性資訊 | 值 |
|-------|-------------------------|
| 標籤   | 0x001A                  |
| 類型  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagnewsubfiletype"></a>PropertyTagNewSubfileType

Subfile 中的資料類型。



| 屬性資訊 | 值 |
|-------|---------------------|
| 標籤   | 0x00FE              |
| 類型  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagsubfiletype"></a>PropertyTagSubfileType

Subfile 中的資料類型。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x00FF               |
| 類型  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagimagewidth"></a>PropertyTagImageWidth

每個資料列的圖元數。



| 屬性資訊 | 值 |
|-------|---------------------------------------------|
| 標籤   | 0x0100                                      |
| 類型  | PropertyTagTypeShort 或 PropertyTagTypeLong |
| Count | 1                                           |



 

## <a name="propertytagimageheight"></a>PropertyTagImageHeight

圖元資料列的數目。



| 屬性資訊 | 值 |
|-------|---------------------------------------------|
| 標籤   | 0x0101                                      |
| 類型  | PropertyTagTypeShort 或 PropertyTagTypeLong |
| Count | 1                                           |



 

## <a name="propertytagbitspersample"></a>PropertyTagBitsPerSample

每個色彩元件的位數。 另請參閱 [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel)。



| 屬性資訊 | 值 |
|-------|------------------------------------------|
| 標籤   | 0x0102                                   |
| 類型  | PropertyTagTypeShort                     |
| Count | 每個圖元)  (元件的樣本數 |



 

## <a name="propertytagcompression"></a>PropertyTagCompression

用於影像資料的壓縮配置。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x0103               |
| 類型  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagphotometricinterp"></a>PropertyTagPhotometricInterp

圖元資料的轉譯方式。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x0106               |
| 類型  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagthreshholding"></a>PropertyTagThreshHolding

用來從灰色圖元轉換成黑色和白色圖元的技巧。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x0107               |
| 類型  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagcellwidth"></a>PropertyTagCellWidth

遞色或半色調矩陣的寬度。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x0108               |
| 類型  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagcellheight"></a>PropertyTagCellHeight

遞色或半色調矩陣的高度。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x0109               |
| 類型  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagfillorder"></a>PropertyTagFillOrder

位元組中位的邏輯順序。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x010A               |
| 類型  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagdocumentname"></a>PropertyTagDocumentName

以 Null 結束的字元字串，指定掃描影像的檔案名稱。



| 屬性資訊 | 值 |
|-------|----------------------------------------------------|
| 標籤   | 0x010D                                             |
| 類型  | PropertyTagTypeASCII                               |
| Count | 字串的長度，包括 Null 結束字元 |



 

## <a name="propertytagimagedescription"></a>PropertyTagImageDescription

以 Null 結束的字元字串，指定影像的標題。



| 屬性資訊 | 值 |
|-------|----------------------------------------------------|
| 標籤   | 0x010E                                             |
| 類型  | PropertyTagTypeASCII                               |
| Count | 字串的長度，包括 Null 結束字元 |



 

## <a name="propertytagequipmake"></a>PropertyTagEquipMake

以 Null 結束的字元字串，指定用來錄製影像之設備的製造商。



| 屬性資訊 | 值 |
|-------|----------------------------------------------------|
| 標籤   | 0x010F                                             |
| 類型  | PropertyTagTypeASCII                               |
| Count | 字串的長度，包括 Null 結束字元 |



 

## <a name="propertytagequipmodel"></a>PropertyTagEquipModel

以 Null 結束的字元字串，指定用來錄製影像之設備的模型名稱或模型編號。



| 屬性資訊 | 值 |
|-------|----------------------------------------------------|
| 標籤   | 0x0110                                             |
| 類型  | PropertyTagTypeASCII                               |
| Count | 字串的長度，包括 Null 結束字元 |



 

## <a name="propertytagstripoffsets"></a>PropertyTagStripOffsets

針對每個區域，該區域的位元組位移。 另請參閱 [PropertyTagRowsPerStrip](#propertytagrowsperstrip) 和 [PropertyTagStripBytesCount](#propertytagstripbytescount)。



| 屬性資訊 | 值 |
|-------|---------------------------------------------|
| 標籤   | 0x0111                                      |
| 類型  | PropertyTagTypeShort 或 PropertyTagTypeLong |
| Count | 停車數                            |



 

## <a name="propertytagorientation"></a>PropertyTagOrientation

根據資料列和資料行來觀看影像方向。



標籤

0x0112

類型

PropertyTagTypeShort

Count

1

1-第0個數據列位於視覺影像的頂端，而第0個數據行則是視覺效果左側。 2-第0個數據列位於影像的視覺頂端，而第0個數據行則是視覺效果右邊。 3-第0個數據列位於影像的視覺底部，而第0個數據行則是視覺效果右邊。 4-第0個數據列位於影像的視覺底部，而第0個數據行則是視覺效果左側。 5-第0個數據列是影像的視覺位置，而第0個數據行則是視覺效果上方。 6-第0個數據列是影像的視覺效果右邊，而第0個數據行則是視覺效果上方。 7-第0個數據列是影像的視覺效果右側，而第0個數據行則是視覺效果底部。 8-第0個數據列是影像左邊的視覺效果，而第0個數據行則是視覺效果底部。



 

## <a name="propertytagsamplesperpixel"></a>PropertyTagSamplesPerPixel

每個圖元的色彩元件數目。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x0115               |
| 類型  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagrowsperstrip"></a>PropertyTagRowsPerStrip

每個資料列的資料列數目。 另請參閱 [PropertyTagStripBytesCount](#propertytagstripbytescount) 和 [PropertyTagStripOffsets](#propertytagstripoffsets)。



| 屬性資訊 | 值 |
|-------|---------------------------------------------|
| 標籤   | 0x0116                                      |
| 類型  | PropertyTagTypeShort 或 PropertyTagTypeLong |
| Count | 1                                           |



 

## <a name="propertytagstripbytescount"></a>PropertyTagStripBytesCount

對於每個區域，該區域中的總位元組數。



| 屬性資訊 | 值 |
|-------|---------------------------------------------|
| 標籤   | 0x0117                                      |
| 類型  | PropertyTagTypeShort 或 PropertyTagTypeLong |
| Count | 停車數                            |



 

## <a name="propertytagminsamplevalue"></a>PropertyTagMinSampleValue

針對每個色彩元件，指派給該元件的最小值。 另請參閱 [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel)。



| 屬性資訊 | 值 |
|-------|------------------------------------------|
| 標籤   | 0x0118                                   |
| 類型  | PropertyTagTypeShort                     |
| Count | 每個圖元)  (元件的樣本數 |



 

## <a name="propertytagmaxsamplevalue"></a>PropertyTagMaxSampleValue

針對每個色彩元件，指派給該元件的最大值。 另請參閱 [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel)。



| 屬性資訊 | 值 |
|-------|------------------------------------------|
| 標籤   | 0x0119                                   |
| 類型  | PropertyTagTypeShort                     |
| Count | 每個圖元)  (元件的樣本數 |



 

## <a name="propertytagxresolution"></a>PropertyTagXResolution

影像寬度的每單位圖元數 (x) 方向。 單位是由 [PropertyTagResolutionUnit](#propertytagresolutionunit)所指定。



| 屬性資訊 | 值 |
|-------|-------------------------|
| 標籤   | 0x011A                  |
| 類型  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagyresolution"></a>PropertyTagYResolution

影像高度 (y) 方向的每單位圖元數。 單位是由 [PropertyTagResolutionUnit](#propertytagresolutionunit)所指定。



| 屬性資訊 | 值 |
|-------|-------------------------|
| 標籤   | 0x011B                  |
| 類型  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagplanarconfig"></a>PropertyTagPlanarConfig

圖元元件是否以大量或平面格式記錄。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x011C               |
| 類型  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagpagename"></a>PropertyTagPageName

以 Null 結束的字元字串，指定掃描影像的頁面名稱。



| 屬性資訊 | 值 |
|-------|----------------------------------------------------|
| 標籤   | 0x011D                                             |
| 類型  | PropertyTagTypeASCII                               |
| Count | 字串的長度，包括 Null 結束字元 |



 

## <a name="propertytagxposition"></a>PropertyTagXPosition

從頁面左側到影像左邊的位移。 測量單位是由 [PropertyTagResolutionUnit](#propertytagresolutionunit)所指定。



| 屬性資訊 | 值 |
|-------|-------------------------|
| 標籤   | 0x011E                  |
| 類型  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagyposition"></a>PropertyTagYPosition

從頁面頂端到影像頂端的位移。 測量單位是由 [PropertyTagResolutionUnit](#propertytagresolutionunit)所指定。



| 屬性資訊 | 值 |
|-------|-------------------------|
| 標籤   | 0x011F                  |
| 類型  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagfreeoffset"></a>PropertyTagFreeOffset

針對連續未使用位元組的每個字串，該字串的位元組位移。



| 屬性資訊 | 值 |
|------|---------------------|
| 標籤  | 0x0120              |
| 類型 | PropertyTagTypeLong |



 

## <a name="propertytagfreebytecounts"></a>PropertyTagFreeByteCounts

針對連續未使用位元組的每個字串，該字串中的位元組數目。



| 屬性資訊 | 值 |
|-------|-----------------------------------------------|
| 標籤   | 0x0121                                        |
| 類型  | PropertyTagTypeLong                           |
| Count | 連續未使用位元組的字串數目。 |



 

## <a name="propertytaggrayresponseunit"></a>PropertyTagGrayResponseUnit

PropertyTagGrayResponseCurve 所指定之數位的精確度。 1指定十分之一、2指定百分之一、3指定千位等。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x0122               |
| 類型  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytaggrayresponsecurve"></a>PropertyTagGrayResponseCurve

針對灰階影像中的每個可能圖元值，這是該圖元值的光學密度。



| 屬性資訊 | 值 |
|-------|---------------------------------|
| 標籤   | 0x0123                          |
| 類型  | PropertyTagTypeShort            |
| Count | 可能圖元值的數目 |



 

## <a name="propertytagt4option"></a>PropertyTagT4Option

與 T4 編碼相關的一組旗標。



| 屬性資訊 | 值 |
|-------|---------------------|
| 標籤   | 0x0124              |
| 類型  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagt6option"></a>PropertyTagT6Option

與 T6 編碼相關的旗標集合。



| 屬性資訊 | 值 |
|-------|---------------------|
| 標籤   | 0x0125              |
| 類型  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagresolutionunit"></a>PropertyTagResolutionUnit

水準解析度和垂直解析度的測量單位。



標籤

0x0128

類型

PropertyTagTypeShort

Count

1

2-英寸 3-釐米



 

## <a name="propertytagpagenumber"></a>PropertyTagPageNumber

掃描影像的頁面頁碼。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x0129               |
| 類型  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagtransferfunction"></a>PropertyTagTransferFunction

為影像指定傳送函數的資料表。



| 屬性資訊 | 值 |
|-------|------------------------------------------------------|
| 標籤   | 0x012D                                               |
| 類型  | PropertyTagTypeShort                                 |
| Count | 資料表所需的16位單字總數 |



 

## <a name="propertytagsoftwareused"></a>PropertyTagSoftwareUsed

以 Null 結束的字元字串，指定用來產生映射之裝置的軟體或固件的名稱和版本。



| 屬性資訊 | 值 |
|-------|----------------------------------------------------|
| 標籤   | 0x0131                                             |
| 類型  | PropertyTagTypeASCII                               |
| Count | 字串的長度，包括 Null 結束字元 |



 

## <a name="propertytagdatetime"></a>PropertyTagDateTime

建立映射的日期和時間。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x0132               |
| 類型  | PropertyTagTypeASCII |
| Count | 20                   |



 

## <a name="propertytagartist"></a>PropertyTagArtist

以 Null 結束的字元字串，指定建立影像的人員名稱。



| 屬性資訊 | 值 |
|-------|----------------------------------------------------|
| 標籤   | 0x013B                                             |
| 類型  | PropertyTagTypeASCII                               |
| Count | 字串的長度，包括 Null 結束字元 |



 

## <a name="propertytaghostcomputer"></a>PropertyTagHostComputer

以 Null 結束的字元字串，指定用來建立映射的電腦和/或作業系統。



| 屬性資訊 | 值 |
|-------|----------------------------------------------------|
| 標籤   | 0x013C                                             |
| 類型  | PropertyTagTypeASCII                               |
| Count | 字串的長度，包括 Null 結束字元 |



 

## <a name="propertytagpredictor"></a>PropertyTagPredictor

套用編碼配置之前，套用至影像資料的預測配置類型。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x013D               |
| 類型  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagwhitepoint"></a>PropertyTagWhitePoint

影像的白色點 Chromaticity。



| 屬性資訊 | 值 |
|-------|-------------------------|
| 標籤   | 0x013E                  |
| 類型  | PropertyTagTypeRational |
| 計數 | 2                       |



 

## <a name="propertytagprimarychromaticities"></a>PropertyTagPrimaryChromaticities

針對影像中的三種主要色彩，這是該色彩的 chromaticity。



| 屬性資訊 | 值 |
|-------|-------------------------|
| 標籤   | 0x013F                  |
| 類型  | PropertyTagTypeRational |
| Count | 6                       |



 

## <a name="propertytagcolormap"></a>PropertyTagColorMap

調色板索引影像的色調色板 (查閱資料表) 。



| 屬性資訊 | 值 |
|-------|-------------------------------------------------|
| 標籤   | 0x0140                                          |
| 類型  | PropertyTagTypeShort                            |
| Count | 調色板所需的16位字組數目 |



 

## <a name="propertytaghalftonehints"></a>PropertyTagHalftoneHints

半色調函數所使用的資訊



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x0141               |
| 類型  | PropertyTagTypeShort |
| 計數 | 2                    |



 

## <a name="propertytagtilewidth"></a>PropertyTagTileWidth

每個圖格中的圖元資料行數目。



| 屬性資訊 | 值 |
|-------|---------------------------------------------|
| 標籤   | 0x0142                                      |
| 類型  | PropertyTagTypeShort 或 PropertyTagTypeLong |
| Count | 1                                           |



 

## <a name="propertytagtilelength"></a>PropertyTagTileLength

每個圖格中的圖元資料列數。



| 屬性資訊 | 值 |
|-------|---------------------------------------------|
| 標籤   | 0x0143                                      |
| 類型  | PropertyTagTypeShort 或 PropertyTagTypeLong |
| Count | 1                                           |



 

## <a name="propertytagtileoffset"></a>PropertyTagTileOffset

針對每個磚，即該磚的位元組位移。



| 屬性資訊 | 值 |
|-------|---------------------|
| 標籤   | 0x0144              |
| 類型  | PropertyTagTypeLong |
| Count | 磚數目     |



 

## <a name="propertytagtilebytecounts"></a>PropertyTagTileByteCounts

針對每個磚，即該磚中的位元組數目。



| 屬性資訊 | 值 |
|-------|---------------------------------------------|
| 標籤   | 0x0145                                      |
| 類型  | PropertyTagTypeShort 或 PropertyTagTypeLong |
| Count | 磚數目                             |



 

## <a name="propertytaginkset"></a>PropertyTagInkSet

用於分隔影像中的一組墨水。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x014C               |
| 類型  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytaginknames"></a>PropertyTagInkNames

串連、以 null 結束的字元字串順序，指定用於分隔影像中的油墨名稱。



| 屬性資訊 | 值 |
|-------|------------------------------------------------------------------------|
| 標籤   | 0x014D                                                                 |
| 類型  | PropertyTagTypeASCII                                                   |
| Count | 字串序列的總長度，包括 Null 結束字元 |



 

## <a name="propertytagnumberofinks"></a>PropertyTagNumberOfInks

油墨數目。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x014E               |
| 類型  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagdotrange"></a>PropertyTagDotRange

對應至0% 點和100% 點的色彩元件值。



| 屬性資訊 | 值 |
|-------|---------------------------------------------|
| 標籤   | 0x0150                                      |
| 類型  | PropertyTagTypeByte 或 PropertyTagTypeShort |
| Count | 2或2× PropertyTagSamplesPerPixel           |



 

## <a name="propertytagtargetprinter"></a>PropertyTagTargetPrinter

以 Null 結束的字元字串，描述預期的列印環境。



| 屬性資訊 | 值 |
|-------|----------------------------------------------------|
| 標籤   | 0x0151                                             |
| 類型  | PropertyTagTypeASCII                               |
| Count | 字串的長度，包括 Null 結束字元 |



 

## <a name="propertytagextrasamples"></a>PropertyTagExtraSamples

額外色彩元件的數目。 例如，一個額外的元件可能會保存 Alpha 值。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x0152               |
| 類型  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagsampleformat"></a>PropertyTagSampleFormat

針對每個色彩元件，數值格式 (該元件的未簽署、帶正負號、浮點數) 。 另請參閱 [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel)。



| 屬性資訊 | 值 |
|-------|------------------------------------------|
| 標籤   | 0x0153                                   |
| 類型  | PropertyTagTypeShort                     |
| Count | 每個圖元)  (元件的樣本數 |



 

## <a name="propertytagsminsamplevalue"></a>PropertyTagSMinSampleValue

針對每個色彩元件，該元件的最小值。 另請參閱 [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel)。



| 屬性資訊 | 值 |
|-------|-----------------------------------------------------|
| 標籤   | 0x0154                                              |
| 類型  | 最符合圖元元件資料的類型 |
| Count | 每個圖元)  (元件的樣本數            |



 

## <a name="propertytagsmaxsamplevalue"></a>PropertyTagSMaxSampleValue

針對每個色彩元件，該元件的最大值。 另請參閱 [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel)。



| 屬性資訊 | 值 |
|-------|-----------------------------------------------------|
| 標籤   | 0x0155                                              |
| 類型  | 最符合圖元元件資料的類型 |
| Count | 每個圖元)  (元件的樣本數            |



 

## <a name="propertytagtransferrange"></a>PropertyTagTransferRange

擴充傳送函數範圍之值的資料表。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x0156               |
| 類型  | PropertyTagTypeShort |
| Count | 6                    |



 

## <a name="propertytagjpegproc"></a>PropertyTagJPEGProc

JPEG 壓縮進程。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x0200               |
| 類型  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagjpeginterformat"></a>PropertyTagJPEGInterFormat

JPEG 位流開頭的位移。



| 屬性資訊 | 值 |
|-------|---------------------|
| 標籤   | 0x0201              |
| 類型  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagjpeginterlength"></a>PropertyTagJPEGInterLength

JPEG 位流的長度（以位元組為單位）。



| 屬性資訊 | 值 |
|-------|---------------------|
| 標籤   | 0x0202              |
| 類型  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagjpegrestartinterval"></a>PropertyTagJPEGRestartInterval

重新開機間隔的長度。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x0203               |
| 類型  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagjpeglosslesspredictors"></a>PropertyTagJPEGLosslessPredictors

針對每個色彩元件，該元件會有不失真的預測器選取值。 另請參閱 [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel)。



| 屬性資訊 | 值 |
|-------|------------------------------------------|
| 標籤   | 0x0205                                   |
| 類型  | PropertyTagTypeShort                     |
| Count | 每個圖元)  (元件的樣本數 |



 

## <a name="propertytagjpegpointtransforms"></a>PropertyTagJPEGPointTransforms

針對每個色彩元件，該元件的點變換值。 另請參閱 [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel)。



| 屬性資訊 | 值 |
|-------|------------------------------------------|
| 標籤   | 0x0206                                   |
| 類型  | PropertyTagTypeShort                     |
| Count | 每個圖元)  (元件的樣本數 |



 

## <a name="propertytagjpegqtables"></a>PropertyTagJPEGQTables

針對每個色彩元件，該元件的量化資料表位移。 另請參閱 [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel)。



| 屬性資訊 | 值 |
|-------|------------------------------------------|
| 標籤   | 0x0207                                   |
| 類型  | PropertyTagTypeLong                      |
| Count | 每個圖元)  (元件的樣本數 |



 

## <a name="propertytagjpegdctables"></a>PropertyTagJPEGDCTables

針對每個色彩元件，DC Huffman 資料表的位移 (或不失真的 Huffman 資料表) 該元件。 另請參閱 [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel)。



| 屬性資訊 | 值 |
|-------|------------------------------------------|
| 標籤   | 0x0208                                   |
| 類型  | PropertyTagTypeLong                      |
| Count | 每個圖元)  (元件的樣本數 |



 

## <a name="propertytagjpegactables"></a>PropertyTagJPEGACTables

針對每個色彩元件，這是該元件之 AC Huffman 資料表的位移。 另請參閱 [PropertyTagSamplesPerPixel](#propertytagsamplesperpixel)。



| 屬性資訊 | 值 |
|-------|------------------------------------------|
| 標籤   | 0x0209                                   |
| 類型  | PropertyTagTypeLong                      |
| Count | 每個圖元)  (元件的樣本數 |



 

## <a name="propertytagycbcrcoefficients"></a>PropertyTagYCbCrCoefficients

從 RGB 轉換成 YCbCr 影像資料的係數。



| 屬性資訊 | 值 |
|-------|-------------------------|
| 標籤   | 0x0211                  |
| 類型  | PropertyTagTypeRational |
| 計數 | 3                       |



 

## <a name="propertytagycbcrsubsampling"></a>PropertyTagYCbCrSubsampling

相對於亮度元件的色度元件取樣率。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x0212               |
| 類型  | PropertyTagTypeShort |
| 計數 | 2                    |



 

## <a name="propertytagycbcrpositioning"></a>PropertyTagYCbCrPositioning

色度元件相對於亮度元件的位置。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x0213               |
| 類型  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagrefblackwhite"></a>PropertyTagREFBlackWhite

參考黑色點值和參考點值。



| 屬性資訊 | 值 |
|-------|-------------------------|
| 標籤   | 0x0214                  |
| 類型  | PropertyTagTypeRational |
| Count | 6                       |



 

## <a name="propertytaggamma"></a>PropertyTagGamma

附加至影像的 Gamma 值。 Gamma 值會儲存為有理數 (成對的 **long**) ，且分子為100000。 例如，將 gamma 值2.2 儲存為配對 (100000，45455) 。



| 屬性資訊 | 值 |
|-------|-------------------------|
| 標籤   | 0x0301                  |
| 類型  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagiccprofiledescriptor"></a>PropertyTagICCProfileDescriptor

識別 ICC 設定檔的以 Null 結束的字元字串。



| 屬性資訊 | 值 |
|-------|----------------------------------------------------|
| 標籤   | 0x0302                                             |
| 類型  | PropertyTagTypeASCII                               |
| Count | 字串的長度，包括 Null 結束字元 |



 

## <a name="propertytagsrgbrenderingintent"></a>PropertyTagSRGBRenderingIntent

應如何依照國際色彩協會 (ICC) 的定義來顯示影像。 如果使用設定為 **TRUE** 的 *useEmbeddedColorManagement* 參數來建立 gdi +[**影像**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image)物件，則 gdi + 會根據指定的轉譯意圖呈現影像。 意圖可以設定為可感知、相對色度、飽和度或絕對色度。

-   適用于相片的可感知意圖可針對顯示裝置範圍提供良好的調整，但代價是會降低色度的精確度。
-   相對色度意圖適用于影像 (例如，標誌) ，其需要相對於顯示裝置的白色點進行色彩外觀比對。
-   飽和度意圖適用于圖表和圖形，可保留色調和亮度的飽和度。
-   絕對色度意圖適用于證明 (預覽版的影像會以不同的顯示裝置) ，需要保留絕對 colorimetry。



標籤

0x0303

類型

BYTE

Count

1

0-感知 1-相對色度 2-飽和度 3-絕對色度



 

## <a name="propertytagimagetitle"></a>PropertyTagImageTitle

以 Null 結束的字元字串，指定影像的標題。



| 屬性資訊 | 值 |
|-------|----------------------------------------------------|
| 標籤   | 0x0320                                             |
| 類型  | PropertyTagTypeASCII                               |
| Count | 字串的長度，包括 Null 結束字元 |



 

## <a name="propertytagresolutionxunit"></a>PropertyTagResolutionXUnit

要顯示水準解析度的單位。



標籤

0x5001

類型

PropertyTagTypeShort

Count

1

1-圖元/每英寸 2-圖元/每釐米



 

## <a name="propertytagresolutionyunit"></a>PropertyTagResolutionYUnit

顯示垂直解析度的單位。



標籤

0x5002

類型

PropertyTagTypeShort

Count

1

1-圖元/每英寸 2-圖元/每釐米



 

## <a name="propertytagresolutionxlengthunit"></a>PropertyTagResolutionXLengthUnit

要顯示影像寬度的單位。



標籤

0x5003

類型

PropertyTagTypeShort

Count

1

1-英寸 2-x 3-點 4-十二點活字 5-欄



 

## <a name="propertytagresolutionylengthunit"></a>PropertyTagResolutionYLengthUnit

要顯示影像高度的單位。



標籤

0x5004

類型

PropertyTagTypeShort

Count

1

1-英寸 2-x 3-點 4-十二點活字 5-欄



 

## <a name="propertytagprintflags"></a>PropertyTagPrintFlags

指定列印選項的單位元組布林值順序。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x5005               |
| 類型  | PropertyTagTypeASCII |
| Count | 旗標數目      |



 

## <a name="propertytagprintflagsversion"></a>PropertyTagPrintFlagsVersion

列印旗標版本。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x5006               |
| 類型  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagprintflagscrop"></a>PropertyTagPrintFlagsCrop

列印旗標中心裁剪標記。



| 屬性資訊 | 值 |
|-------|---------------------|
| 標籤   | 0x5007              |
| 類型  | PropertyTagTypeByte |
| Count | 1                   |



 

## <a name="propertytagprintflagsbleedwidth"></a>PropertyTagPrintFlagsBleedWidth

列印旗標出血寬度。



| 屬性資訊 | 值 |
|-------|---------------------|
| 標籤   | 0x5008              |
| 類型  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagprintflagsbleedwidthscale"></a>PropertyTagPrintFlagsBleedWidthScale

列印旗標出血寬度尺規。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x5009               |
| 類型  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytaghalftonelpi"></a>PropertyTagHalftoneLPI

筆墨的螢幕頻率（以每英寸的行數為單位）。



| 屬性資訊 | 值 |
|-------|-------------------------|
| 標籤   | 0x500A                  |
| 類型  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytaghalftonelpiunit"></a>PropertyTagHalftoneLPIUnit

螢幕頻率的單位。



標籤

0x500B

類型

PropertyTagTypeShort

Count

1

1-每英寸2行2行（每個釐米）



 

## <a name="propertytaghalftonedegree"></a>PropertyTagHalftoneDegree

螢幕的角度。



| 屬性資訊 | 值 |
|-------|-------------------------|
| 標籤   | 0x500C                  |
| 類型  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytaghalftoneshape"></a>PropertyTagHalftoneShape

半色調點的形狀。



標籤

0x500D

類型

PropertyTagTypeShort

Count

1

0-四捨五入 1-橢圓形 2-行 3-方形 4-交叉 6-菱形



 

## <a name="propertytaghalftonemisc"></a>PropertyTagHalftoneMisc

其他半色調資訊。



| 屬性資訊 | 值 |
|-------|---------------------|
| 標籤   | 0x500E              |
| 類型  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytaghalftonescreen"></a>PropertyTagHalftoneScreen

指定是否要使用印表機預設畫面的布林值。



標籤

0x500F

類型

PropertyTagTypeByte

Count

1

1-使用印表機的預設畫面 2-其他



 

## <a name="propertytagjpegquality"></a>PropertyTagJPEGQuality

Adobe Photoshop 格式所使用的私用標記。 不提供公開使用。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x5010               |
| 類型  | PropertyTagTypeShort |
| Count | 任意                  |



 

## <a name="propertytaggridsize"></a>PropertyTagGridSize

格線和輔助線的相關資訊區塊。



| 屬性資訊 | 值 |
|-------|--------------------------|
| 標籤   | 0x5011                   |
| 類型  | PropertyTagTypeUndefined |
| Count | 任意                      |



 

## <a name="propertytagthumbnailformat"></a>PropertyTagThumbnailFormat

縮圖影像的格式。



標籤

0x5012

類型

PropertyTagTypeLong

Count

1

0-原始 RGB 1-JPEG



 

## <a name="propertytagthumbnailwidth"></a>PropertyTagThumbnailWidth

縮圖影像的寬度（以圖元為單位）。



| 屬性資訊 | 值 |
|-------|---------------------|
| 標籤   | 0x5013              |
| 類型  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagthumbnailheight"></a>PropertyTagThumbnailHeight

縮圖影像的高度（以圖元為單位）。



| 屬性資訊 | 值 |
|-------|---------------------|
| 標籤   | 0x5014              |
| 類型  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagthumbnailcolordepth"></a>PropertyTagThumbnailColorDepth

縮圖影像的每一像素位元數 (BPP) 。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x5015               |
| 類型  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagthumbnailplanes"></a>PropertyTagThumbnailPlanes

縮圖影像的色彩平面數目。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x5016               |
| 類型  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagthumbnailrawbytes"></a>PropertyTagThumbnailRawBytes

圖元資料列之間的位元組位移。



| 屬性資訊 | 值 |
|-------|---------------------|
| 標籤   | 0x5017              |
| 類型  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagthumbnailsize"></a>PropertyTagThumbnailSize

縮圖影像的總大小（以位元組為單位）。



| 屬性資訊 | 值 |
|-------|---------------------|
| 標籤   | 0x5018              |
| 類型  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagthumbnailcompressedsize"></a>PropertyTagThumbnailCompressedSize

縮圖影像的壓縮大小（以位元組為單位）。



| 屬性資訊 | 值 |
|-------|---------------------|
| 標籤   | 0x5019              |
| 類型  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagcolortransferfunction"></a>PropertyTagColorTransferFunction

指定色彩傳送函式之值的資料表。



| 屬性資訊 | 值 |
|-------|--------------------------|
| 標籤   | 0x501A                   |
| 類型  | PropertyTagTypeUndefined |
| Count | 任意                      |



 

## <a name="propertytagthumbnaildata"></a>PropertyTagThumbnailData

JPEG 或 RGB 格式的原始縮圖位。 取決於 PropertyTagThumbnailFormat。



| 屬性資訊 | 值 |
|-------|---------------------|
| 標籤   | 0x501B              |
| 類型  | PropertyTagTypeByte |
| Count | 變數            |



 

## <a name="propertytagthumbnailimagewidth"></a>PropertyTagThumbnailImageWidth

縮圖影像中每個資料列的圖元數。



| 屬性資訊 | 值 |
|-------|---------------------------------------------|
| 標籤   | 0x5020                                      |
| 類型  | PropertyTagTypeShort 或 PropertyTagTypeLong |
| Count | 1                                           |



 

## <a name="propertytagthumbnailimageheight"></a>PropertyTagThumbnailImageHeight

縮圖影像中的圖元資料列數。



| 屬性資訊 | 值 |
|-------|---------------------------------------------|
| 標籤   | 0x5021                                      |
| 類型  | PropertyTagTypeShort 或 PropertyTagTypeLong |
| Count | 1                                           |



 

## <a name="propertytagthumbnailbitspersample"></a>PropertyTagThumbnailBitsPerSample

縮圖影像中每個色彩元件的位數。 另請參閱 [PropertyTagThumbnailSamplesPerPixel](#propertytagthumbnailsamplesperpixel)。



| 屬性資訊 | 值 |
|-------|-----------------------------------------------------------------|
| 標籤   | 0x5022                                                          |
| 類型  | PropertyTagTypeShort                                            |
| Count | 縮圖影像中每個圖元)  (元件的樣本數 |



 

## <a name="propertytagthumbnailcompression"></a>PropertyTagThumbnailCompression

用於縮圖影像資料的壓縮配置。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x5023               |
| 類型  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagthumbnailphotometricinterp"></a>PropertyTagThumbnailPhotometricInterp

縮圖圖元資料的轉譯方式。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x5024               |
| 類型  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagthumbnailimagedescription"></a>PropertyTagThumbnailImageDescription

以 Null 結束的字元字串，指定影像的標題。



| 屬性資訊 | 值 |
|-------|----------------------------------------------------|
| 標籤   | 0x5025                                             |
| 類型  | PropertyTagTypeASCII                               |
| Count | 字串的長度，包括 Null 結束字元 |



 

## <a name="propertytagthumbnailequipmake"></a>PropertyTagThumbnailEquipMake

以 Null 結束的字元字串，指定用來錄製縮圖影像的設備製造商。



| 屬性資訊 | 值 |
|-------|----------------------------------------------------|
| 標籤   | 0x5026                                             |
| 類型  | PropertyTagTypeASCII                               |
| Count | 字串的長度，包括 Null 結束字元 |



 

## <a name="propertytagthumbnailequipmodel"></a>PropertyTagThumbnailEquipModel

以 Null 結束的字元字串，指定用來記錄縮圖影像之設備的模型名稱或模型編號。



| 屬性資訊 | 值 |
|-------|----------------------------------------------------|
| 標籤   | 0x5027                                             |
| 類型  | PropertyTagTypeASCII                               |
| Count | 字串的長度，包括 Null 結束字元 |



 

## <a name="propertytagthumbnailstripoffsets"></a>PropertyTagThumbnailStripOffsets

縮圖影像中的每個區域，該區域的位元組位移。 另請參閱 [PropertyTagThumbnailRowsPerStrip](#propertytagthumbnailrowsperstrip) 和 [PropertyTagThumbnailStripBytesCount](#propertytagthumbnailstripbytescount)。



| 屬性資訊 | 值 |
|-------|---------------------------------------------|
| 標籤   | 0x5028                                      |
| 類型  | PropertyTagTypeShort 或 PropertyTagTypeLong |
| Count | 停車數                            |



 

## <a name="propertytagthumbnailorientation"></a>PropertyTagThumbnailOrientation

根據資料列和資料行的縮圖影像方向。 另請參閱 [PropertyTagOrientation](#propertytagorientation)。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x5029               |
| 類型  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagthumbnailsamplesperpixel"></a>PropertyTagThumbnailSamplesPerPixel

縮圖影像中每個圖元的色彩元件數目。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x502A               |
| 類型  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagthumbnailrowsperstrip"></a>PropertyTagThumbnailRowsPerStrip

縮圖影像中每個資料列的資料列數目。 另請參閱 [PropertyTagThumbnailStripBytesCount](#propertytagthumbnailstripbytescount) 和 [PropertyTagThumbnailStripOffsets](#propertytagthumbnailstripoffsets)。



| 屬性資訊 | 值 |
|-------|---------------------------------------------|
| 標籤   | 0x502B                                      |
| 類型  | PropertyTagTypeShort 或 PropertyTagTypeLong |
| Count | 1                                           |



 

## <a name="propertytagthumbnailstripbytescount"></a>PropertyTagThumbnailStripBytesCount

針對每個縮圖影像區域，該區域中的總位元組數。



| 屬性資訊 | 值 |
|-------|---------------------------------------------|
| 標籤   | 0x502C                                      |
| 類型  | PropertyTagTypeShort 或 PropertyTagTypeLong |
| Count | 縮圖影像中的條紋數     |



 

## <a name="propertytagthumbnailresolutionx"></a>PropertyTagThumbnailResolutionX

寬度方向的縮圖解析度。 解析單位會在 [PropertyTagThumbnailResolutionUnit](#propertytagthumbnailresolutionunit)中提供。



| 屬性資訊 | 值 |
|-----|--------|
| 標籤 | 0x502D |



 

## <a name="propertytagthumbnailresolutiony"></a>PropertyTagThumbnailResolutionY

高度方向的縮圖解析度。 解析單位會在 [PropertyTagThumbnailResolutionUnit](#propertytagthumbnailresolutionunit)中提供。



| 屬性資訊 | 值 |
|-----|--------|
| 標籤 | 0x502E |



 

## <a name="propertytagthumbnailplanarconfig"></a>PropertyTagThumbnailPlanarConfig

縮圖影像中的圖元元件是否以大量或平面格式記錄。 另請參閱 [PropertyTagPlanarConfig](#propertytagplanarconfig)。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x502F               |
| 類型  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagthumbnailresolutionunit"></a>PropertyTagThumbnailResolutionUnit

水準解析度的測量單位，以及縮圖影像的垂直解析度。 另請參閱 [PropertyTagResolutionUnit](#propertytagresolutionunit)。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x5030               |
| 類型  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagthumbnailtransferfunction"></a>PropertyTagThumbnailTransferFunction

為縮圖影像指定傳送函數的資料表。 另請參閱 [PropertyTagTransferFunction](#propertytagtransferfunction)。



| 屬性資訊 | 值 |
|-------|------------------------------------------------------|
| 標籤   | 0x5031                                               |
| 類型  | PropertyTagTypeShort                                 |
| Count | 資料表所需的16位單字總數 |



 

## <a name="propertytagthumbnailsoftwareused"></a>PropertyTagThumbnailSoftwareUsed

以 Null 結束的字元字串，指定用來產生縮圖影像之裝置的軟體或固件的名稱和版本。



| 屬性資訊 | 值 |
|-------|----------------------------------------------------|
| 標籤   | 0x5032                                             |
| 類型  | PropertyTagTypeASCII                               |
| Count | 字串的長度，包括 Null 結束字元 |



 

## <a name="propertytagthumbnaildatetime"></a>PropertyTagThumbnailDateTime

建立縮圖影像的日期和時間。 另請參閱 [PropertyTagDateTime](#propertytagdatetime)。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x5033               |
| 類型  | PropertyTagTypeASCII |
| Count | 20                   |



 

## <a name="propertytagthumbnailartist"></a>PropertyTagThumbnailArtist

以 Null 結束的字元字串，指定建立縮圖影像的人員名稱。



| 屬性資訊 | 值 |
|-------|----------------------------------------------------|
| 標籤   | 0x5034                                             |
| 類型  | PropertyTagTypeASCII                               |
| Count | 字串的長度，包括 Null 結束字元 |



 

## <a name="propertytagthumbnailwhitepoint"></a>PropertyTagThumbnailWhitePoint

縮圖影像的白色點 Chromaticity。 另請參閱 [PropertyTagWhitePoint](#propertytagwhitepoint)。



| 屬性資訊 | 值 |
|-------|-------------------------|
| 標籤   | 0x5035                  |
| 類型  | PropertyTagTypeRational |
| 計數 | 2                       |



 

## <a name="propertytagthumbnailprimarychromaticities"></a>PropertyTagThumbnailPrimaryChromaticities

針對縮圖影像中的三種主要色彩，這是該色彩的 chromaticity。 另請參閱 [PropertyTagPrimaryChromaticities](#propertytagprimarychromaticities)。



| 屬性資訊 | 值 |
|-------|-------------------------|
| 標籤   | 0x5036                  |
| 類型  | PropertyTagTypeRational |
| Count | 6                       |



 

## <a name="propertytagthumbnailycbcrcoefficients"></a>PropertyTagThumbnailYCbCrCoefficients

從 RGB 轉換成 YCbCr 縮圖影像之資料的係數。 另請參閱 [PropertyTagYCbCrCoefficients](#propertytagycbcrcoefficients)。



| 屬性資訊 | 值 |
|-------|-------------------------|
| 標籤   | 0x5037                  |
| 類型  | PropertyTagTypeRational |
| 計數 | 3                       |



 

## <a name="propertytagthumbnailycbcrsubsampling"></a>PropertyTagThumbnailYCbCrSubsampling

相對於縮圖影像的亮度元件，色度元件的取樣率。 另請參閱 [PropertyTagYCbCrSubsampling](#propertytagycbcrsubsampling)。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x5038               |
| 類型  | PropertyTagTypeShort |
| 計數 | 2                    |



 

## <a name="propertytagthumbnailycbcrpositioning"></a>PropertyTagThumbnailYCbCrPositioning

色度元件相對於縮圖影像的亮度元件的位置。 另請參閱 [PropertyTagYCbCrPositioning](#propertytagycbcrpositioning)。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x5039               |
| 類型  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagthumbnailrefblackwhite"></a>PropertyTagThumbnailRefBlackWhite

參考黑色點值以及縮圖影像的參考泛點值。 另請參閱 [PropertyTagREFBlackWhite](#propertytagrefblackwhite)。



| 屬性資訊 | 值 |
|-------|-------------------------|
| 標籤   | 0x503A                  |
| 類型  | PropertyTagTypeRational |
| Count | 6                       |



 

## <a name="propertytagthumbnailcopyright"></a>PropertyTagThumbnailCopyRight

以 Null 結束的字元字串，其中包含縮圖影像的著作權資訊。



| 屬性資訊 | 值 |
|-------|----------------------------------------------------|
| 標籤   | 0x503B                                             |
| 類型  | PropertyTagTypeASCII                               |
| Count | 字串的長度，包括 Null 結束字元 |



 

## <a name="propertytagluminancetable"></a>PropertyTagLuminanceTable

亮度表。 亮度表和色度資料表是用來控制 JPEG 品質。 有效的亮度或色度資料表具有64型別 PropertyTagTypeShort 的專案。 如果影像具有亮度資料表或色度資料表，則它必須有兩個數據表。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x5090               |
| 類型  | PropertyTagTypeShort |
| Count | 64                   |



 

## <a name="propertytagchrominancetable"></a>PropertyTagChrominanceTable

色度資料表。 亮度表和色度資料表是用來控制 JPEG 品質。 有效的亮度或色度資料表具有64型別 PropertyTagTypeShort 的專案。 如果影像具有亮度資料表或色度資料表，則它必須有兩個數據表。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x5091               |
| 類型  | PropertyTagTypeShort |
| Count | 64                   |



 

## <a name="propertytagframedelay"></a>PropertyTagFrameDelay

動畫 GIF 影像中兩個框架之間的時間延遲（百分之一秒）。



| 屬性資訊 | 值 |
|-------|-------------------------------|
| 標籤   | 0x5100                        |
| 類型  | PropertyTagTypeLong           |
| Count | 影像中的畫面格數目 |



 

## <a name="propertytagloopcount"></a>PropertyTagLoopCount

針對動畫 GIF 影像，顯示動畫的次數。 值為0會指定動畫應無限顯示。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x5101               |
| 類型  | PropertyTagTypeShort |
| Count | 1                    |



 

## <a name="propertytagglobalpalette"></a>PropertyTagGlobalPalette

GIF 影像中索引點陣圖的色調色板。



| 屬性資訊 | 值 |
|-------|-------------------------------|
| 標籤   | 0x5102                        |
| 類型  | PropertyTagTypeByte           |
| Count | 3 x 個調色板專案數目 |



 

## <a name="propertytagindexbackground"></a>PropertyTagIndexBackground

GIF 影像之調色板中的背景色彩索引。



| 屬性資訊 | 值 |
|-------|---------------------|
| 標籤   | 0x5103              |
| 類型  | PropertyTagTypeByte |
| Count | 1                   |



 

## <a name="propertytagindextransparent"></a>PropertyTagIndexTransparent

GIF 影像的調色板中透明色彩的索引。



| 屬性資訊 | 值 |
|-------|---------------------|
| 標籤   | 0x5104              |
| 類型  | PropertyTagTypeByte |
| Count | 1                   |



 

## <a name="propertytagpixelunit"></a>PropertyTagPixelUnit

PropertyTagPixelPerUnitX 和 PropertyTagPixelPerUnitY 的單位。



標籤

0x5110

類型

PropertyTagTypeByte

Count

1

0-未知



 

## <a name="propertytagpixelperunitx"></a>PropertyTagPixelPerUnitX

X 方向的每單位圖元。



| 屬性資訊 | 值 |
|-------|---------------------|
| 標籤   | 0x5111              |
| 類型  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagpixelperunity"></a>PropertyTagPixelPerUnitY

Y 方向的每單位圖元。



| 屬性資訊 | 值 |
|-------|---------------------|
| 標籤   | 0x5112              |
| 類型  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagpalettehistogram"></a>PropertyTagPaletteHistogram

調色板長條圖。



| 屬性資訊 | 值 |
|-------|-------------------------|
| 標籤   | 0x5113                  |
| 類型  | PropertyTagTypeByte     |
| Count | 長條圖的長度 |



 

## <a name="propertytagcopyright"></a>PropertyTagCopyright

以 Null 結束的字元字串，其中包含著作權資訊。



| 屬性資訊 | 值 |
|-------|----------------------------------------------------|
| 標籤   | 0x8298                                             |
| 類型  | PropertyTagTypeASCII                               |
| Count | 字串的長度，包括 Null 結束字元 |



 

## <a name="propertytagexifexposuretime"></a>PropertyTagExifExposureTime

曝光時間，以秒為單位。



| 屬性資訊 | 值 |
|-------|-------------------------|
| 標籤   | 0x829A                  |
| 類型  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagexiffnumber"></a>PropertyTagExifFNumber

F 編號。



| 屬性資訊 | 值 |
|-------|----------|
| 標籤   | 0x829D   |
| 類型  | 理性 |
| Count | 1        |



 

## <a name="propertytagexififd"></a>PropertyTagExifIFD

GDI + 所使用的私用標記。 不提供公開使用。 GDI + 會使用這個標記來尋找 Exif 特定的資訊。



| 屬性資訊 | 值 |
|-------|---------------------|
| 標籤   | 0x8769              |
| 類型  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagiccprofile"></a>PropertyTagICCProfile

內嵌于映射中的 ICC 設定檔。



| 屬性資訊 | 值 |
|-------|-----------------------|
| 標籤   | 0x8773                |
| 類型  | PropertyTagTypeByte   |
| Count | 設定檔的長度 |



 

## <a name="propertytagexifexposureprog"></a>PropertyTagExifExposureProg

相機使用的程式類別，在拍攝圖片時設定曝光。



標籤

0x8822

類型

SHORT

Count

1

預設

0

0-未定義 1-手動 2-一般程式 3-光圈先決級 4-快門優先 5-創意計畫 (偏高) 6-行動計畫 (偏高的快門速度) 7-縱向模式 (適用于具有背景焦點的橫向相片) 9 至 255-保留



 

## <a name="propertytagexifspectralsense"></a>PropertyTagExifSpectralSense

以 Null 結束的字元字串，指定所使用之相機的每個通道的光譜敏感度。 此字串與 ASTM 技術委員會所開發的標準相容。



| 屬性資訊 | 值 |
|-------|----------------------------------------------------|
| 標籤   | 0x8824                                             |
| 類型  | PropertyTagTypeASCII                               |
| Count | 字串的長度，包括 Null 結束字元 |



 

## <a name="propertytaggpsifd"></a>PropertyTagGpsIFD

GPS 屬性專案區塊的位移。 其標記具有前置詞 PropertyTagGps 的屬性專案會儲存在 GPS 區塊中。 GPS 屬性專案是在 EXIF 規格中定義。 GDI + 會使用這個標記來找出 GPS 資訊，但 GDI + 不會公開此標記以供公開使用。



| 屬性資訊 | 值 |
|-------|---------------------|
| 標籤   | 0x8825              |
| 類型  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagexifisospeed"></a>PropertyTagExifISOSpeed

以 iso 12232 指定的相機或輸入裝置的 ISO 速度和 ISO 緯度。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x8827               |
| 類型  | PropertyTagTypeShort |
| Count | 任意                  |



 

## <a name="propertytagexifoecf"></a>PropertyTagExifOECF

Optoelectronic 轉換函式 (ISO 14524 中指定的 OECF) 。 OECF 是攝影機光學輸入與影像值之間的關聯性。



| 屬性資訊 | 值 |
|-------|--------------------------|
| 標籤   | 0x8828                   |
| 類型  | PropertyTagTypeUndefined |
| Count | 任意                      |



 

## <a name="propertytagexifver"></a>PropertyTagExifVer

支援的 EXIF 標準版本。 此欄位的存在會用來表示標準的不符合項。 將0210記錄為4位元組 ASCII 字串表示標準的一致性。 因為類型是 PropertyTagTypeUndefined，所以沒有 Null 結束字元。



| 屬性資訊 | 值 |
|---------|--------------------------|
| 標籤     | 0x9000                   |
| 類型    | PropertyTagTypeUndefined |
| Count   | 4                        |
| 預設 | 0210                     |



 

## <a name="propertytagexifdtorig"></a>PropertyTagExifDTOrig

產生原始影像資料的日期和時間。 DSC 是拍攝圖片的日期和時間。 格式為 YYYY： MM： DD HH： MM： SS，以24小時制顯示時間，並以一個空白字元分隔日期和時間 (0x2000) 。 字元字串長度為20個位元組，包括 Null 結束字元。 當欄位為空白時，就會將其視為未知。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x9003               |
| 類型  | PropertyTagTypeASCII |
| Count | 20                   |



 

## <a name="propertytagexifdtdigitized"></a>PropertyTagExifDTDigitized

影像儲存為數字資料的日期和時間。 例如，如果影像是由 DSC 所捕捉，並且在記錄檔的同時，則 DateTimeOriginal 和 DateTimeDigitized 將會有相同的內容。

格式為 YYYY： MM： DD HH： MM： SS，以24小時制顯示時間，並以一個空白字元分隔日期和時間 (0x2000) 。 字元字串長度為20個位元組，包括 Null 結束字元。 當欄位為空白時，就會將其視為未知。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0x9004               |
| 類型  | PropertyTagTypeASCII |
| Count | 20                   |



 

## <a name="propertytagexifcompconfig"></a>PropertyTagExifCompConfig

壓縮資料的特定資訊。 每個元件的通道會依序從第一個元件排列至第四個元件。 針對未壓縮的資料，PropertyTagPhotometricInterp 標記中會提供資料排列。

不過，因為 PropertyTagPhotometricInterp 只能表達 Y、Cb 和 Cr 的順序，所以當壓縮的資料使用 Y、Cb 和 Cr 以外的元件，並支援其他順序時，就會提供此標記。



標籤

0x9101

類型

PropertyTagTypeUndefined

Count

4

預設

4 5 6 0 (如果 RGB 未壓縮) 1 2 3 0 (其他案例) 

0-不存在 1-Y 2-Cb 3-Cr 4-R 5-G 6-B （其他）保留



 

## <a name="propertytagexifcompbpp"></a>PropertyTagExifCompBPP

壓縮資料的特定資訊。 壓縮的影像所使用的壓縮模式會以單位 BPP 表示。



| 屬性資訊 | 值 |
|-------|-------------------------|
| 標籤   | 0x9102                  |
| 類型  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagexifshutterspeed"></a>PropertyTagExifShutterSpeed

快門速度。 此單位是影像曝光的加法系統 (頂點) 值。



| 屬性資訊 | 值 |
|-------|--------------------------|
| 標籤   | 0x9201                   |
| 類型  | PropertyTagTypeSRational |
| Count | 1                        |



 

## <a name="propertytagexifaperture"></a>PropertyTagExifAperture

鏡頭光圈。 此單位為頂點值。



| 屬性資訊 | 值 |
|-------|-------------------------|
| 標籤   | 0x9202                  |
| 類型  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagexifbrightness"></a>PropertyTagExifBrightness

亮度值。 此單位為頂點值。 通常會在-99.99 到99.99 的範圍中提供。



| 屬性資訊 | 值 |
|-------|--------------------------|
| 標籤   | 0x9203                   |
| 類型  | PropertyTagTypeSRational |
| Count | 1                        |



 

## <a name="propertytagexifexposurebias"></a>PropertyTagExifExposureBias

暴露偏差。 此單位為頂點值。 通常會提供範圍-99.99 到99.99。



| 屬性資訊 | 值 |
|-------|--------------------------|
| 標籤   | 0x9204                   |
| 類型  | PropertyTagTypeSRational |
| Count | 1                        |



 

## <a name="propertytagexifmaxaperture"></a>PropertyTagExifMaxAperture

最小的鏡頭 F 數目。 此單位為頂點值。 通常會提供00.00 到99.99 的範圍，但不限於此範圍。



| 屬性資訊 | 值 |
|-------|-------------------------|
| 標籤   | 0x9205                  |
| 類型  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagexifsubjectdist"></a>PropertyTagExifSubjectDist

與主旨之間的距離，以計量測量。



| 屬性資訊 | 值 |
|-------|-------------------------|
| 標籤   | 0x9206                  |
| 類型  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagexifmeteringmode"></a>PropertyTagExifMeteringMode

計量模式。



標籤

0x9207

類型

PropertyTagTypeShort

Count

1

預設

0

0-未知的 1-平均 2-CenterWeightedAverage 3-點 4-MultiSpot 5-模式 6-部分7到 254-保留 255-其他



 

## <a name="propertytagexiflightsource"></a>PropertyTagExifLightSource

燈光來源的類型。



標籤

0x9208

類型

PropertyTagTypeShort

Count

1

預設

0

0-未知的 1-日光 2-螢光 3-Tungsten 17-標準光 A 18-標準燈 B 19-標準燈 C 20-D55 21-D65 22-D75 23 到 254-保留 255-其他



 

## <a name="propertytagexifflash"></a>PropertyTagExifFlash

閃爍狀態。 使用明暗色亮 (flash) 來拍攝影像時，會記錄此標記。 Bit 0 表示 flash 引發狀態，而位1和2表示 flash 傳回狀態。



標籤

0x9209

類型

PropertyTagTypeShort

Count

1

位0的值，指出是否已引發閃爍： 0b-閃爍未引發 1b-flash

位1和2的值，表示傳回的燈狀態： 00b-沒有閃光燈傳回偵測函式01b 每個-保留的全選色-未偵測到未偵測到的的 11b-閃光燈傳回的光線

產生的閃光燈標記值： 0x0000-flash 未引發 0x0001-flash 引發的 0x0005-未偵測到明暗的傳回燈



 

## <a name="propertytagexiffocallength"></a>PropertyTagExifFocalLength

鏡頭的實際焦點長度（以毫米為單位）。 不是對35毫米膠捲攝影機的焦距進行轉換。



| 屬性資訊 | 值 |
|-------|-------------------------|
| 標籤   | 0x920A                  |
| 類型  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagexifmakernote"></a>PropertyTagExifMakerNote

附注標記。 EXIF 寫入器製造商用來記錄資訊的標記。 內容是由製造商所組成。



| 屬性資訊 | 值 |
|-------|--------------------------|
| 標籤   | 0x927C                   |
| 類型  | PropertyTagTypeUndefined |
| Count | 任意                      |



 

## <a name="propertytagexifusercomment"></a>PropertyTagExifUserComment

註解標記。 由 EXIF 使用者用來寫入影像的關鍵字或批註的標籤，除了在 PropertyTagImageDescription 中，以及沒有 PropertyTagImageDescription 標記的字元碼限制之外。



| 屬性資訊 | 值 |
|-------|--------------------------|
| 標籤   | 0x9286                   |
| 類型  | PropertyTagTypeUndefined |
| Count | 任意                      |



 

PropertyTagExifUserComment 標籤中使用的字元碼是根據標記資料區域開頭固定8位元組區域中的識別碼碼來識別。 區域未使用的部分會以 null 字元填補 (0) 。 識別碼代碼是透過註冊方式來指派。 因為類型不是 ASCII，所以不需要使用 Null 結束字元。

## <a name="propertytagexifdtsubsec"></a>PropertyTagExifDTSubsec

以 Null 結束的字元字串，指定 PropertyTagDateTime 標記的第二個部分。



| 屬性資訊 | 值 |
|-------|----------------------------------------------------|
| 標籤   | 0x9290                                             |
| 類型  | PropertyTagTypeASCII                               |
| Count | 字串的長度，包括 Null 結束字元 |



 

## <a name="propertytagexifdtorigss"></a>PropertyTagExifDTOrigSS

以 Null 結束的字元字串，指定 PropertyTagExifDTOrig 標記的第二個部分。



| 屬性資訊 | 值 |
|------|----------------------------------------------------|
| 標籤  | 0x9291                                             |
| 類型 | PropertyTagTypeASCII                               |
| N    | 字串的長度，包括 Null 結束字元 |



 

## <a name="propertytagexifdtdigss"></a>PropertyTagExifDTDigSS

以 Null 結束的字元字串，指定 PropertyTagExifDTDigitized 標記的第二個部分。



| 屬性資訊 | 值 |
|------|----------------------------------------------------|
| 標籤  | 0x9292                                             |
| 類型 | ASCII                                              |
| N    | 字串的長度，包括 Null 結束字元 |



 

## <a name="propertytagexiffpxver"></a>PropertyTagExifFPXVer

FPXR 檔案支援的 FlashPix 格式版本。 如果 FPXR 函式支援 FlashPix 格式版本1.0，則會以4位元組 ASCII 字串的形式錄製0100，以類似 PropertyTagExifVer 的方式來表示。 因為類型是 PropertyTagTypeUndefined，所以沒有 Null 結束字元。



標籤

0xA000

類型

PropertyTagTypeUndefined

Count

4

預設

0100

0100-FlashPix format version 1.0 Other-reserved



 

## <a name="propertytagexifcolorspace"></a>PropertyTagExifColorSpace

色彩空間規範。 通常是使用 sRGB (= 1) ，根據電腦監視器的狀況和環境定義色彩空間。 如果使用 sRGB 以外的色彩空間，則會設定 Uncalibrated (= 0xFFFF) 。 記錄為 Uncalibrated 的影像資料在轉換成 FlashPix 時，可以視為 sRGB。



標籤

0xA001

類型

PropertyTagTypeShort

Count

1

0x1-sRGB 0xFFFF-uncalibrated 其他-保留



 

## <a name="propertytagexifpixxdim"></a>PropertyTagExifPixXDim

壓縮資料的特定資訊。 當記錄了壓縮檔案時，無論是否有填補資料或重新開機標記，都必須在此標記中記錄有意義之影像的有效寬度。 此標記不應該存在於未壓縮檔案中。



| 屬性資訊 | 值 |
|-------|---------------------------------------------|
| 標籤   | 0xA002                                      |
| 類型  | PropertyTagTypeShort 或 PropertyTagTypeLong |
| Count | 1                                           |



 

## <a name="propertytagexifpixydim"></a>PropertyTagExifPixYDim

壓縮資料的特定資訊。 當記錄了壓縮檔案時，無論是否有填補資料或重新開機標記，都必須在此標記中記錄有意義之影像的有效高度。 此標記不應該存在於未壓縮檔案中。 因為垂直方向不需要資料填補，所以在此有效影像高度標記中錄製的行數將與 t 中記錄的行數相同。



| 屬性資訊 | 值 |
|-------|---------------------------------------------|
| 標籤   | 0xA003                                      |
| 類型  | PropertyTagTypeShort 或 PropertyTagTypeLong |
| Count | 1                                           |



 

## <a name="propertytagexifrelatedwav"></a>PropertyTagExifRelatedWav

與影像資料相關的音訊檔案名。 唯一記錄的關聯式資訊是 EXIF 音訊檔案名和副檔名， (包含8個字元加上句號 ( 的 ASCII 字串。 ) ，再加上3個字元) 。 不會記錄路徑。 當您使用此標記時，必須記錄音訊檔案，且必須符合 EXIF 音訊格式。 寫入器也可以將 APP2 中的音訊資料儲存為 FlashPix 擴充資料流程資料。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0xA004               |
| 類型  | PropertyTagTypeASCII |
| Count | 13                   |



 

## <a name="propertytagexifinterop"></a>PropertyTagExifInterop

包含互通性資訊的屬性專案區塊的位移。



| 屬性資訊 | 值 |
|-------|---------------------|
| 標籤   | 0xA005              |
| 類型  | PropertyTagTypeLong |
| Count | 1                   |



 

## <a name="propertytagexifflashenergy"></a>PropertyTagExifFlashEnergy

在捕獲映射時， (BCPS) 的閃光燈能源（以橫樑為單位）。



| 屬性資訊 | 值 |
|-------|-------------------------|
| 標籤   | 0xA20B                  |
| 類型  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagexifspatialfr"></a>PropertyTagExifSpatialFR

攝影機或輸入裝置空間頻率表，以及影像寬度、影像高度和對角線方向的 SFR. 值（如 ISO 12233 中所指定）。



| 屬性資訊 | 值 |
|-------|--------------------------|
| 標籤   | 0xA20C                   |
| 類型  | PropertyTagTypeUndefined |
| Count | 任意                      |



 

## <a name="propertytagexiffocalxres"></a>PropertyTagExifFocalXRes

影像寬度的圖元數， (相機焦點平面上每個單位的 x) 方向。 單位是在 PropertyTagExifFocalResUnit 中指定。



| 屬性資訊 | 值 |
|-------|-------------------------|
| 標籤   | 0xA20E                  |
| 類型  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagexiffocalyres"></a>PropertyTagExifFocalYRes

影像高度中的圖元數 (y) 相機焦點平面上每個單位的方向。 單位是在 PropertyTagExifFocalResUnit 中指定。



| 屬性資訊 | 值 |
|-------|-------------------------|
| 標籤   | 0xA20F                  |
| 類型  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagexiffocalresunit"></a>PropertyTagExifFocalResUnit

PropertyTagExifFocalXRes 和 PropertyTagExifFocalYRes 的測量單位。



標籤

0xA210

類型

PropertyTagTypeShort

Count

1

2-英寸 3-釐米



 

## <a name="propertytagexifsubjectloc"></a>PropertyTagExifSubjectLoc

場景中主體的位置。 此標記的值代表主要主體相對於左邊緣的圖元。 第一個值表示資料行編號，而第二個值表示資料列編號。



| 屬性資訊 | 值 |
|-------|----------------------|
| 標籤   | 0xA214               |
| 類型  | PropertyTagTypeShort |
| 計數 | 2                    |



 

## <a name="propertytagexifexposureindex"></a>PropertyTagExifExposureIndex

在拍攝映射時，于相機或輸入裝置上選取的公開索引。



| 屬性資訊 | 值 |
|-------|-------------------------|
| 標籤   | 0xA215                  |
| 類型  | PropertyTagTypeRational |
| Count | 1                       |



 

## <a name="propertytagexifsensingmethod"></a>PropertyTagExifSensingMethod

相機或輸入裝置上的影像感應器類型。



標籤

0xA217

類型

PropertyTagTypeShort

Count

1

1-未定義 2-一晶片色彩區域感應器 3-雙晶片色彩區域感應器 4-三晶片色彩區域感應器 5-彩色順序區域感應器 7-色彩順序區域感應器 7-三線性感應器 8-色彩順序線性感應器（其他-保留）



 

## <a name="propertytagexiffilesource"></a>PropertyTagExifFileSource

影像來源。 如果 DSC 錄製了映射，則此標記的值為3。



| 屬性資訊 | 值 |
|-------|--------------------------|
| 標籤   | 0xA300                   |
| 類型  | PropertyTagTypeUndefined |
| Count | 1                        |



 

## <a name="propertytagexifscenetype"></a>PropertyTagExifSceneType

場景的型別。 如果 DSC 錄製了映射，此標記的值必須設定為1，表示已直接拍攝映射。



| 屬性資訊 | 值 |
|-------|--------------------------|
| 標籤   | 0xA301                   |
| 類型  | PropertyTagTypeUndefined |
| Count | 1                        |



 

## <a name="propertytagexifcfapattern"></a>PropertyTagExifCfaPattern

色彩篩選器陣列 (使用單一晶片色彩區域感應器時，共同體影像感應器) 幾何模式。 它並不適用于所有的檢測方法。



| 屬性資訊 | 值 |
|-------|--------------------------|
| 標籤   | 0xA302                   |
| 類型  | PropertyTagTypeUndefined |
| Count | 任意                      |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[影像檔案格式規格](-gdiplus-constant-image-file-format-specifications.md)
</dt> <dt>

[影像屬性標記常數](-gdiplus-constant-image-property-tag-constants.md)
</dt> <dt>

[**影像屬性標記類型常數**](-gdiplus-constant-image-property-tag-type-constants.md)
</dt> <dt>

[依字母順序排列的屬性標記](-gdiplus-constant-property-tags-in-alphabetical-order.md)
</dt> <dt>

[以數位順序排序的屬性標記](-gdiplus-constant-property-tags-in-numerical-order.md)
</dt> <dt>

[讀取和寫入中繼資料](-gdiplus-reading-and-writing-metadata-use.md)
</dt> </dl>

 

 



