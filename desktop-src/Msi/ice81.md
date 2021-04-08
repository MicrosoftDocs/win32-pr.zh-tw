---
description: ICE81 會驗證 MsiDigitalCertificate 資料表、MsiDigitalSignature 資料表、MsiPatchCertificate 資料表和 MsiPackageCertificate 資料表。
ms.assetid: 83d8bc62-679e-410f-a95c-ffe13952b710
title: ICE81
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2fef8da1027fc739ce8e6e979ca998a1cd053a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691072"
---
# <a name="ice81"></a>ICE81

ICE81 會驗證 [MsiDigitalCertificate 資料表](msidigitalcertificate-table.md)、 [MsiDigitalSignature 資料表](msidigitalsignature-table.md)、 [MsiPatchCertificate 資料表](msipatchcertificate-table.md)和 [MsiPackageCertificate 資料表](msipackagecertificate-table.md)。 此 ICE 自訂動作會針對未使用或未參考的數位憑證張貼警告，並在簽署的物件不存在或簽署物件的封包未指向外部資料時張貼錯誤。

請注意，ICE03 會確認 MsiDigitalSignature 資料表的資料表資料行中的專案是 "Media"。

## <a name="result"></a>結果

ICE81 會針對未使用或未參考的數位憑證張貼下列警告。



| ICE81 警告                                                                                                                                                      | Description                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| 在 MsiDigitalSignature、MsiPackageCertificate 或 MsiPatchCertificate 資料表中，找不到 MsiDigitalCertificate 資料表中任何記錄的參考。 | 如果未使用所有記錄，則會傳回此警告。                |
| \[ \] 在 MsiDigitalSignature、MsiPackageCertificate 或 MsiPatchCertificate 資料表中，找不到數位憑證1的參考。                         | 如果未使用某些記錄（但不是全部），則會傳回此警告。 |



 

ICE81 會張貼下列錯誤。



| ICE81 錯誤                                                                                                                                                              | Description                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 媒體資料表不存在。 因此，MsiDigitalSignature 中的所有專案都不正確                                                                                   | 簽署的物件不存在。 如果媒體資料表不存在，但 MsiDigitalSignature 有專案，則會傳回此錯誤。                                |
| \[媒體資料表中缺少已簽署的物件 2 \]                                                                                                                               | 簽署的物件 \[ 2 不 \] 存在。 如果媒體資料表存在，就會傳回此錯誤，但在 MsiDigitalSignature 中的此專案不會出現在媒體資料表中。 |
| 具有金鑰2的表1中的專案 \[ \] \[ \] 已簽署。 因此，封包應該指向封裝外的物件， (封包的值不應加上前置詞 \#)  | 簽署物件的封包不會指向外部資料。 \[1 \] 是資料表名稱。 \[2 \] 是媒體資料表中的索引鍵。                                             |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



