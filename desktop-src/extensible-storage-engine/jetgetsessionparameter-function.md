---
description: 深入瞭解： JetGetSessionParameter 函數
title: JetGetSessionParameter 函式
TOCTitle: JetGetSessionParameter Function
ms:assetid: 36fbcc06-a72d-4bfb-976b-1b705487732a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835039(v=EXCHG.10)
ms:contentKeyID: 49894661
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetGetSessionParameter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: effd1ea5a9489df0a85af54a79cd773cc05b2fa3d6dbe57096a61fbd4c79c25a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119472028"
---
# <a name="jetgetsessionparameter-function"></a>JetGetSessionParameter 函式


_**適用于：** Windows |Windows伺服器_

**JetGetSessionParameter** 函式會讀取指定會話的 session 參數。

**JetGetSessionParameter** 函式是在 Windows 8 作業系統中引進的。

``` c++
JET_ERR JET_API JetGetSessionParameter (
  __in_opt      JET_SESID sesid,
  __in          unsigned long sesparamid,
  __out_cap_post_count_(cbParamMax, *pcbParamActual)  void* pvParam,
  __in          unsigned long cbParamMax,
  __out_opt_    unsigned long pcbParamActual
);
```

### <a name="parameters"></a>參數

*sesid*

此呼叫所要使用的會話。

指定時，會忽略指定的實例，並使用與會話相關聯的實例。

*sesparamid*

要設定之會話參數的識別碼。

*pvParam*

此會話參數中的資料。

*cbParamMax*

此會話參數中資料集的大小上限。

*pcbParamActual*

此會話參數中資料集的實際大小。

### <a name="return-value"></a>傳回值

成功時，適用于所要求會話參數的輸出緩衝區將會設定為該會話參數的值。

失敗時，輸出緩衝區的狀態將會是未定義的。

#### <a name="remarks"></a>備註

Session 參數會用於會話的存留期，或在重設值之前使用。

#### <a name="requirements"></a>規格需求

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>用戶端</strong></p></td>
<td><p>需要 Windows 8。</p></td>
</tr>
<tr class="even">
<td><p><strong>伺服器</strong></p></td>
<td><p>需要 Windows Server 2012。</p></td>
</tr>
<tr class="odd">
<td><p><strong>標頭</strong></p></td>
<td><p>宣告于 Esent. h 中。</p></td>
</tr>
<tr class="even">
<td><p><strong>程式庫</strong></p></td>
<td><p>使用 ESENT。</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>需要 ESENT.dll。</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>另請參閱

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)  
[系統參數](./extensible-storage-engine-system-parameters.md)
