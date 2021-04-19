---
description: 抓取封包訊息的收件者集合。
ms.assetid: de9cbf8e-f34c-4e08-89aa-b5ac842aa599
title: EnvelopedData [收件者] 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Recipients
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f047b4a8c579fb7f327b7410965a326c4a2f255d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995273"
---
# <a name="envelopeddatarecipients-property"></a>EnvelopedData [收件者] 屬性

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。 相反地，請使用 [**EnvelopedCms 類別**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

收件 **者屬性會** 抓取封包訊息的收件者集合。

## <a name="syntax"></a>Syntax


```VB
EnvelopedData.Recipients As Recipients
```



## <a name="property-value"></a>屬性值

代表封包訊息收件者的收件 [**者集合。**](recipients.md)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EnvelopedData**](envelopeddata.md)
</dt> </dl>

 

 
