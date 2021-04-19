---
description: 代表憑證物件的集合。
ms.assetid: 11d294b5-0a8a-4970-be10-a3b22389d96e
title: 收件者物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c68ca0217631970f35680160b71841f758b13fd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985954"
---
# <a name="recipients-object"></a>收件者物件

\[[收件者 **] 物件可** 用於 [需求] 區段中指定的作業系統。 相反地，請使用 [**CmsRecipientCollection 類別**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

收件者物件代表 [**憑證**](certificate.md)**物件的集合**。 每個物件都代表封包訊息的預定收件者。 [**EnvelopedData**](envelopeddata.md)物件中的資料會使用 [*對稱*](../secgloss/s-gly.md)工作階段金鑰進行加密，而該對稱工作階段金鑰接著會使用來自該預定收件者憑證的公開金鑰，針對每個收件者進行加密。 具有與憑證 [*公開金鑰*](../secgloss/p-gly.md)相關聯之 [*私密金鑰*](../secgloss/p-gly.md)存取權的收件者，可以將 [*工作階段金鑰*](../secgloss/s-gly.md)解密，並使用解密的工作階段金鑰來解密實際的資料。

## <a name="when-to-use"></a>使用時機

收件 **者物件是** 用來執行下列工作：

-   新增或移除集合中的 [**憑證**](certificate.md) 物件。
-   取得集合中的憑證數目。
-   從集合中 **取出特定的** 收件者物件。
-   逐一查看集合。

## <a name="members"></a>成員

收件 **者物件有** 下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

收件 **者物件有** 這些方法。



| 方法                              | 描述                                                                            |
|:------------------------------------|:---------------------------------------------------------------------------------------|
| [**添加**](recipients-add.md)       | 將 [**憑證**](certificate.md) 物件加入至集合。<br/>         |
| [**清楚**](recipients-clear.md)   | 從集合中移除所有的 [**憑證**](certificate.md) 物件。<br/> |
| [**移除**](recipients-remove.md) | 從集合中移除 [**憑證**](certificate.md) 物件。<br/>    |



 

### <a name="properties"></a>屬性

收件 **者物件具有** 這些屬性。



| 屬性                                           | 存取類型          | Description                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](recipients-newenum.md)<br/> | 唯讀<br/> | 在可以用來列舉集合的物件上，抓取 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 介面。 這個屬性會在 Visual Basic Scripting Edition (VBScript) 中隱藏。<br/> |
| [**計數**](recipients-count.md)<br/>       |                      | 收件 **者集合中的物件** 數目。<br/>                                                                                                                                                              |
| [**項目**](recipients-item.md)<br/>         |                      | 集合中的索引物件。 這是預設屬性。<br/>                                                                                                                                                   |



 

## <a name="remarks"></a>備註

無法建立收件 **者物件。**

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**加密物件**](cryptography-objects.md)
</dt> </dl>

 

 
