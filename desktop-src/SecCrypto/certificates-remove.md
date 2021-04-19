---
description: 從集合中移除單一憑證物件。
ms.assetid: dff82825-1a7d-4c1a-94e2-7f9d1281ecf2
title: ICertificates2：： Remove 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Remove
- ICertificates2.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6a2f9336a420f1d014e178f67cae02cf85f0fd44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976216"
---
# <a name="icertificates2remove-method"></a>ICertificates2：： Remove 方法

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2Collection 類別**](/previous-versions/windows/embedded/hh424013(v=msdn.10))。\]

**Remove** 方法會從集合中移除單一 [**憑證**](certificate.md)物件。 此方法是在 CAPICOM 2.0 中引進。

## <a name="syntax"></a>語法


```VB
Certificates.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*索引* \[在\]
</dt> <dd>

要移除之 [**憑證**](certificate.md) 物件的索引值。 這個參數可以是下列其中一種可能的類型。



| 類型                                                                                                                                                                                                                                                              | 意義                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Long"></span><span id="long"></span><span id="LONG"></span><dl> <dt>* * * * 長 *</dt> * * <dt></dt> </dl>                                                | 已移除集合中指定索引處的 [**憑證**](certificate.md) 物件。<br/>                                                                                                          |
| <span id="String"></span><span id="string"></span><span id="STRING"></span><dl> <dt>* * * * 字串 * *</dt> * * <dt></dt> </dl>                                        | 集合中的第一個符合指定字串之 [*sha-1*](../secgloss/s-gly.md)指紋的 [**憑證**](certificate.md)物件會被移除。<br/> |
| <span id="Certificate"></span><span id="certificate"></span><span id="CERTIFICATE"></span><dl> <dt>**[**憑證**](certificate.md)**</dt><dt></dt> </dl> | 集合中符合指定 **憑證** 物件的第一個 [**憑證**](certificate.md)物件會被移除。<br/>                                                                           |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
