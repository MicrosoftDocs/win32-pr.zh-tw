---
description: DVDDirectory 屬性會設定或抓取目前 DVD 磁片區的目前的目錄。
ms.assetid: 0dbfdf28-cda5-41b2-82ce-114d9b940d91
title: DVDDirectory 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2431d9255aa743698baeb9c4b8427ffa9bf5220a60182ac08c246e11f20bcec8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749098"
---
# <a name="dvddirectory-property"></a>DVDDirectory 屬性

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

`DVDDirectory`屬性會設定或抓取目前 DVD 磁片區的目前的目錄。

``` syntax
[ sDirPath = ] MSWebDVD.DVDDirectory
```

## <a name="return-value"></a>傳回值

傳回表示 DVD 根目錄路徑的字串值。

## <a name="remarks"></a>備註

此屬性是讀取/寫入，沒有預設值。 當系統上有一個以上的 DVD 光碟機時，請使用這個方法來設定根路徑。 當系統上只有一個磁片磁碟機，而且其磁碟機號高於 "C" 時，MSWebDVD 物件會自動尋找它。 若為標準 DVD-Video 光碟，根路徑應該包含 ts \_ video 目錄：


```VB
MSWebDVD.DVDDirectory = "e:\\video_ts"
```



某些 DVD 磁片區的影片可能會在名為「影片 ts」以外的目錄中 \_ 。 一般的概念是，有一個額外的「DVD 磁片區」 (的組合。IFO。 VOB、和。通常儲存在 VIDEO TS 目錄) 的 BUP 檔案 \_ 可以放在光碟片上的子目錄中。藉由將根變更為指向此目錄，MSWebDVD 會在此不同的 DVD 磁片區上運作。 您可以使用一組新的功能表、標題等等，與影片 TS 根目錄中的標題無關， \_ 這將無法再存取。 這類目錄稱為「隱藏目錄」。 下列範例示範如何將隱藏的目錄設定為根目錄，其中「隱藏」是光碟作者提供給目錄之任何名稱的預留位置。


```VB
MSWebDVD.DVDDirectory = "d:\\webdvd\\hidden"
```



 

 



