---
description: 深入瞭解： StopServiceGrbit 列舉
title: StopServiceGrbit 列舉 (Windows8) 的列舉
TOCTitle: StopServiceGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.stopservicegrbit(v=EXCHG.10)
ms:contentKeyID: 55104330
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.All
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.BackgroundUserTasks
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.QuiesceCaches
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.Resume
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.BackgroundUserTasks
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.All
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.QuiesceCaches
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.Resume
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7ecd096cc6d55aa989b758f7c30364844d160e59e5eba209f8e38c73ae87d0ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119603818"
---
# <a name="stopservicegrbit-enumeration"></a>StopServiceGrbit 列舉

[JetStopServiceInstance2 (JET_INSTANCE、StopServiceGrbit) ](./windows8api.jetstopserviceinstance2-method.md)的選項。

此列舉有 [FlagsAttribute](/dotnet/api/system.flagsattribute) 屬性，因此其成員值可進行位元組合。

**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration StopServiceGrbit
'Usage
Dim instance As StopServiceGrbit
```

``` csharp
[FlagsAttribute]
public enum StopServiceGrbit
```

## <a name="members"></a>成員

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th>成員名稱</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>全部</td>
<td>停止指定之實例的所有 ESE 服務。</td>
</tr>
<tr class="even">
<td></td>
<td>BackgroundUserTasks</td>
<td>停止可重新開機的用戶端指定背景維護工作 (B + 樹重組) 。</td>
</tr>
<tr class="odd">
<td></td>
<td>QuiesceCaches</td>
<td>將所有中途快取 Quiesces 至磁片。 非同步： 如果後續呼叫了 Resume 位，則會取消靜止。</td>
</tr>
<tr class="even">
<td></td>
<td>繼續</td>
<td>繼續先前發出的 StopService 作業，亦即 &quot; 重新開機服務 &quot; 。 可以與上述 grbits 結合以繼續特定服務，或使用0x0 繼續所有先前已停止的服務。
<p>警告：這個位只能用來繼續 JET_bitStopServiceBackground，JET_bitStopServiceQuiesceCaches，如果您已 JET_bitStopServiceAll 或 JET_bitStopServiceAPI，嘗試使用 JET_bitStopServiceResume 將會失敗。</p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Windows8 命名空間。](./microsoft.isam.esent.interop.windows8-namespace.md)
