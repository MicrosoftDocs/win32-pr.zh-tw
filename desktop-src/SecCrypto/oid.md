---
description: 代表數個 CAPICOM 屬性所使用 (OID) 的物件識別碼。
ms.assetid: d9dc2a9a-920b-41e1-91fb-da1628df577d
title: OID 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a524bfd8d2eb2edcf3c97919129dd694414d5ace
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994908"
---
# <a name="oid-object"></a>OID 物件

\[**OID** 物件可在 [需求] 區段中指定的作業系統中使用。 相反地，請在 [**system.object**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)命名空間中使用 [**Oid 類別**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1)。\]

**Oid** 物件代表數個 CAPICOM 屬性所使用 (OID) 的 [*物件識別碼*](../secgloss/o-gly.md)。

## <a name="when-to-use"></a>使用時機

**OID** 物件是用來執行下列工作：

-   設定或取得 OID 名稱和 OID 的顯示名稱。
-   設定或取出 OID 的點號。

## <a name="members"></a>成員

**OID** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**OID** 物件具有這些屬性。



| 屬性                                            | 存取類型           | Description                                                                                      |
|:----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [**FriendlyName**](oid-friendlyname.md)<br/> | 讀取/寫入<br/> | 設定或抓取 OID 的顯示名稱。<br/>                                       |
| [**Name**](oid-name.md)<br/>                 | 讀取/寫入<br/> | 為 OID 設定或抓取 CAPICOM 定義的名稱。 這是預設屬性。<br/> |
| [**值**](oid-value.md)<br/>               | 讀取/寫入<br/> | 設定或抓取 OID 的 OID 點值。<br/>                      |



 

## <a name="remarks"></a>備註

您可以建立 **OID** 物件，並且可以安全地進行腳本處理。 **OID** 物件的 PROGID 是 CAPICOM。OID. 1。

下列的 CAPICOM 物件屬性會傳回 **OID** 物件：

-   [**PolicyInformation OID**](policyinformation-oid.md)
-   [**限定詞。 OID**](qualifier-oid.md)
-   [**副檔名 OID**](extension-oid.md)
-   [**範本 OID**](template-oid.md)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
