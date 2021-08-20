---
description: '[憑證] 屬性會抓取代表鏈中憑證的憑證集合。 這是預設屬性。'
ms.assetid: c3e6953f-35e5-469a-a1aa-e3a4ebe21ac3
title: IChain2：： certificate 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChain2.Certificates
- IChain2.get_Certificates
- IChain.Certificates
- IChain.get_Certificates
- Chain.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 16fb08d020dcd59ed7caf22a0e93f4a4866b58642f12d0c131f3f0368bd3e7e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769649"
---
# <a name="ichain2certificates-property"></a>IChain2：： certificate 屬性

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Chain 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1)。\]

[ **憑證** ] 屬性會抓取代表鏈中憑證的 [**憑證**](certificates.md) 集合。 這是預設屬性。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
Chain.Certificates As Certificates
```



## <a name="property-value"></a>屬性值

用來取得鏈中每個憑證相關資訊的 [**憑證**](certificates.md) 集合。 傳回之集合中的第一個憑證（certificate **. Item** (1) ）是鏈的最終憑證。 集合中的最後一個憑證（certificate **.** (Certificate **. Count**) ，是此鏈的 [*根憑證*](../secgloss/r-gly.md) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
