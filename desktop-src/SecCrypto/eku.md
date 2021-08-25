---
description: 代表憑證 (EKU) 屬性的單一擴充金鑰使用方式。
ms.assetid: 08eb7c77-0224-4ab5-99e7-edf18eb23c60
title: EKU 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKU
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: bd887204abc31583e596e94c25b64addcfe8109e6432845d25d939fd8e79e2d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875138"
---
# <a name="eku-object"></a>EKU 物件

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509EnhancedKeyUsageExtension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1)。\]

**Eku** 物件代表憑證 (EKU) 屬性的單一擴充金鑰使用方式。

## <a name="members"></a>成員

**EKU** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**EKU** 物件具有這些屬性。



| 屬性                            | 存取類型           | 描述                                                                                                                                                                                                   |
|:------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**名稱**](eku-name.md)<br/> | 讀取/寫入<br/> | 設定或抓取指定 EKU 之 CAPICOM 名稱的列舉值。 這是預設屬性。<br/>                                                                                   |
| [**老**](eku-oid.md)<br/>   | 讀取/寫入<br/> | 設定或抓取包含 EKU [*物件識別碼*](../secgloss/o-gly.md) 的字串， (OID) 字串值，如 Wincrypt 中所定義。<br/> |



 

## <a name="remarks"></a>備註

下列集合和屬性會使用 **EKU** 物件：

-   [**Eku**](ekus.md) 集合
-   [**CERTIFICATESTATUS EKU**](certificatestatus-eku.md) 屬性

無法建立 **EKU** 物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
