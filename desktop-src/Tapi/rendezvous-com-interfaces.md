---
description: 下表列出與會合會議控制項相關聯的 COM 物件和介面。
ms.assetid: d9634586-8315-46d3-9ffc-bfa9a4d7738e
title: 會合 COM 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6df7fbdac45480ae7aa9d5968209f22fabe9a4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971786"
---
# <a name="rendezvous-com-interfaces"></a>會合 COM 介面

\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

下表列出與會合會議控制項相關聯的 COM 物件和介面。

如需元件物件模型 (COM) 的詳細資訊，請參閱平臺軟體發展工具組 (SDK) 中的相關章節。



| 介面                                                         | Description                                                                                                               |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**IEnumDialableAddrs**](/windows/desktop/api/Rend/nn-rend-ienumdialableaddrs)                   | 列舉目前目錄中可用的可撥位址。                                                     |
| [**IEnumDirectory**](/windows/desktop/api/Rend/nn-rend-ienumdirectory)                           | 列舉 [**ITDirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory) 物件。                                                                    |
| [**IEnumDirectoryObject**](/windows/desktop/api/Rend/nn-rend-ienumdirectoryobject)               | 列舉 [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject) 物件。                                                        |
| [**IEnumMcastScope**](/windows/desktop/api/Mdhcp/nn-mdhcp-ienummcastscope)                         | 列舉 [**IMcastScope**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastscope) 物件。                                                                    |
| [**IEnumMedia**](ienummedia.md)                                   | 列舉 [**ITMedia**](itmedia.md) 物件。                                                                            |
| [**IEnumTime**](ienumtime.md)                                     | 列舉 [**ITTime**](ittime.md) 物件。                                                                              |
| [**IMcastAddressAllocation**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastaddressallocation)         | 多播位址配置的 COM 包裝函式的主要介面。                                                           |
| [**IMcastLeaseInfo**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastleaseinfo)                         | 提供方法來取得和設定位址租用資訊。                                                           |
| [**IMcastScope**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastscope)                                 | 封裝多播領域的所有屬性，並提供方法來取得範圍的相關資訊。             |
| [**ITAttributeList**](itattributelist.md)                         | 允許取得和設定未中斷的屬性。                                                                   |
| [**ITConferenceBlob**](itconferenceblob.md)                       | 提供對提供者特定會議資訊的存取。                                                              |
| [**ITConnection**](itconnection.md)                               | 提供可操作連接因素的方法，例如會議位址、範圍和頻寬。                       |
| [**ITDirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory)                                 | 取得和設定目錄資訊，並提供特定目錄物件的存取權。                                |
| [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject)                     | 取得和設定目錄內會議或使用者的一般資訊。                                            |
| [**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference) | 取得和設定會議特定的一般資訊，例如開始和停止時間。                                 |
| [**ITDirectoryObjectUser**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectuser)             | 取得和設定使用者專屬的一般資訊，例如使用者的主要 IP 電話之電腦的名稱。 |
| [**ITILSConfig**](/windows/desktop/api/Rend/nn-rend-itilsconfig)                                 | 取得和設定指定之 ILS 目錄之伺服器的特定資訊。                                                |
| [**ITMedia**](itmedia.md)                                         | 取得和設定基本媒體屬性，例如媒體名稱和傳輸通訊協定。                                       |
| [**ITMediaCollection**](itmediacollection.md)                     | 允許依索引存取媒體。 啟用媒體的建立和刪除。                                                     |
| [**ITRendezvous**](/windows/desktop/api/Rend/nn-rend-itrendezvous)                               | 會合控制項的主要介面。                                                                                |
| [**ITSdp**](itsdp.md)                                             | 操縱 SDP (會話描述通訊協定) blob。 參考： RFC 2327。                                             |
| [**ITTime**](ittime.md)                                           | 提供會話的一組啟用時間存取權。                                                             |
| [**ITTimeCollection**](ittimecollection.md)                       | 允許依索引進行時間元件存取。 可建立和刪除時間元件。                                  |



 

 

 



