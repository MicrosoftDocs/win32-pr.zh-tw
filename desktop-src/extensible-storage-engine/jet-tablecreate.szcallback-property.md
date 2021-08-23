---
description: 深入瞭解： JET_TABLECREATE szCallback 屬性
title: JET_TABLECREATE szCallback 屬性
TOCTitle: 'szCallback property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_TABLECREATE.szCallback
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tablecreate.szcallback(v=EXCHG.10)
ms:contentKeyID: 55103969
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.szCallback
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.set_szCallback
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.get_szCallback
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.szCallback
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 414abc99547a07f46902a355efcb42ce01cd6bde24c84d3a0ca309b008ef02c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729058"
---
# <a name="jet_tablecreateszcallback-property"></a>JET_TABLECREATE szCallback 屬性

取得或設定要用於資料表的回呼函數。 這是 "module \! functionName" 形式，並假設非受控碼。 如需替代方法，請參閱 **JetRegisterCallback (JET_SESID、JET_TABLEID、JET_cbtyp、JET_CALLBACK、IntPtr、JET_HANDLE)** 。

**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property szCallback As String
    Get
    Set
'Usage
Dim instance As JET_TABLECREATE
Dim value As String

value = instance.szCallback

instance.szCallback = value
```

``` csharp
public string szCallback { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： [system.string](/dotnet/api/system.string)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_TABLECREATE 類別](./jet-tablecreate-class.md)

[JET_TABLECREATE 成員](./jet-tablecreate-members.md)

[Microsoft. Esent 命名空間](./microsoft.isam.esent.interop-namespace.md)
