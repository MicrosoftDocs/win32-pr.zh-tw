---
description: 提供對憑證的「擴充金鑰使用方法」 (EKU) 屬性的唯讀存取權。
ms.assetid: 636d7f65-d286-4800-a576-a23e6e9811b2
title: ExtendedKeyUsage 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 927e219e22bd0e87c444b1ca3cb63b09a5ddc2fb9ac74e63ebb8f66c6ed75437
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007316"
---
# <a name="extendedkeyusage-object"></a>ExtendedKeyUsage 物件

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509EnhancedKeyUsageExtension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1)。\]

**ExtendedKeyUsage** 物件提供對憑證的「擴充金鑰使用方法」 (EKU) 屬性的唯讀存取權。

## <a name="members"></a>成員

**ExtendedKeyUsage** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**ExtendedKeyUsage** 物件具有這些屬性。



| 屬性                                                     | 存取類型          | 描述                                                                                                                             |
|:-------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**Eku**](extendedkeyusage-ekus.md)<br/>             | 唯讀<br/> | [**Eku**](ekus.md) 集合，其中包含憑證的 [**EKU**](eku.md) 物件。<br/>                            |
| [**IsCritical**](extendedkeyusage-iscritical.md)<br/> | 唯讀<br/> | 抓取 **布林** 值，指出 EKU 延伸是否標記為重大。<br/>                                   |
| [**IsPresent**](extendedkeyusage-ispresent.md)<br/>   | 唯讀<br/> | 抓取 **布林** 值，指出 EKU 延伸是否存在。<br/> 這是預設屬性。 <br/> |



 

## <a name="remarks"></a>備註

無法建立 **ExtendedKeyUsage** 物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**加密物件**](cryptography-objects.md)
</dt> </dl>

 

 
