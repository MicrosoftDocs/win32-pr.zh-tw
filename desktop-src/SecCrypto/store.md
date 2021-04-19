---
description: 提供屬性和方法，可讓您用來選擇、管理及使用憑證存放區和這些存放區中的憑證。
ms.assetid: de4eecf7-c03b-4733-ac29-d5b26b873dba
title: 存放區物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4e8a14fcecf0ded2e4e1a56e2b98e4ac4838b776
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984134"
---
# <a name="store-object"></a>存放區物件

\[**Store** 物件可在 [需求] 區段中指定的作業系統中使用。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**system.security.cryptography.x509certificates.x509store 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1)。\]

Store 物件提供屬性和方法，您可以使用這些屬性和方法來選擇、管理及使用這些 **存放** 區中的 [*憑證存放區*](../secgloss/c-gly.md) 和憑證。 CAPICOM 可以使用目前的使用者、本機電腦、記憶體和 Active Directory 存放區。 此外，存放區支援以智慧卡為基礎的憑證存放區。 開發人員應該注意，如果嘗試操作的使用者沒有許可權，某些存放區的某些方法可能會失敗。

## <a name="members"></a>成員

**Store** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Store** 物件具有這些方法。



| 方法                         | 描述                                                                                                                                                                                                      |
|:-------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**添加**](store-add.md)       | 將 [**憑證**](certificate.md) 物件新增至開啟的憑證存放區。<br/>                                                                                                                       |
| [**關閉**](store-close.md)   | 關閉開啟的憑證存放區。<br/> **CAPICOM 2.0.0.3 和更早版本：** 不支援 [**Close**](store-close.md) 方法。<br/>                                                               |
| [**刪除**](store-delete.md) | 刪除目前 [**存放區**](certificate.md) 物件所代表的憑證存放區。<br/> **CAPICOM 2.0.0.3 和更早版本：** 不支援 [**Delete**](store-delete.md) 方法。<br/> |
| [**出口**](store-export.md) | 匯出編碼 [*BLOB*](../secgloss/b-gly.md)的存放區。<br/>                                                                                                       |
| [**匯入**](store-import.md) | 匯入先前匯出的存放區。<br/>                                                                                                                                                                  |
| [**載入**](store-load.md)     | 從檔案將 [**憑證**](certificate.md) 物件匯入存放區。<br/>                                                                                                                        |
| [**打開**](store-open.md)     | 開啟憑證存放區。<br/>                                                                                                                                                                            |
| [**移除**](store-remove.md) | 從開啟的存放區中移除 [**憑證**](certificate.md) 物件。<br/>                                                                                                                               |



 

### <a name="properties"></a>屬性

**Store** 物件具有這些屬性。



| 屬性                                              | 存取類型          | Description                                                                                                                                                                                           |
|:------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**憑證**](store-certificates.md)<br/> | 唯讀<br/> | 抓取存放區的 [**憑證**](certificates.md) 集合。 這是預設屬性。<br/>                                                                                  |
| [**Location**](store-location.md)<br/>         | 唯讀<br/> | 抓取此物件所代表之憑證存放區的位置。<br/> **CAPICOM 2.0.0.3 和更早版本：** 不支援 [**Location**](store-location.md) 屬性。<br/> |
| [**Name**](store-name.md)<br/>                 | 唯讀<br/> | 抓取此物件所代表的憑證存放區名稱。<br/> **CAPICOM 2.0.0.3 和更早版本：** 不支援 [**Name**](store-name.md) 屬性。<br/>             |



 

## <a name="remarks"></a>備註

您可以建立 **存放區** 物件，而且可以安全地進行腳本處理。 **存放區** 物件的 PROGID 是 CAPICOM。存放區。2。

**CAPICOM 1。*x*：** **存放區** 物件的 ProgID 是 CAPICOM。Store. 1。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**加密物件**](cryptography-objects.md)
</dt> </dl>

 

 
