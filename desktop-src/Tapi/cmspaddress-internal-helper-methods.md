---
description: 下列清單包含內部 CMSP 位址方法。
ms.assetid: 2016a776-1464-46b5-96b9-b045834f9e38
title: CMSPAddress 內部 Helper 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17064d161e2a073addb2e8eef6d9d290b41278b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991944"
---
# <a name="cmspaddress-internal-helper-methods"></a>CMSPAddress 內部 Helper 方法



| CMSPAddress 內部 helper 方法                                        | Description                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetStaticTerminals**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getstaticterminals)               | 由 [**get \_ StaticTerminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_staticterminals) 和 [**EnumerateStaticTerminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratestaticterminals) 呼叫，以取得可用於此位址的靜態終端陣列。                                     |
| [**GetDynamicTerminalClasses**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getdynamicterminalclasses) | 由 [**get \_ DynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_dynamicterminalclasses) 和 [**EnumerateDynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratedynamicterminalclasses) 呼叫，以取得可在此位址上使用的動態終端機類別陣列。 |
| [**UpdateTerminalList**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-updateterminallist)               | 填入 MSP 的靜態終端機清單。                                                                                                                                                                                                                                |
| [**ReceiveTSPAddressData**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-receivetspaddressdata)         | 當 TSP 資料訊息要由位址處理，而不是由特定呼叫來處理時呼叫。                                                                                                                                                                    |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**CMSPAddress**](/windows/desktop/api/Mspaddr/nl-mspaddr-cmspaddress)
</dt> </dl>

 

 
