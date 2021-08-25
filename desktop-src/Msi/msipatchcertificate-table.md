---
description: 識別用來數位簽署修補程式的可能簽署者憑證。
ms.assetid: 8f76c27d-92f1-4de7-a69c-fba877e0325d
title: MsiPatchCertificate 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f39d2bc3a05c8b3fe3f23cd7dce01da36e14ce1f3984f24e827606bbc44c1a77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913308"
---
# <a name="msipatchcertificate-table"></a>MsiPatchCertificate 資料表

MsiPatchCertificate 資料表會識別用來數位簽署修補程式的可能簽署者憑證。 MsiPatchCertificate 資料表包含啟用應用程式的 [使用者帳戶控制 (UAC) 修補](user-account-control--uac--patching.md) 所需的資訊。

MsiPatchCertificate 資料表具有下列資料行：



| Column               | 類型                         | 答案 | Nullable |
|----------------------|------------------------------|-----|----------|
| PatchCertificate     | [識別碼](identifier.md) | Y   | N        |
| DigitalCertificate\_ | [識別碼](identifier.md) | N   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="PatchCertificate"></span><span id="patchcertificate"></span><span id="PATCHCERTIFICATE"></span>PatchCertificate
</dt> <dd>

MsiPatchCertificate 資料表中這個資料列的唯一識別碼。

</dd> <dt>

<span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate
</dt> <dd>

[MsiDigitalCertificate 資料表](msidigitalcertificate-table.md)的第一個資料行中的外部索引鍵。 MsiDigitalCertificate 資料表中指出的資料列包含簽署者憑證的二進位標記法。

</dd> </dl>

## <a name="remarks"></a>備註

在套用修補程式時，一律會針對目前的 MsiPatchCertificate 資料表評估修補程式。 Patch 可以藉由新增或移除專案來修改 MsiPatchCertificate 資料表。 這可讓修補程式修改稍後在修補順序中套用的未來修補程式評估。 資料表中可以有多個憑證，且修補程式必須至少符合一個要套用的憑證。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE81](ice81.md)  
</dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DisableLUAPatching](disableluapatching.md)
</dt> <dt>

[ (UAC) 修補的使用者帳戶控制](user-account-control--uac--patching.md)
</dt> <dt>

[**MSIDISABLELUAPATCHING**](msidisableluapatching.md)
</dt> <dt>

[數位簽章和 Windows Installer](digital-signatures-and-windows-installer.md)
</dt> <dt>

[Windows Installer 2.0 及更早版本不支援](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



