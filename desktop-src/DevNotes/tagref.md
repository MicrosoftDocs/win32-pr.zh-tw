---
description: TAGREF-在填充碼資料庫中包含專案和其標記資訊的索引。
ms.assetid: e7d83dca-13a5-4396-b50b-0d068209c03c
title: TAGREF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bf5a9de8da025e8278ab0bca7ccbe16d70d16b782591181f6ce6ce74a010a39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075773"
---
# <a name="tagref"></a>TAGREF

在填充碼資料庫中包含專案和其標記資訊的索引。


```C++
typedef DWORD TAGREF;
```



## <a name="remarks"></a>備註

**TAGREF** 適用于填充碼資料庫，且在多個資料庫中都是有效的。 它可以是代表索引的整數值，也可以是下列其中一個值：

<dl> <dt>

<span id="TAGREF_NULL__0_"></span><span id="tagref_null__0_"></span>TAGREF \_ Null (0) 
</dt> <dd>

**TAGREF** 不存在。 當函數無法傳回有效的 **TAGREF** 時，就會從該函式傳回這個值。

</dd> <dt>

<span id="TAGREF_ROOT__0_"></span><span id="tagref_root__0_"></span>TAGREF \_ ROOT (0) 
</dt> <dd>

表示根清單標記，可用來做為取得子 **TAGREF** 的父系。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SdbTagRefToTagID**](sdbtagreftotagid.md)
</dt> <dt>

[**標記**](tag.md)
</dt> <dt>

[標記類型](tag-types.md)
</dt> <dt>

[**TAGID**](tagid.md)
</dt> </dl>

 

 




