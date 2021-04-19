---
description: 憑證註冊 API 支援下列一般使用介面。
ms.assetid: 6b9d9761-6131-4408-8177-5418abd5e406
title: Helper 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9a0c6948e9b0fe09aee0b983d230f53bc8e76b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975859"
---
# <a name="helper-interfaces"></a>Helper 介面

憑證註冊 API 支援下列一般使用介面。



| 介面                                                                    | 描述                                                                                                                                                            |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IBinaryConverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter)                                 | 從位元組陣列建立 Unicode 編碼的字串、從 Unicode 編碼的字串建立位元組陣列，並修改套用至字串的 Unicode 編碼類型。 |
| [**ICertificateAttestationChallenge**](/windows/desktop/api/Certenroll/nn-certenroll-icertificateattestationchallenge) | 支援憑證證明挑戰。                                                                                                                           |
| [**IObjectId**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid)                                               | 表示物件識別碼。                                                                                                                                       |
| [**IObjectIds**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectids)                                             | 管理 [**IObjectId**](/windows/desktop/api/CertEnroll/nn-certenroll-iobjectid) 物件的集合。                                                                                                        |
| [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname)                     | 表示 x.500 辨別名稱。                                                                                                                                |
| [**IX509EndorsementKey**](/windows/desktop/api/Certenroll/nn-certenroll-ix509endorsementkey)                           | X.509 簽署金鑰介面                                                                                                                                        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[CertEnroll 介面](certenroll-interfaces.md)
</dt> </dl>

 

 



