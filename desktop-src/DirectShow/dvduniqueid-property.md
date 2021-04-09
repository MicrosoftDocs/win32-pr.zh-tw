---
description: DVDUniqueID 屬性會抓取可唯一識別目前光碟的系統產生數位。
ms.assetid: 8ea6dd4d-6998-4212-8874-9c6cd93a1db3
title: DVDUniqueID 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23138f348ef1ec71f1506c8892532bd42f1c807d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846340"
---
# <a name="dvduniqueid-property"></a>DVDUniqueID 屬性

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

`DVDUniqueID`屬性會抓取可唯一識別目前光碟的系統產生數位。

``` syntax
[ iDiscID = ] MSWebDVD.DVDUniqueID
```

## <a name="return-value"></a>傳回值

傳回可唯一識別目前光碟的整數值。

## <a name="remarks"></a>備註

這個屬性是唯讀的，沒有預設值。 識別碼 (識別碼) 號碼不是絕對唯一的，但在所有實際用途中都是唯一的。 此識別碼會套用至所有已複寫的光碟複本。換句話說，特定電影的所有複本都有相同的識別碼。 此識別碼是根據檔案大小、日期和其他資訊，而不是 BCA 值。

 

 



