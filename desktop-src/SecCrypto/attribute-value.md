---
description: 設定或抓取屬性的值。
ms.assetid: aaf0c07c-756f-48c8-b4cd-def40f7cb1a3
title: Attribute。 Value 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 41737e086f1889531322115c8ff57e64c8893063f498b2566f0010f0f3f0ca30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773702"
---
# <a name="attributevalue-property"></a>Attribute。 Value 屬性

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista Windows XP。 請改用 [**system.string 命名空間中的**](/previous-versions/windows/) [**CryptographicAttributeObject 類別**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true)。\]

**Value** 屬性會設定或抓取屬性的值。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
Attribute.Value As Variant
```



## <a name="property-value"></a>屬性值

包含屬性值的 **Variant** 變數。 若為 **CAPICOM \_ 驗證的 \_ 屬性 \_ 簽署 \_ 時間** 屬性，資料類型為 **DATE**。 若為其他所有屬性，則屬性值為字串。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
