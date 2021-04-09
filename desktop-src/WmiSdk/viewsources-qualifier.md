---
description: 所有視圖類別都必須有一個稱為 ViewSources 的字串陣列限定詞。
ms.assetid: aefa8cda-962f-4f6c-92a0-a8825d48db60
ms.tgt_platform: multiple
title: ViewSources 辨識符號
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ViewSources
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1f39146f8065401052c352472b28c4946cca6b98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693815"
---
# <a name="viewsources-qualifier"></a>ViewSources 辨識符號

所有視圖類別都必須有一個稱為 **ViewSources** 的字串陣列限定詞。 **ViewSources** 限定詞包含定義 view 類別中所使用之來源實例的來源查詢。 **ViewSources** 限定詞的值是字串陣列，其中包含 [*(WQL)*](gloss-w.md)查詢的 WMI 查詢語言。 您可以定義來源類別，並限制 view 類別所使用的來源實例與使用 [WQL](querying-with-wql.md)[WHERE 子句](where-clause.md) 進行查詢，以建立篩選的視圖。

[視圖提供者](view-provider.md)會依列出查詢和命名空間的順序，將 **ViewSources** 限定詞中的來源查詢與 [ViewSpaces 辨識符號](viewspaces-qualifier.md)中列出的命名空間相符。 來源查詢的數目必須符合 ViewSpaces 限定詞中列出的命名空間數目。 您列出來源查詢的順序會決定來源實例繪製所在的命名空間。

下列範例只會選取 **LocalDisk** 類別的實例，其中 **FileSystem** 屬性的值是 "NTFS" 和 **RemoteDisk** 類別的實例，其中的可 **空間** 屬性值大於 45 mb：


```sql
ViewSources{
"SELECT __Namespace, 
   Description, 
   DeviceID, 
   FileSystem, 
   FreeSpace, 
   VolumeName FROM LocalDisk 
 WHERE FileSystem = \"NTFS\"", 
   "SELECT __Namespace, 
   Description,
   DeviceID, 
   FileSystem, 
   FreeSpace, 
   VolumeName FROM RemoteDisk 
 WHERE FreeSpace > 45000000"}
```



> [!Note]  
> 您可以針對聯結視圖類別定義的來源查詢數目，取決於這些查詢所傳回的實例數目，以及這些實例可以聯結的方式有好幾種。 View 類別的來源實例可能組合的數目會以指數方式成長，因此請盡可能將聯結視圖類別的來源查詢保持在最簡單的情況。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**視圖提供者專用的限定詞**](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

 




