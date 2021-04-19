---
description: 提供存取擴充功能的原則資訊。
ms.assetid: 03d627b3-2d44-4637-97a4-85cdcaf3e4d3
title: PolicyInformation 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PolicyInformation
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9d0cc89d6f993b72763083e69bb88e848134e8bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106975958"
---
# <a name="policyinformation-object"></a>PolicyInformation 物件

\[**PolicyInformation** 物件可用於 [需求] 區段中指定的作業系統。 相反地，請在 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中使用 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)，方法是呼叫採用 OID 作為參數的函式，然後使用憑證原則的 oid 來處理憑證原則延伸中的原則資訊。\]

**PolicyInformation** 物件可讓您存取延伸模組的原則資訊。

## <a name="when-to-use"></a>使用時機

**PolicyInformation** 物件是用來執行下列工作：

-   取出原則 OID。
-   取出原則的限定詞集合。

## <a name="members"></a>成員

**PolicyInformation** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**PolicyInformation** 物件具有這些屬性。



| 屬性                                                      | 描述                                                                                                 |
|:--------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**老**](policyinformation-oid.md)<br/>               | 以 [**oid**](oid.md) 物件形式抓取原則的 oid。 這是預設屬性。<br/>       |
| [**限定詞**](policyinformation-qualifiers.md)<br/> | 以 [**限定詞**](qualifiers.md) 物件形式抓取原則的限定詞集合。<br/> |



 

## <a name="remarks"></a>備註

無法建立 **PolicyInformation** 物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
