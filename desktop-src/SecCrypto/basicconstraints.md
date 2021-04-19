---
description: 表示憑證的基本條件約束延伸。
ms.assetid: c21794f6-7654-4140-8114-0edb398d6de8
title: BasicConstraints 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 85e912542b09b02297f5119392115857259f70f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981654"
---
# <a name="basicconstraints-object"></a>BasicConstraints 物件

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista、Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/previous-versions/windows/)命名空間中的 [**X509BasicConstraintsExtension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1)。\]

**BasicConstraints** 物件代表憑證的基本限制延伸。

## <a name="when-to-use"></a>使用時機

**BasicConstraints** 物件是用來執行下列工作：

-   判斷基本條件約束延伸是否存在。
-   判斷基本條件約束延伸是否標記為重大。
-   判斷憑證是否受限於憑證授權單位單位。
-   判斷路徑長度條件約束是否存在，並取得路徑長度條件約束值。

## <a name="members"></a>成員

**BasicConstraints** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**BasicConstraints** 物件具有這些屬性。



| 屬性                                                                                     | 存取類型          | Description                                                                                                                                                                                                        |
|:---------------------------------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IsCertificateAuthority**](basicconstraints-iscertificateauthority.md)<br/>         | 唯讀<br/> | 取得布林值，指出憑證是否為證書 [*頒發機構*](../secgloss/c-gly.md) 單位 (CA) 。<br/> |
| [**IsCritical**](basicconstraints-iscritical.md)<br/>                                 | 唯讀<br/> | 抓取布林值，指出基本條件約束延伸是否標記為重大。<br/>                                                                                                     |
| [**IsPathLenConstraintPresent**](basicconstraints-ispathlenconstraintpresent.md)<br/> | 唯讀<br/> | 抓取布林值，指出憑證的路徑長度條件約束是否存在。<br/>                                                                                                   |
| [**IsPresent**](basicconstraints-ispresent.md)<br/>                                   | 唯讀<br/> | 抓取布林值，這個值會指出基本條件約束延伸是否存在。 這是預設屬性。<br/>                                                                              |
| [**PathLenConstraint**](basicconstraints-pathlenconstraint.md)<br/>                   | 唯讀<br/> | 抓取路徑長度條件約束的值。<br/>                                                                                                                                                      |



 

## <a name="remarks"></a>備註

無法建立 **BasicConstraints** 物件。

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
</dt> </dl>

 

 
