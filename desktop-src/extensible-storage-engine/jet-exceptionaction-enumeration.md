---
description: 深入瞭解： JET_ExceptionAction 列舉
title: JET_ExceptionAction 列舉
TOCTitle: JET_ExceptionAction enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_ExceptionAction
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_exceptionaction(v=EXCHG.10)
ms:contentKeyID: 55103631
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ExceptionAction
- Microsoft.Isam.Esent.Interop.JET_ExceptionAction.MsgBox
- Microsoft.Isam.Esent.Interop.JET_ExceptionAction.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ExceptionAction.MsgBox
- Microsoft.Isam.Esent.Interop.JET_ExceptionAction
- Microsoft.Isam.Esent.Interop.JET_ExceptionAction.None
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0cba09666308ab55ae4327a9f9a683734aa28f41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971837"
---
# <a name="jet_exceptionaction-enumeration"></a>JET_ExceptionAction 列舉

要搭配 JET_paramExceptionAction 使用的常數。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Enumeration JET_ExceptionAction
'Usage
Dim instance As JET_ExceptionAction
```

``` csharp
public enum JET_ExceptionAction
```

## <a name="members"></a>成員

<table>
<thead>
<tr class="header">
<th></th>
<th>成員名稱</th>
<th>說明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>MsgBox</td>
<td>例外狀況時顯示訊息方塊。</td>
</tr>
<tr class="even">
<td></td>
<td>無</td>
<td>請勿處理例外狀況。 將它們擲回給呼叫者。</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
