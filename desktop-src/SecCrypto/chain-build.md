---
description: 從終端憑證建立憑證驗證鏈至受信任的根憑證，並傳回布林值，指出鏈的整體有效性。
ms.assetid: 878f09ba-d79b-4f14-b4f6-ecb54771f56f
title: IChain2：： Build 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain.Build
- IChain2.Build
- IChain.Build
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 66ad51d94fdbd361a34e25b4b76289139abb87f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979888"
---
# <a name="ichain2build-method"></a>IChain2：： Build 方法

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Chain 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1)。\]

**Build** 方法會從終端憑證建立憑證驗證鏈至受信任的 [*根憑證*](../secgloss/r-gly.md)，並傳回布林值，指出鏈的整體有效性。

## <a name="syntax"></a>語法


```VB
Chain.Build( _
  ByVal Certificate _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*憑證* \[在\]
</dt> <dd>

[**憑證**](certificate.md)物件，代表要在其中建立驗證鏈的終端憑證。

</dd> </dl>

## <a name="return-value"></a>傳回值

指出鏈整體有效性的布林值。 整體有效性是以適當的有效性檢查原則為基礎。

## <a name="remarks"></a>備註

此鏈是使用 [**CertificateStatus CheckFlag**](certificatestatus-checkflag.md) 屬性，以及 [**CertificateStatus**](certificatestatus.md) 物件所指定的應用程式和憑證原則所建立。 傳回的集合已排序;集合中的第一個憑證（certificate **. Item** (1) ）是鏈的最終憑證。 集合中的最後一個憑證（certificate **.** (Certificate **. Count**) ，是此鏈的 [*根憑證*](../secgloss/r-gly.md) 。 **憑證。專案** (0) 代表整個鏈。

每次呼叫 **chain** 方法時，都會重設 [**連鎖店**](chain.md)物件的 [*狀態*](../secgloss/s-gly.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**加密物件**](cryptography-objects.md)
</dt> <dt>

[**鏈**](chain.md)
</dt> </dl>

 

 
