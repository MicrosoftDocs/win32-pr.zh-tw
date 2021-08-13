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
ms.openlocfilehash: 38ddb306ee6fdcbd1eb792b2c29ca367adc0f4b88cc25dfcbdde22c2638258d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118765035"
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

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>詞彙</p></th>
<th><p>描述</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitLSReset</p></td>
<td><p>內容控制碼與物件解除關聯。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitLSCursor</p></td>
<td><p>設定或取出與資料表資料指標相關聯的本機儲存體。</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitLSTable</p></td>
<td><p>設定或取得與資料表相關聯的本機儲存體。</p></td>
</tr>
<tr class="even">
<td><p>JET_LSNil</p></td>
<td><p>內容控制碼無效。</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>規格需求

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>用戶端</strong></p></td>
<td><p>需要 Windows Vista 或 Windows XP。</p></td>
</tr>
<tr class="even">
<td><p><strong>伺服器</strong></p></td>
<td><p>需要 Windows server 2008 或 Windows server 2003。</p></td>
</tr>
<tr class="odd">
<td><p><strong>標頭</strong></p></td>
<td><p>宣告于 Esent. h 中。</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>另請參閱

[JetSetLS](./jetsetls-function.md)  
[JetGetLS](./jetgetls-function.md)
