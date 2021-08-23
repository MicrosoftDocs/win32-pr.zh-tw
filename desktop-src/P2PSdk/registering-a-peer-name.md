---
description: 若要註冊對等名稱，應用程式必須提供下列資訊： IP 位址 listPeer identityPeer nameIf 不安全的對等名稱，身分識別是選擇性的。
ms.assetid: 4de87146-3ea1-4019-9d3f-59de296083ae
title: 註冊對等名稱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41fcedbe3e405e21ec9709289e8a9237179703b1b8e81f40b449479373524beb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011486"
---
# <a name="registering-a-peer-name"></a>註冊對等名稱

若要註冊對等名稱，應用程式必須提供下列資訊：

-   IP 位址清單
-   [對等身分識別](creating-a-peer-identity.md)
-   [對等名稱](peer-names.md)

如果對等名稱是不安全的，則身分識別是選擇性的。 如果對等身分識別已指定為 **Null**，則對等名稱解析通訊協定 (PNRP) 會使用內部的預設對等身分識別。

## <a name="registering-a-peer-name"></a>註冊對等名稱

在識別 IP 位址清單、對等身分識別及對等名稱之後，應用程式可以藉由呼叫 [**WSASetService**](pnrp-and-wsasetservice.md)來註冊對等名稱。 您可以使用本主題的下列各節中的指導方針，對 **WSASetService** 參數和 [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) 結構進行必要的設定。

### <a name="configuring-wsasetservice"></a>設定 WSASetService

當應用程式呼叫 [**WSASetService**](pnrp-and-wsasetservice.md)時，必須根據下列規格設定參數：

-   *essOperation* 的值必須是 **RNRSERVICE \_ REGISTER**。
-   *dwFlags* 必須是零 (0) 。
-   *lpqsRegInfo* 必須指向 [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) 結構，此結構必須使用本主題的下列設定 **WSAQUERYSET** 一節中的指導方針進行設定。

### <a name="configuring-wsaqueryset"></a>設定 WSAQUERYSET

[**WSAQUERYSET**](pnrp-and-wsaqueryset.md)結構必須根據下列規格進行設定：

-   **dwSize** 必須指定 [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) 結構的大小。
-   **lpszServiceInstanceName** 必須指向正在註冊的對等名稱。
-   **lpBlob** 必須指向 [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) 結構。
-   **lpcsaBuffer** 必須指向地址清單。

> [!Note]  
> 其餘成員將在 [**PNRP 和 WSASetService**](pnrp-and-wsasetservice.md)中說明。

 

註冊對等名稱之後，對等基礎結構會提供資訊。 但是，註冊時間與其他節點的註冊資訊傳播之間會有延遲。 在這段期間，其他節點可能無法解析新註冊的對等。

## <a name="example-of-registering-a-peer-name"></a>註冊對等名稱的範例

下列程式碼片段示範如何在使用 [**WSAQUERYSET**](pnrp-and-wsaqueryset.md)結構呼叫 [**WSASetService**](pnrp-and-wsasetservice.md)時提供正確的資訊，以註冊對等名稱。


```C++
#define UNICODE
#include <initguid.h>
#include <p2p.h>

#pragma comment(lib, "ws2_32.lib")

//-------------------------------------------------------------------------
// Function: PnrpRegister
//
// Purpose:  Register the given name in the PNRP cloud
//
// Arguments:
//   pwzIdentity : identity string created using PeerIdentityCreate
//   pwzName     : name to register in PNRP
//   pwzCloud    : name of the cloud to register in, NULL = global cloud
//   pNodeInfo   : local node info returned from 

//
// Returns:  HRESULT
//
HRESULT PnrpRegister(PWSTR pwzIdentity, PWSTR pwzName, PWSTR pwzCloud, SOCKADDR_IN6* pAddress)
{
    HRESULT         hr = S_OK;
    CSADDR_INFO     csaAddr = {0};
    PNRPINFO        pnrpInfo = {0};
    BLOB            blPnrpData = {0};
    WSAQUERYSET     querySet = {0};
    INT             iRet;

    //
    // fill a CSADDR_INFO structure from the address
    //
    csaAddr.iProtocol = IPPROTO_TCP;
    csaAddr.iSocketType = SOCK_STREAM;
    csaAddr.LocalAddr.iSockaddrLength = sizeof(SOCKADDR_IN6);
    csaAddr.LocalAddr.lpSockaddr = (LPSOCKADDR)pAddress; 

    //
    // build the WSAQUERYSET required to register
    //
    pnrpInfo.dwSize = sizeof(pnrpInfo);
    pnrpInfo.dwLifetime = 60 * 60 * 8; //8 hours
    pnrpInfo.lpwszIdentity = pwzIdentity;

    blPnrpData.cbSize = sizeof(pnrpInfo);
    blPnrpData.pBlobData = (BYTE*)&pnrpInfo;

    querySet.dwSize = sizeof(querySet);
    querySet.dwNameSpace = NS_PNRPNAME;
    querySet.dwNumberOfCsAddrs = 1; // one address
    querySet.lpServiceClassId = (LPGUID)&SVCID_PNRPNAME;
    querySet.lpszServiceInstanceName = pwzName;
    querySet.lpszContext = pwzCloud;
    querySet.lpszComment = L"SomeComment";
    querySet.lpcsaBuffer = &csaAddr;
    querySet.lpBlob = &blPnrpData;

    // register the name with PNRP
    iRet = WSASetService(&querySet, RNRSERVICE_REGISTER, 0);
    if (iRet != 0)
    {
        hr = HRESULT_FROM_WIN32(WSAGetLastError());
    }
    
    return hr;
}
```



 

 



