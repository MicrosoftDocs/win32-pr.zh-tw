---
description: PublicKey 方法會傳回憑證物件的公開金鑰物件。
ms.assetid: 9a7ea6d5-365e-4360-ab50-2bafcfaecaa0
title: PublicKey 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.PublicKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 47bf713038f048048613a0be17c8a0523e33c603fbc761b57c3a76ee163534be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126928"
---
# <a name="certificatepublickey-method"></a>PublicKey 方法

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2 類別**](/previous-versions/windows/embedded/hh424017(v=msdn.10))。\]

**PublicKey** 方法會傳回 [**憑證**](certificate.md)物件的公開金鑰物件。

## <a name="syntax"></a>語法


```VB
Certificate.PublicKey()
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



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**憑證**](certificate.md)
</dt> </dl>

 

 
