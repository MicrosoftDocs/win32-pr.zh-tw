---
description: PNRP 命名空間提供者 API 會使用下列結構：
ms.assetid: 697fb99a-259f-429c-8818-0d725255bc86
title: PNRP 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a78e2ee85f3673395ade31417c79c010354f16b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974452"
---
# <a name="pnrp-structures"></a>PNRP 結構

PNRP 命名空間提供者 API 會使用下列結構：



| 結構                                                             | Description                                                                                                                                                         |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**對等 \_ PNRP \_ 端點 \_ 資訊**](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_endpoint_info)         | 包含與對等端點相關聯的 IP 位址和資料。                                                                                                 |
| [**對等 \_ PNRP \_ 雲端 \_ 資訊**](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_cloud_info)               | 包含 (PNRP) 雲端之對等名稱解析通訊協定的相關資訊。                                                                                            |
| [**對等 \_ PNRP \_ 註冊 \_ 資訊**](/windows/desktop/api/P2P/ns-p2p-peer_pnrp_registration_info) | 包含向 PNRP 雲端註冊時，對等身分識別所提供的資訊。                                                                           |
| [PNRP 和 BLOB](pnrp-and-blob.md)                                    | 呼叫多個函數時，將資料傳遞至 [**WSAQUERYSET**](winsock-nsp-reference-links.md) 結構。                                                  |
| [PNRP 和 WSAQUERYSET](pnrp-and-wsaqueryset.md)                      | 有助於解析名稱和雲端的名稱和列舉。                                                                                         |
| [**PNRP \_ 雲端 \_ 識別碼**](/windows/desktop/api/Pnrpdef/ns-pnrpdef-pnrp_cloud_id)                              | 包含定義網路雲端的值。                                                                                                                    |
| [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)                                | 由 [**WSAQUERYSET**](winsock-nsp-reference-links.md)結構的 **lpBlob** 成員指向。                                                            |
| [**PNRPINFO \_ V1**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)                                      | 由 [**WSAQUERYSET**](winsock-nsp-reference-links.md)結構的 **lpBlob** 成員指向                                                             |
| [**PNRPINFO \_ V2**](/previous-versions/windows/desktop/legacy/aa371671(v=vs.85))                                   | 由 [**WSAQUERYSET**](winsock-nsp-reference-links.md)結構的 **lpBlob** 成員指向，並提供應用程式特定的不透明資料的支援。 |



 

 

 
