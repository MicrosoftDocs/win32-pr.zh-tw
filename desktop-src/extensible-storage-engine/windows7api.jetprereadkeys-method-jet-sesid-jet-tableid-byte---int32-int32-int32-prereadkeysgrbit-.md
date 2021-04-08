---
description: '深入瞭解： Windows7Api. JetPrereadKeys 方法 (JET_SESID、JET_TABLEID、Byte [] []、Int32、Int32、Int32、PrereadKeysGrbit) '
title: 'Windows7Api. JetPrereadKeys 方法 (JET_SESID、JET_TABLEID、Byte [] []、Int32、Int32、Int32、PrereadKeysGrbit)  (最為理想) '
TOCTitle: JetPrereadKeys method (JET_SESID, JET_TABLEID, Byte[][], Int32 , Int32, Int32, PrereadKeysGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows7.Windows7Api.JetPrereadKeys(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[][],System.Int32[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.Windows7.PrereadKeysGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows7.windows7api.jetprereadkeys(v=EXCHG.10)
ms:contentKeyID: 55107785
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Windows7.Windows7Api.JetPrereadKeys
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 66f85c08c1fccc58702d4ac4cf170d6b0493ab8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026081"
---
# <a name="windows7apijetprereadkeys-method-jet_sesid-jet_tableid-byte-int32--int32-int32-prereadkeysgrbit"></a>Windows7Api. JetPrereadKeys 方法 (JET_SESID、JET_TABLEID、Byte \[ \] \[ \] 、int32、int32、int32、PrereadKeysGrbit) 

如果具有指定索引鍵的記錄不在緩衝區快取中，則會啟動非同步讀取，以將記錄帶入資料庫緩衝區快取中。

**命名空間：**  [Microsoft 最為理想](./microsoft.isam.esent.interop.windows7-namespace.md)  
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>語法

``` vb
'Declaration
Public Shared Sub JetPrereadKeys ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    keys As Byte()(), _
    keyLengths As Integer(), _
    keyCount As Integer, _
    <OutAttribute> ByRef keysPreread As Integer, _
    grbit As PrereadKeysGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim keys As Byte()()
Dim keyLengths As Integer()
Dim keyCount As Integer
Dim keysPreread As Integer
Dim grbit As PrereadKeysGrbitWindows7Api.JetPrereadKeys(sesid, tableid, _
    keys, keyLengths, keyCount, keysPreread, _
    grbit)
```

``` csharp
public static void JetPrereadKeys(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[][] keys,
    int[] keyLengths,
    int keyCount,
    out int keysPreread,
    PrereadKeysGrbit grbit
)
```

#### <a name="parameters"></a>參數

  - sesid  
    類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    要使用的會話。

<!-- end list -->

  - tableid  
    類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    要針對其發出 prereads 的資料表。

<!-- end list -->

  - 金鑰  
    類型： \[\]  
    
    要 preread 的索引鍵。 金鑰必須經過排序。

<!-- end list -->

  - keyLengths  
    類型： \[\]  
    
    要 preread 的索引鍵長度。

<!-- end list -->

  - keyCount  
    類型： [system.object](/dotnet/api/system.int32)  
    
    要 preread 的索引鍵數目上限。

<!-- end list -->

  - keysPreread  
    類型： [system.object](/dotnet/api/system.int32)  
    
    傳回要實際 preread 的索引鍵數目。

<!-- end list -->

  - grbit  
    型別： [最為理想. PrereadKeysGrbit](./prereadkeysgrbit-enumeration.md)  
    
    Preread 選項。 用來指定 preread 的方向。

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[Windows7Api 類別](./windows7api-class.md)

[Windows7Api 成員](./windows7api-members.md)

[JetPrereadKeys 多載](./windows7api.jetprereadkeys-method.md)

[最為理想命名空間。](./microsoft.isam.esent.interop.windows7-namespace.md)
