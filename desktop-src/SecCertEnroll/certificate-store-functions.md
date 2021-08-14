---
description: 'Xenroll.dll 程式庫包含下列可用來管理憑證存放區的方法和屬性。FunctionsDescriptionCAStoreFlagsSpecifies 或傳回旗標，以控制 (CA) 存放區之憑證授權單位單位的存取權。CAStoreNameWStrSpecifies 或傳回 CA 存放區的名稱。CAStoreTypeWStrSpecifies 或傳回 CAStoreName 屬性所識別之存放區的類型。MyStoreFlagsSpecifies 或傳回旗標，此旗標會決定個人存放區的路徑。MyStoreNameWStrSpecifies 或傳回個人存放區的名稱。MyStoreTypeWStrSpecifies 或傳回個人存放區的類型。RequestStoreFlagsSpecifies 或傳回旗標，此旗標會決定要求存放區的路徑。RequestStoreNameWStrSpecifies 或傳回要求存放區的名稱。RequestStoreTypeWStrSpecifies 或傳回要求存放區的類型。RootStoreFlagsSpecifies 或傳回旗標，這個旗標會決定根存放區的路徑。RootStoreNameWStrSpecifies 或傳回根存放區的名稱。RootStoreTypeWStrSpecifies 或傳回根存放區的類型。SetHStoreCASpecifies CA 存放區的控制碼。SetHStoreMySpecifies 個人存放區的控制碼。SetHStoreRequestSpecifies 要求存放區的控制碼。SetHStoreROOTSpecifies 根存放區的控制碼。 '
ms.assetid: 15e4368b-4199-415a-9c2c-2c1351b717e6
title: 憑證存放區功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53a90a6fd2146517d4d70f653da42961274301a3058f8dbad9e72b8b90228bc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902172"
---
# <a name="certificate-store-functions"></a>憑證存放區功能

Xenroll.dll 程式庫包含下列可用來管理憑證存放區的方法和屬性。

| 函式                                                          | Description                                                                                                                                                                                          |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CAStoreFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castoreflags)                 | 指定或傳回旗標，以控制 (CA) 存放區的 [*憑證授權單位*](/windows/desktop/SecGloss/c-gly) 單位的存取權。<br/> |
| [**CAStoreNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castorenamewstr)           | 指定或傳回 CA 存放區的名稱。<br/>                                                                                                                                            |
| [**CAStoreTypeWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_castoretypewstr)           | 指定或傳回 **CAStoreName** 屬性所識別之存放區的類型。<br/>                                                                                                    |
| [**MyStoreFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystoreflags)                 | 指定或傳回旗標，這個旗標會決定個人存放區的路徑。<br/>                                                                                                               |
| [**MyStoreNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystorenamewstr)           | 指定或傳回個人存放區的名稱。<br/>                                                                                                                                      |
| [**MyStoreTypeWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_mystoretypewstr)           | 指定或傳回個人存放區的類型。<br/>                                                                                                                                      |
| [**RequestStoreFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststoreflags)       | 指定或傳回旗標，這個旗標會決定要求存放區的路徑。<br/>                                                                                                                |
| [**RequestStoreNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststorenamewstr) | 指定或傳回要求存放區的名稱。<br/>                                                                                                                                       |
| [**RequestStoreTypeWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_requeststoretypewstr) | 指定或傳回要求存放區的類型。<br/>                                                                                                                                       |
| [**RootStoreFlags**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstoreflags)             | 指定或傳回旗標，這個旗標會決定根存放區的路徑。<br/>                                                                                                                   |
| [**RootStoreNameWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstorenamewstr)       | 指定或傳回根存放區的名稱。<br/>                                                                                                                                          |
| [**RootStoreTypeWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll-get_rootstoretypewstr)       | 指定或傳回根存放區的類型。<br/>                                                                                                                                          |
| [**SetHStoreCA**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-sethstoreca)                   | 指定 CA 存放區的控制碼。<br/>                                                                                                                                                     |
| [**SetHStoreMy**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-sethstoremy)                   | 指定個人存放區的控制碼。<br/>                                                                                                                                               |
| [**SetHStoreRequest**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-sethstorerequest)         | 指定要求存放區的控制碼。<br/>                                                                                                                                                |
| [**SetHStoreROOT**](/windows/desktop/api/xenroll/nf-xenroll-ienroll2-sethstoreroot)               | 指定根存放區的控制碼。<br/>                                                                                                                                                   |



 

CertEnroll.dll 不會匯出功能，此功能可讓您指定或抓取存放區屬性值，或將憑證複製到特定存放區。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[將 Xenroll.dll 對應至 CertEnroll.dll](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> </dl>

 

