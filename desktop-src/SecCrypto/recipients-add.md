---
description: 將憑證物件加入至收件者集合。
ms.assetid: 2a1b9e0f-ccbf-4042-871b-397de6b6fc35
title: 收件者. 新增方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 255d17485e3423d50cd86b092c2120605f0f1106
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989746"
---
# <a name="recipientsadd-method"></a>收件者. 新增方法

\[**Add** 方法可用於 [需求] 區段中指定的作業系統。 相反地，請使用 [**CmsRecipientCollection 類別**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

**Add** 方法會將 [**憑證**](certificate.md)物件新增至收件 [**者集合。**](recipients.md)

## <a name="syntax"></a>語法


```VB
Recipients.Add( _
  ByVal Certificate _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*憑證* \[在\]
</dt> <dd>

解析為要加入至集合之 [**憑證**](certificate.md) 物件的運算式。

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

 

 
