---
description: 在填充碼資料庫中包含專案和其標記資訊的索引。
ms.assetid: 2ff58e01-cc47-4612-a3bc-a87ccb343bd2
title: TAGID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e7d8b8a25633d3505936d105b0eef7ed38746ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936161"
---
# <a name="tagid"></a>TAGID

在填充碼資料庫中包含專案和其標記資訊的索引。


```C++
typedef DWORD TAGID;
```



## <a name="remarks"></a>備註

**TAGID** 是資料庫特有的。 它可以是代表索引的整數值，也可以是下列其中一個值：

<dl> <dt>

<span id="TAGID_NULL__0_"></span><span id="tagid_null__0_"></span>TAGID \_ Null (0) 
</dt> <dd>

**TAGID** 不存在。 當函數無法傳回有效的 **TAGID** 時，就會從該函式傳回這個值。

</dd> <dt>

<span id="TAGID_ROOT__0_"></span><span id="tagid_root__0_"></span>TAGID \_ ROOT (0) 
</dt> <dd>

表示根清單標記，可用來做為取得子 **TAGID** 的父系。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**標記**](tag.md)
</dt> <dt>

[標記類型](tag-types.md)
</dt> <dt>

[**TAGREF**](tagref.md)
</dt> </dl>

 

 




