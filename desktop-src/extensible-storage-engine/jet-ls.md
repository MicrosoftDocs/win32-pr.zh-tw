---
description: 深入瞭解： JET_LS
title: JET_LS
TOCTitle: JET_LS
ms:assetid: 8e4e7902-84b1-404b-8654-bb430a0952aa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269336(v=EXCHG.10)
ms:contentKeyID: 32765625
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 546ace6b93328c3420a33c131250510d8421491b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470834"
---
# <a name="jet_ls"></a>JET_LS


_**適用于：** Windows |Windows伺服器_

## <a name="jet_ls"></a>JET_LS

**JET_LS** 資料類型包含本機儲存體 (LS) 的內容控制碼。這個控制碼可能會與資料指標或資料表相關聯，而且可能會參考動態配置的資源。

**Windows xp： JET_LS** 是 Windows xp 引進的。

```cpp
    typedef JET_API_PTR JET_LS;
```

### <a name="data-types"></a>資料類型

JET_LS

JET_LSNil 的值表示不正確內容控制碼。

### <a name="remarks"></a>備註

內容控制碼一開始會與 **JET_LS** 資料類型（使用 [JetSetLS](./jetsetls-function.md)）相關聯。 您可以使用 [JetGetLS](./jetgetls-function.md)，從 **JET_LS** 資料類型中取出內容控制碼。

您可以使用 [JetGetLS](./jetgetls-function.md)搭配 JET_bitLSReset，明確地將內容控制碼與 **JET_LS** 資料類型解除關聯。 或者，當資料庫引擎釋出基礎物件做為應用程式直接或間接動作的結果時，內容控制碼也可以從 **JET_LS** 資料類型隱含地解除關聯。 在隱含的情況下，會將執行時間回呼發給應用程式，讓它可以清除內容控制碼。 如需從 **JET_LS** 資料類型隱含解除關聯的詳細資訊，請參閱 [JetSetLS](./jetsetls-function.md)。

下列旗標會與 JET_LS 資料類型相關聯。


| <p>詞彙</p> | <p>描述</p> | 
|-------------|--------------------|
| <p>JET_bitLSReset</p> | <p>內容控制碼與物件解除關聯。</p> | 
| <p>JET_bitLSCursor</p> | <p>設定或取出與資料表資料指標相關聯的本機儲存體。</p> | 
| <p>JET_bitLSTable</p> | <p>設定或取得與資料表相關聯的本機儲存體。</p> | 
| <p>JET_LSNil</p> | <p>內容控制碼無效。</p> | 



### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista 或 Windows XP。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008 或 Windows server 2003。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 



### <a name="see-also"></a>另請參閱

[JetSetLS](./jetsetls-function.md)  
[JetGetLS](./jetgetls-function.md)
