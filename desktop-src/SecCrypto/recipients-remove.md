---
description: 從收件者集合移除憑證物件。
ms.assetid: bb75f6d0-4bab-40dd-9d0c-f0431da9c5f3
title: 收件者. 移除方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0da608dcafc8fc0c2341a053679dee0f8d2715c34dcbfb28e84bee02aa658093
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900758"
---
# <a name="recipientsremove-method"></a>收件者. 移除方法

\[**Remove** 方法可在 [需求] 區段中指定的作業系統中使用。 相反地，請使用 [**CmsRecipientCollection 類別**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

**Remove** 方法會從收件 [**者集合中**](recipients.md)移除 [**憑證**](certificate.md)物件。

## <a name="syntax"></a>語法


```VB
Recipients.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*索引* \[在\]
</dt> <dd>

要從集合移除之 [**憑證**](certificate.md) 物件的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**加密物件**](cryptography-objects.md)
</dt> <dt>

[**收件者**](recipients.md)
</dt> </dl>

 

 
