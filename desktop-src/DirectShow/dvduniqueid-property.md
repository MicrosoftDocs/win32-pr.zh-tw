---
description: DVDUniqueID 屬性會抓取可唯一識別目前光碟的系統產生數位。
ms.assetid: 8ea6dd4d-6998-4212-8874-9c6cd93a1db3
title: DVDUniqueID 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 488a3e76c93005a55f58e631f0b166b51f036e63857df3b2e21eed6e093e55b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652901"
---
# <a name="dvduniqueid-property"></a>DVDUniqueID 屬性

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

`DVDUniqueID`屬性會抓取可唯一識別目前光碟的系統產生數位。

``` syntax
[ iDiscID = ] MSWebDVD.DVDUniqueID
```

## <a name="return-value"></a>傳回值

傳回可唯一識別目前光碟的整數值。

## <a name="remarks"></a>備註

這個屬性是唯讀的，沒有預設值。 識別碼 (識別碼) 號碼不是絕對唯一的，但在所有實際用途中都是唯一的。 此識別碼會套用至所有已複寫的光碟複本。換句話說，特定電影的所有複本都有相同的識別碼。 此識別碼是根據檔案大小、日期和其他資訊，而不是 BCA 值。

 

 



