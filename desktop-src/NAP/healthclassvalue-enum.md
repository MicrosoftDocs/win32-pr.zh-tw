---
title: 'HealthClassValue 列舉 (NapProtocol) '
description: 表示健全狀況類別 TLV 的值。
ms.assetid: af80c27a-a686-494b-8795-73eb366deaa0
keywords:
- HealthClassValue 列舉 NAP
topic_type:
- apiref
api_name:
- HealthClassValue
api_location:
- NapProtocol.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b76b3fef268417f14bf22d2e25539a245cebc31820b746847f1e7b1091492b82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891638"
---
# <a name="healthclassvalue-enumeration"></a>HealthClassValue 列舉

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**HealthClassValue** 列舉型別會指出健全狀況類別 TLV 的值。

## <a name="syntax"></a>Syntax


```C++
typedef enum tagHealthClassValue { 
  healthClassFirewall        = 0,
  healthClassPatchLevel      = 1,
  healthClassAntiVirus       = 2,
  healthClassCriticalUpdate  = 3,
  healthClassReserved        = 128
} HealthClassValue;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="healthClassFirewall"></span><span id="healthclassfirewall"></span><span id="HEALTHCLASSFIREWALL"></span>**healthClassFirewall**
</dt> <dd>

健康情況類別的 TLV 是防火牆。

</dd> <dt>

<span id="healthClassPatchLevel"></span><span id="healthclasspatchlevel"></span><span id="HEALTHCLASSPATCHLEVEL"></span>**healthClassPatchLevel**
</dt> <dd>

健全狀況類別的 TLV 是修補程式等級。

</dd> <dt>

<span id="healthClassAntiVirus"></span><span id="healthclassantivirus"></span><span id="HEALTHCLASSANTIVIRUS"></span>**healthClassAntiVirus**
</dt> <dd>

健康情況類別的 TLV 是防毒軟體。

</dd> <dt>

<span id="healthClassCriticalUpdate"></span><span id="healthclasscriticalupdate"></span><span id="HEALTHCLASSCRITICALUPDATE"></span>**healthClassCriticalUpdate**
</dt> <dd>

健全狀況類別的 TLV 是重大更新。

</dd> <dt>

<span id="healthClassReserved"></span><span id="healthclassreserved"></span><span id="HEALTHCLASSRESERVED"></span>**healthClassReserved**
</dt> <dd>

保留供系統使用。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>NapProtocol。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapProtocol .idl</dt> </dl> |



 

 





