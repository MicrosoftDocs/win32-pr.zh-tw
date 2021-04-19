---
description: 表示 OID 物件的集合。
ms.assetid: 2c4ff87a-58e1-46aa-9680-29062b05308c
title: Oid 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 894689c214d8b7d352a2453d2d62c847866b9bc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990105"
---
# <a name="oids-object"></a>Oid 物件

\[**Oid** 物件可在 [需求] 區段中指定的作業系統中使用。 請改用 [**system.string 命名空間中的**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) [**OidCollection 類別**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1)。\]

**Oid** 物件代表 [**oid**](oid.md)物件的集合。 每個 [**OID**](oid.md) 物件都代表一個物件識別碼。

## <a name="when-to-use"></a>使用時機

**Oid** 物件是用來執行下列工作：

-   從集合中加入或移除 [**OID**](oid.md) 物件。
-   清除集合中的所有 [**OID**](oid.md) 物件。
-   取得集合中的物件識別碼數目。
-   從集合中取出特定的 [**OID**](oid.md) 物件。
-   逐一查看集合。

## <a name="members"></a>成員

**Oid** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Oid** 物件具有這些方法。



| 方法                        | 描述                                                                  |
|:------------------------------|:-----------------------------------------------------------------------------|
| [**添加**](oids-add.md)       | 將 [**OID**](oid.md) 物件加入至集合。<br/>              |
| [**清楚**](oids-clear.md)   | 從集合中清除所有 [**OID**](oid.md) 物件。<br/>        |
| [**移除**](oids-remove.md) | 從集合中移除已編制索引的 [**OID**](oid.md) 物件。<br/> |



 

### <a name="properties"></a>屬性

**Oid** 物件具有這些屬性。



| 屬性                                     | 存取類型          | Description                                                                                                                                                                                                                     |
|:---------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](oids-newenum.md)<br/> | 唯讀<br/> | 在可以用來列舉集合的物件上，抓取 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 介面。 這個屬性會在 Visual Basic Scripting Edition (VBScript) 中隱藏。<br/> |
| [**計數**](oids-count.md)<br/>       | 唯讀<br/> | 抓取集合中的 [**OID**](oid.md) 物件數目。<br/>                                                                                                                                                |
| [**項目**](oids-item.md)<br/>         | 唯讀<br/> | 從集合中抓取索引的 [**OID**](oid.md) 物件。 這是預設屬性。<br/>                                                                                                                    |



 

## <a name="remarks"></a>備註

無法建立 **oid** 物件。

**Oid** 物件是由下列屬性使用：

-   [**CertificateStatus.ApplicationPolicies**](certificatestatus-applicationpolicies.md)
-   [**CertificateStatus.CertificatePolicies**](certificatestatus-certificatepolicies.md)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
