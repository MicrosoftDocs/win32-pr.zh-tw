---
description: 從收件者集合移除所有的憑證物件。
ms.assetid: 456fcfbc-4388-40f4-ab58-04508ee2141b
title: 收件者. Clear 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients.Clear
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 7d9bd711bbc97997045989f2eb4ffdbc51ae3559
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994008"
---
# <a name="recipientsclear-method"></a>收件者. Clear 方法

\[**Clear** 方法可用於 [需求] 區段中指定的作業系統。 相反地，請使用 [**CmsRecipientCollection 類別**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

**Clear** 方法會從收件 [**者集合移除**](recipients.md)所有的 [**憑證**](certificate.md)物件。

## <a name="syntax"></a>語法


```VB
Recipients.Clear()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。 使用這個方法的應用程式必須包含程式碼，以處理此方法所引發的例外狀況。

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

 

 
