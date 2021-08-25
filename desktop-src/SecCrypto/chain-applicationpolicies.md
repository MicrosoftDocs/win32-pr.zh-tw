---
description: 傳回 Oid 集合，這個集合表示對鏈有效的應用程式原則 Oid。
ms.assetid: 4e4a7dce-5004-4b80-b132-3cdc0c048cde
title: IChain2：： ApplicationPolicies 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain.ApplicationPolicies
- IChain2.ApplicationPolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c5283ea684e1d84b64644891aa2819c3e37d20126ddd227a06ad3c38c7cb92bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877058"
---
# <a name="ichain2applicationpolicies-method"></a>IChain2：： ApplicationPolicies 方法

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Chain 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1)。\]

**ApplicationPolicies** 方法會傳回 [**oid**](oids.md)集合，以代表對鏈有效的應用程式原則 oid。

此方法是在 CAPICOM 2.0 中引進。

## <a name="syntax"></a>語法


```VB
Chain.ApplicationPolicies()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
