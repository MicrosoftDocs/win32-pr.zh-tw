---
description: 從字串將先前編碼的憑證匯入到憑證物件中。
ms.assetid: 8515e034-08aa-4575-9b96-34cdee3ccba8
title: ICertificate2：： Import 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Import
- ICertificate2.Import
- ICertificate.Import
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ea639f1cd89b673ecf8da77302e3d812894a202b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987045"
---
# <a name="icertificate2import-method"></a>ICertificate2：： Import 方法

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2 類別**](/previous-versions/windows/embedded/hh424017(v=msdn.10))。\]

匯 **入** 方法會將先前編碼的憑證從字串匯入到 [**憑證**](certificate.md) 物件中。 呼叫這個方法會重設這個物件的 [*狀態*](../secgloss/s-gly.md) 。

## <a name="syntax"></a>語法


```VB
Certificate.Import( _
  ByVal EncodedCertificate _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*EncodedCertificate* \[在\]
</dt> <dd>

字串，包含要匯入的編碼憑證資料。

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



## <a name="see-also"></a>另請參閱

<dl> <dt>

[加密物件](cryptography-objects.md)
</dt> <dt>

[**憑證**](certificate.md)
</dt> </dl>

 

 
