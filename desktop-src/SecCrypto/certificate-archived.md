---
description: 設定或抓取布林值，指出憑證是否已封存。
ms.assetid: a6526b0e-e76b-4f03-a6ba-9e380e362364
title: Certificate. 封存的屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Archived
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d2e3ab848caa24cb77a8cb45e992eeac7365af0de743fa148b07b484239fa658
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771947"
---
# <a name="certificatearchived-property"></a>Certificate. 封存的屬性

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1)。\]

封存 **的屬性會** 設定或抓取布林值，指出憑證是否已封存。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
Certificate.Archived As Boolean
```



## <a name="property-value"></a>屬性值

指出憑證是否已封存的布林值。 若 **為 true**，則表示憑證已封存。 請注意，將值從 **false** 變更為 **true** 會封存憑證。

## <a name="remarks"></a>備註

\_ \_ \_ 從 web 應用程式編寫腳本時，這個屬性不允許引發 CAPICOM E。

> [!Note]  
> 憑證管理使用者介面中看不到封存的憑證。 此外，封存的憑證將不會包含在 [**存放區中。**](store-open.md) 除非 \_ \_ \_ \_ 已指定 [CAPICOM 存放區開啟包含封存]，否則會開啟方法。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
