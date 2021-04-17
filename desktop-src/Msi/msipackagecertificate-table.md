---
description: MsiPackageCertificate 資料表會列出數位簽章憑證，用來驗證讓此 Multiple-Package 安裝的安裝套件身分識別。
ms.assetid: d3a97325-2136-4745-8a7d-57e4d6b9d27e
title: MsiPackageCertificate 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fd39ac93ff24da2fa8334a6e4865172471080b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195276"
---
# <a name="msipackagecertificate-table"></a>MsiPackageCertificate 資料表

MsiPackageCertificate 資料表會列出用來驗證安裝封裝之身分識別的數位簽章憑證，以進行 [多套件安裝](multiple-package-installations.md)。

您可以使用此資料表，針對包含多個 Windows Installer 套件的產品，撰寫 [多套件安裝](multiple-package-installations.md) 。 如果第一個封裝經過數位簽署，而包含的 MsiPackageCertificate 資料表指定產品中所有其餘套件的數位憑證，則系統管理員只需要針對第一個套件顯示 (UAC) 提示字元，接受 [*使用者帳戶控制*](u-gly.md) 。 在接受 UAC 的第一個封裝提示之後， [MsiEmbeddedChainer 資料表](msiembeddedchainer-table.md) 中的使用者定義函數接著可以將其餘套件加入多套件安裝，而不需要顯示 UAC 提示字元，而且需要每個套件的系統管理員回應。

如果 [MsiEmbeddedChainer 資料表](msiembeddedchainer-table.md) 中的一或多個函式要求未簽署的封裝，則會針對每個未簽署的套件顯示另一個需要系統管理員互動的 UAC 提示。 如果系統管理員接受此 UAC 提示，則會繼續執行多套件安裝。 系統管理員為套件提供認證之後，在此多套件安裝期間不會再顯示該套件的任何 UAC 提示。 如果系統管理員拒絕封裝的 UAC 提示，Windows installer 會在認可安裝任何屬於產品的封裝之前，回復多套件安裝。

**[Windows Installer 4.0 或更早版本](not-supported-in-windows-installer-4-0.md)：** 不支援。 從 Windows Installer 4.5 開始，可以使用此資料表。

MsiPackageCertificate 資料表具有下列資料行：



| Column               | 類型                         | 答案 | Nullable |
|----------------------|------------------------------|-----|----------|
| PackageCertificate   | [識別碼](identifier.md) | Y   | N        |
| DigitalCertificate\_ | [識別碼](identifier.md) | N   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="PackageCertificate"></span><span id="packagecertificate"></span><span id="PACKAGECERTIFICATE"></span>PackageCertificate
</dt> <dd>

MsiPackageCertificate 資料表中這個資料列的唯一識別碼。

</dd> <dt>

<span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate
</dt> <dd>

[MsiDigitalCertificate 資料表](msidigitalcertificate-table.md)的第一個資料行中的外部索引鍵。 MsiDigitalCertificate 資料表中指出的資料列包含簽署者憑證的二進位標記法。

</dd> </dl>

## <a name="validation"></a>驗證

<dl>

[ICE39](ice39.md)  
[ICE81](ice81.md)  
</dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[MsiEmbeddedChainer](msiembeddedchainer-table.md)
</dt> <dt>

[MsiDigitalCertificate 資料表](msidigitalcertificate-table.md)
</dt> </dl>

 

 



