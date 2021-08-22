---
description: 深入瞭解： JET_OPENTEMPORARYTABLE cbKeyMost 屬性
title: 'JET_OPENTEMPORARYTABLE. cbKeyMost 屬性 (Microsoft. < a0/&gt; < a1/&gt;) '
TOCTitle: 'cbKeyMost property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbKeyMost
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable.cbkeymost(v=EXCHG.10)
ms:contentKeyID: 55104228
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbKeyMost
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.set_cbKeyMost
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbKeyMost
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.get_cbKeyMost
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 225c801770bb41337ee9f3ae248092c60441cd2e9a059f64897ad19053bfe30b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119107697"
---
# <a name="jet_opentemporarytablecbkeymost-property"></a>JET_OPENTEMPORARYTABLE cbKeyMost 屬性

取得或設定表示指定資料列之索引鍵的大小上限。 您可以設定最大索引鍵大小來控制如何截斷金鑰。 金鑰截斷很重要，因為它可能會影響資料列視為相異的時間。 如果此參數設定為0或255，則最大的索引鍵大小及其語義將維持與 Windows Server 2003 所支援的最大金鑰大小相同。 此參數也可以設定為較大的值，做為實例 [DatabasePageSize](./jet-param-enumeration.md)之資料庫頁面大小的功能。 如需詳細資訊，請參閱 [KeyMost](./vistaparam.keymost-field.md) 。

**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。    
**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。

## <a name="syntax"></a>Syntax

``` vb
'Declaration
Public Property cbKeyMost As Integer
    Get
    Set
'Usage
Dim instance As JET_OPENTEMPORARYTABLE
Dim value As Integer

value = instance.cbKeyMost

instance.cbKeyMost = value
```

``` csharp
public int cbKeyMost { get; set; }
```

#### <a name="property-value"></a>屬性值

類型： [system.object](/dotnet/api/system.int32)  

## <a name="see-also"></a>另請參閱

#### <a name="reference"></a>參考

[JET_OPENTEMPORARYTABLE 類別](./jet-opentemporarytable-class.md)

[JET_OPENTEMPORARYTABLE 成員](./jet-opentemporarytable-members.md)

[Microsoft.Isam.Esent.Interop.Vista namespace](./microsoft.isam.esent.interop.vista-namespace.md)
