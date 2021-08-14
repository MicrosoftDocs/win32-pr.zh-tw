---
description: 設定或抓取與憑證相關聯的私密金鑰。
ms.assetid: 976d81b4-5cbe-4824-9087-9a908b0e60e5
title: Certificate. PrivateKey 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.PrivateKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 18e6acc2aa4b765e9219eff479280df814f1089dc27366c5d175dcdeda4fd890
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771552"
---
# <a name="certificateprivatekey-property"></a>Certificate. PrivateKey 屬性

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2 類別**](/previous-versions/windows/embedded/hh424017(v=msdn.10))。\]

**PrivateKey** 屬性會設定或抓取與憑證相關聯的私密金鑰。 這個屬性是在 CAPICOM 2.0 中引進。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
Certificate.PrivateKey As PrivateKey
```



## <a name="property-value"></a>屬性值

[**PrivateKey**](privatekey.md)物件，代表與憑證相關聯的私密金鑰。

## <a name="remarks"></a>備註

將 **PrivateKey** 屬性設定為 Nothing 時，不會移除私密金鑰與憑證之間的關聯，但不會刪除私密金鑰。 若要刪除私密金鑰，請呼叫 [**PrivateKey**](privatekey-delete.md) 方法，然後將此屬性設定為 Nothing。

\_ \_ \_ 從 web 應用程式設定時，此屬性會引發 CAPICOM E （不允許）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**憑證**](certificate.md)
</dt> </dl>

 

 
