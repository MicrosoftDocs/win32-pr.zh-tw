---
description: 憑證註冊 API 支援下列一般使用介面。
ms.assetid: 6b9d9761-6131-4408-8177-5418abd5e406
title: Helper 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aec54f9e092bb7675f18a28e7af8599a4e870b5aec1d88d0c5d3332c33c2bef4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117779537"
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

 

 



