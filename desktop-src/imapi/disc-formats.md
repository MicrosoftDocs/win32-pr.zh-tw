---
title: 光碟格式
description: IMAPI.EXE 支援三種檔案系統格式： ISO 9660、Joliet 和 UDF。
ms.assetid: 9cd782c0-203b-452c-9d04-3464d39453b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af9b4d4c5c5b6aa3e0c4c96598486a531c297b61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300923"
---
# <a name="disc-formats"></a>光碟格式

IMAPI.EXE 支援三種檔案系統格式： [ISO 9660](#iso-9660)、 [Joliet](#joliet)和 [UDF](#universal-disk-format-udf)。

## <a name="iso-9660"></a>ISO 9660

ISO 9660 格式是 CD 資料光碟的原始標準檔案系統。 此格式可在數個作業系統上辨識，包括 MSDOS.SYS、Mac OS、UNIX 和 Windows 作業系統。 ISO 9660 格式是由國際標準組織 (ISO) 所發行。

格式從第16磁區開始，磁片區標頭為 CD0001;標頭的其餘部分如下。 其他衍生格式也會從第16磁區開始，但會使用另一個字串作為磁片區標頭。 例如，高塞拉里昂光碟使用字串 CD ROM0001 和光碟互動格式使用 CD I0001。

標頭會指向以 ISO 9660 格式儲存檔案名的光碟區域。 檔案和目錄命名慣例是由8個字元、一個句點和3個字元所組成。 這是由 MSDOS.SYS 作業系統所使用的相同命名慣例。

針對 Joliet 和 UDF 等格式的其他檔案系統標頭可以並存存在於光碟，而不會影響 ISO 9660 格式的可讀性。 在索引之後，一組資料檔案會佔用光碟。每個檔案系統的索引會獨立參考光碟上的資料檔案。

ISO 9660 規格定義了下列三種層級的格式：

-   層級1定義使用8.3 字元格式的檔案名。
-   層級2允許較長的檔案名，如 DOS 6. xx、MacIntosh 和 UNIX 平臺上所找到的名稱。
-   層級3允許交錯的資料和音訊檔案，以改善) 效能的抓取 (播放。 此層級也會移除2GB 的檔案限制。 映射主控 API **不** 支援此層級。

DVD 光碟也可以使用 ISO 9660;不過，UDF 檔案系統是與 DVD 媒體搭配使用的最常見檔案系統。

## <a name="joliet"></a>Joliet

Joliet 格式是 ISO 9660 的衍生。 此格式除了 ISO 9660 檔案系統索引之外，還會將 Joliet 檔案系統索引寫入光碟映射。

Joliet 索引會針對檔案系統索引提供下列改善：

-   辨識長度最多為32個字元的長檔名。
-   區分檔案名中的大寫和小寫字母。
-   支援檔案名中的 Unicode 字元。

Joliet 格式標頭開始于光碟的第17磁區。

由於 Joliet 格式會保留光碟上的 ISO 9660 檔案系統，因此會保留與符合 ISO 9660 規範之裝置的相容性。

## <a name="universal-disk-format-udf"></a>國際磁碟格式 (UDF)

 (UDF) 的國際磁碟格式是以光學儲存體技術關聯 (OSTA) 為光學媒體所開發的較新檔案系統。 UDF 是數個作業系統所能辨識的可移植格式。 UDF 會將 ISO 9660 取代為新的標準，尤其是在讀取/寫入媒體中。

UDF 的功能包括下列各項：

-   最多可支援2TB 大小的媒體。
-   支援 flash 媒體、Iomega REV 光碟以及 CD MRW 光碟。
-   將小於 2 KB 的檔案儲存在檔案專案區塊中。
-   最多可支援 2 TB 的檔案，且長度為255個字元。
-   支援一組符合各種作業系統的豐富檔案屬性。
-   支援橋接器格式，其中的 ISO 9660、Joliet 和 UDF 格式都位於相同的光碟片上。這是在影片應用程式中使用，例如 DVD 影片、DVD + VR 和 DVD VR。
-   支援命名資料流程和「即時」檔案。

 

 




