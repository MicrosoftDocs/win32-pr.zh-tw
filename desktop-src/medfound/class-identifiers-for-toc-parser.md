---
description: 下列類別會在 wmcodecdsp 中宣告並與類別識別碼關聯 (Clsid) 。
ms.assetid: f82d92dc-fbce-4274-a10f-72fa8dd776cc
title: '目錄剖析器的類別識別碼 (Wmcodecdsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5108855c687085e77ce36aa14b3424732e25572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971155"
---
# <a name="class-identifiers-for-table-of-contents-parser"></a>目錄剖析器的類別識別碼

下列類別會在 wmcodecdsp 中宣告並與類別識別碼關聯 (Clsid) 。



| 類別名稱       | 易記的物件名稱 |
|------------------|----------------------|
| CTocEntry        | TOC 專案            |
| CTocEntryList    | 目錄專案清單       |
| CToc             | 目錄                  |
| CTocCollection   | 目錄集合       |
| CTocParser       | TOC 剖析器           |
| CTocGeneratorDmo | TOC 產生器        |



 

上表為每個類別提供易記的物件名稱。 本檔使用這些易記名稱來參考類別的實例。 例如，檔是指 CTocEntry 類別的實例做為 TOC 專案物件。

在程式碼中，您可以使用 **\_ \_ uuidof** 來參考 clsid。 例如，您可以使用下列程式碼來參考 CTocGeneratorDmo 的 CLSID。


```C++
__uuidof(CTocGeneratorDmo)
```



### <a name="clsid-constants-defined-in-wmcodecdsph"></a>Wmcodecdsp 中定義的 CLSID 常數

除了使用 **\_ \_ uuidof** 之外，您還可以使用常數來參考 clsid。 下列常數定義于 wmcodecdsp 中。



| 類別名稱     | CLSID 常數        |
|----------------|-----------------------|
| CTocEntry      | CLSID \_ CTocEntry      |
| CTocEntryList  | CLSID \_ CTocEntryList  |
| CToc           | CLSID \_ CToc           |
| CTocCollection | CLSID \_ CTocCollection |
| CTocParser     | CLSID \_ CTocParser     |



 

### <a name="clsid-constants-defined-in-wmcodecdspuuidlib"></a>Wmcodecdspuuid 中定義的 CLSID 常數

下列 CLSID 常數是在 wmcodecdsp 中宣告，但未定義。 若要在程式碼中使用它，您必須連結至 wmcodecdspuuid .lib。



| 類別名稱       | CLSID 常數          |
|------------------|-------------------------|
| CTocGeneratorDmo | CLSID \_ CTocGeneratorDmo |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wmvdspa.dll</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[目錄剖析器物件](toc-parser-objects.md)
</dt> </dl>

 

 




