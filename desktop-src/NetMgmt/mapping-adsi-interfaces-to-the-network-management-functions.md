---
title: 將 ADSI 介面對應到網路管理功能
description: Active Directory 服務介面 (ADSI) 是一組 COM 介面，可用來從不同的網路提供者存取目錄服務的功能。
ms.assetid: dfa81c58-3ce4-40ee-8bfc-a19a13781992
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ed9411989d5db754326a7a89130deada129fa6a58322ddef7e118772960d71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912047"
---
# <a name="mapping-adsi-interfaces-to-the-network-management-functions"></a>將 ADSI 介面對應到網路管理功能

Active Directory 服務介面 (ADSI) 是一組 COM 介面，可用來從不同的網路提供者存取目錄服務的功能。 ADSI 提供一組目錄服務介面，用來管理分散式運算環境中的網路資源。

如果您正在針對 Active Directory 進行程式設計，您可以呼叫特定的 ADSI 介面方法，以取得您可以藉由呼叫特定網路管理功能來達成的相同功能。

下表列出網路管理功能和函數群組，以及函式所對應的 ADSI 介面。



| 函式                                                                  | 介面                                                                                             |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**NetFileEnum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum)、 [ **NetFileGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) | [**IADsResource**](/windows/desktop/api/iads/nn-iads-iadsresource)、 [ **IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations) |
| [NetGroup](group-functions.md)\*                                          | [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup)                                                                        |
| [NetLocalGroup](local-group-functions.md)\*                               | [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup)                                                                        |
| [NetServer](server-functions.md)\*                                        | [**IADsComputer**](/windows/desktop/api/iads/nn-iads-iadscomputer)                                                                  |
| [NetSession](session-functions.md)\*                                      | [**IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession)、 [ **IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations)   |
| [NetShare](share-functions.md)\*                                          | [**IADsFileShare**](/windows/desktop/api/iads/nn-iads-iadsfileshare)                                                                |
| [NetUser](user-functions.md)\*                                            | [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser)、 [ **IADsComputer**](/windows/desktop/api/iads/nn-iads-iadscomputer)                                   |
| [NetUserModals](user-modal-functions.md)\*                                | [**IADsDomain**](/windows/desktop/api/iads/nn-iads-iadsdomain)                                                                      |



 

如需有關目錄服務和使用 ADSI 進行程式設計的詳細資訊，請參閱 [Active Directory 服務介面](/windows/desktop/ADSI/active-directory-service-interfaces-adsi)。 如需 WinNT 提供者可供使用者類別使用之自訂屬性的相關資訊，以及 WinNT 提供者不支援之 [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) 介面的屬性方法，請參閱 [ADSI WinNT 提供者](/windows/desktop/ADSI/adsi-winnt-provider)。

 

 