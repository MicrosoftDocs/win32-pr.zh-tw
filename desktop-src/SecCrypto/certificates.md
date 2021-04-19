---
description: 代表憑證物件的集合。
ms.assetid: 82011c49-38fb-4261-8fb3-b76859da8a9e
title: 憑證物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2e8c12c16820342c5687720a35ce81aa7b94f180
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997439"
---
# <a name="certificates-object"></a>憑證物件

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2Collection 類別**](/previous-versions/windows/embedded/hh424013(v=msdn.10))。\]

**憑證** 物件代表 [**憑證**](certificate.md)物件的集合。 每個 [**憑證**](certificate.md) 物件都代表一個 [*數位憑證*](../secgloss/d-gly.md)。

**憑證** 物件會公開下列介面：

-   **ICertificates2**：在 CAPICOM 2.0 中引進。
-   **ICertificates**：在 CAPICOM 1.0 中引進。

## <a name="when-to-use"></a>使用時機

**憑證** 物件用來執行下列工作：

-   在集合中加入或移除 [**憑證**](certificate.md) 物件。
-   藉由尋找一組憑證或顯示對話方塊來選取憑證，以產生集合的子集。
-   清除集合中的所有 [**憑證**](certificate.md) 物件。
-   取得集合中的憑證數目。
-   從集合中取出特定的 [**憑證**](certificate.md) 物件。
-   逐一查看集合。

## <a name="members"></a>成員

**憑證** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**憑證** 物件有這些方法。



| 方法                                | 描述                                                                                                                                                           |
|:--------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**添加**](certificates-add.md)       | 將 [**憑證**](certificate.md) 物件加入至集合。<br/>  (繼承自 **CertificatesICertificates2**)                                         |
| [**清楚**](certificates-clear.md)   | 從集合中移除所有的 [**憑證**](certificate.md) 物件。<br/>  (繼承自 **CertificatesICertificates2**)                                 |
| [**Find**](certificates-find.md)     | 傳回 **憑證** 物件，其中包含符合指定之搜尋準則的所有憑證。<br/>  (繼承自 **CertificatesICertificates2**)  |
| [**移除**](certificates-remove.md) | 從集合中移除單一 [**憑證**](certificate.md) 物件。<br/>  (繼承自 **CertificatesICertificates2**)                             |
| [**儲存**](certificates-save.md)     | 將憑證儲存至指定的檔案。<br/>  (繼承自 **CertificatesICertificates2**)                                                                 |
| [**選取**](certificates-select.md) | 顯示用來選取憑證的對話方塊，並傳回選取的憑證集合。<br/>  (繼承自 **CertificatesICertificates2**)   |



 

### <a name="properties"></a>屬性

**憑證** 物件具有這些屬性。



| 屬性                                             | 存取類型          | Description                                                                                                                                                                                                                     |
|:-----------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](certificates-newenum.md)<br/> | 唯讀<br/> | 在可以用來列舉集合的物件上，抓取 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 介面。 這個屬性會在 Visual Basic Scripting Edition (VBScript) 中隱藏。<br/> |
| [**計數**](certificates-count.md)<br/>       | 唯讀<br/> | 抓取集合中的 [**憑證**](certificate.md) 物件數目。<br/>                                                                                                                                |
| [**項目**](certificates-item.md)<br/>         | 唯讀<br/> | 抓取代表集合之索引憑證的 [**憑證**](certificate.md) 物件。 這是預設屬性。<br/>  (繼承自 **CertificatesICertificates2ICertificates**)           |



 

## <a name="remarks"></a>備註

您可以建立 **憑證** 物件，而且可以安全地進行腳本處理。 **憑證** 物件的 ProgID 是「CAPICOM」。[憑證]。2。

**CAPICOM 1。*x*：** **憑證** 物件的 ProgID 是「CAPICOM」。憑證. 1」。

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

 

 
