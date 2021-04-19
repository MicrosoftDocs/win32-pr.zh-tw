---
description: 深入瞭解： VistaApi. JetOpenTemporaryTable 方法
title: 'VistaApi. JetOpenTemporaryTable 方法 (< a0/&gt; < a1/&gt;) '
TOCTitle: 'JetOpenTemporaryTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOpenTemporaryTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetopentemporarytable(v=EXCHG.10)
ms:contentKeyID: 55104291
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOpenTemporaryTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOpenTemporaryTable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0a261494cf8b12039371c445a4cf2124f3ec1c52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981159"
---
# <a name="vistaapijetopentemporarytable-method"></a>VistaApi. JetOpenTemporaryTable 方法

使用單一索引建立臨時表。 臨時表會儲存和抓取記錄，就像使用 JetCreateTableColumnIndex 建立的一般資料表一樣。 不過，臨時表的速度會比一般資料表快許多，因為它們是暫時性的本質。 它們也可用來在以純粹順序存取的方式存取記錄集時，非常快速地排序和執行重複的移除。 另請參閱[JetOpenTempTable (JET_SESID、 \[ \] 、Int32、TempTableGrbit、JET_TABLEID、 \[ \]) ](./api.jetopentemptable-method.md)、 [JetOpenTempTable3 (JET_SESID、 \[ \] 、Int32、JET_UNICODEINDEX、TempTableGrbit、JET_TABLEID、 \[ \]) ](./api.jetopentemptable3-method.md)。

**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。    
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Sub JetOpenTemporaryTable ( _
    sesid As JET_SESID, _
    temporarytable As JET_OPENTEMPORARYTABLE _
)
'Usage
Dim sesid As JET_SESID
Dim temporarytable As JET_OPENTEMPORARYTABLEVistaApi.JetOpenTemporaryTable(sesid, _
    temporarytable)
```

``` csharp
public static void JetOpenTemporaryTable(
    JET_SESID sesid,
    JET_OPENTEMPORARYTABLE temporarytable
)
```

#### <a name="parameters"></a>參數

  - sesid  
    類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    要使用的會話。

<!-- end list -->

  - temporarytable  
    類型： [Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)  
    
    要在輸入上建立之臨時表的描述。 在成功呼叫之後，結構會包含臨時表和資料行標識的控制碼。 使用 [JetCloseTable (JET_SESID，JET_TABLEID) ](./api.jetclosetable-method.md) 在完成時釋放臨時表。

## <a name="remarks"></a>備註

在 Windows Vista 中引進。 針對較早版本的 Esent，請使用[JetOpenTempTable3 (JET_SESID、 \[ \] 、Int32、JET_UNICODEINDEX、TempTableGrbit、JET_TABLEID \[ \]) ](./api.jetopentemptable3-method.md) 。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[VistaApi 類別](./vistaapi-class.md)

[VistaApi 成員](./vistaapi-members.md)

[Microsoft.Isam.Esent.Interop.Vista namespace](./microsoft.isam.esent.interop.vista-namespace.md)
