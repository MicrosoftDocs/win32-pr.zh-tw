---
description: 深入瞭解：不正確控制碼常數
title: 不正確控制碼常數
TOCTitle: Invalid Handle Constants
ms:assetid: 594d7804-725f-4f72-b5f0-56f099c1c17b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269256(v=EXCHG.10)
ms:contentKeyID: 32765558
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
ms.openlocfilehash: f5614b36acfca8b5be4c13849d459d25f984336a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027376"
---
# <a name="invalid-handle-constants"></a>不正確控制碼常數


_**適用于：** Windows |Windows Server_

## <a name="invalid-handle-constants"></a>不正確控制碼常數

下列常數表示 ESE 不同方面的無效控制碼。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>常數/值</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_instanceNil<br />
 (~ (JET_INSTANCE) 0) </p></td>
<td><p>資料庫實例的控制碼無效。<br />
<strong>WINDOWS XP：</strong> 在 Windows XP 中引進。</p></td>
</tr>
<tr class="even">
<td><p>JET_sesidNil<br />
 (~ (JET_SESID) 0) </p></td>
<td><p>會話識別碼的控制碼無效。</p></td>
</tr>
<tr class="odd">
<td><p>JET_tableidNil<br />
 (~ (JET_TABLEID) 0) </p></td>
<td><p>資料表識別碼的無效控制碼。</p></td>
</tr>
<tr class="even">
<td><p>JET_bitNil<br />
 ( (JET_GRBIT) 0) </p></td>
<td><p>位群組的無效控制碼。</p></td>
</tr>
<tr class="odd">
<td><p>JET_LSNil<br />
 (~ (JET_LS) 0) </p></td>
<td><p>本機儲存區的控制碼無效。</p></td>
</tr>
<tr class="even">
<td><p>JET_dbidNil<br />
 ( (JET_DBID) 0xFFFFFFFF) </p></td>
<td><p>資料庫識別碼的控制碼無效。</p></td>
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
<td><p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p></td>
</tr>
<tr class="even">
<td><p><strong>伺服器</strong></p></td>
<td><p>需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</p></td>
</tr>
<tr class="odd">
<td><p><strong>標頭</strong></p></td>
<td><p>宣告于 Esent. h 中。</p></td>
</tr>
</tbody>
</table>

