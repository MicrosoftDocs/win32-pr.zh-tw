---
description: 描述硬碟、磁碟分割和主開機記錄。
ms.assetid: daf45180-2cc3-433d-823e-395e85ce3410
title: 磁片裝置和磁碟分割
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 758454c9fc9e684e918646bf99869c7544b3b02c0201eb2ba507f8ffbdc303d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015369"
---
# <a name="disk-devices-and-partitions"></a>磁片裝置和磁碟分割

硬碟是由一組堆疊片片所組成，每個都有 electromagnetically 儲存在同心圓或 *追蹤* 中的資料。 每個磁碟片都有兩個標頭，每一端都有一個，在磁片旋轉時讀取或寫入資料。 *硬碟* 控制硬碟的位置、讀取和寫入。 請注意，所有光碟的標頭都是以一個單位來放置。

曲目的最小可定址單位是一個 *磁區*。 *圓柱* 會定義為出現在每個片上相同位置中的一組曲目。 例如，下圖顯示具有四個磁碟片的硬碟。 柱面 X 是由每個每一端的 (軌 X) 的曲目組成。

![硬碟，包括曲目、磁區和磁碟片](images/diskdevice.png)

硬碟可以包含一或多個稱為 *磁碟分割* 的邏輯區域。 當使用者將硬碟格式化為 *基本磁碟* 時，會建立磁碟分割。 Windows 也支援 *動態磁碟*，本主題不會討論這些動態磁碟。 如需基本磁碟和動態磁碟的詳細資訊，請參閱 [基本和動態磁碟](basic-and-dynamic-disks.md)。

在磁片上建立多個磁碟分割，可讓您使用不同的硬碟。 例如，具有一個磁碟分割之硬碟的系統會包含單一磁片區，而系統會將該磁片磁碟機指定為磁片磁碟機 C。具有具有兩個磁碟分割之硬碟的系統，通常會包含磁片磁碟機 C 和 D。在硬碟上擁有多個磁碟分割可讓您更輕鬆地管理系統，例如組織檔案或支援多個使用者。

基本磁碟上的第一個實體磁區包含一種資料結構，稱為主開機記錄 (MBR) 。 MBR 包含下列各項：

-   開機程式 (大小上限為442個位元組) 
-   磁片簽章 (唯一的4位元組數位) 
-   分割資料表最多 (四個專案) 
-    (永遠 0x55AA) 的 MBR 標記結尾

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於磁片區管理](about-volume-management.md)
</dt> <dt>

[基本和動態磁碟](basic-and-dynamic-disks.md)
</dt> </dl>

 

 



