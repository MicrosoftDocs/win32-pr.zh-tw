---
description: 當您取消註冊對等名稱時，會從對等名稱解析通訊協定（ (PNRP) 雲端）移除已註冊的名稱。
ms.assetid: a451988e-7026-4b3c-a7a3-366f9886aa02
title: 取消註冊對等名稱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6ee0bd03e881f93321c31dfccd03cc71459b323f1ed356a88f829489c578a80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675008"
---
# <a name="unregistering-a-peer-name"></a>取消註冊對等名稱

當您取消註冊對等名稱時，會從對等名稱解析通訊協定（ (PNRP) 雲端）移除已註冊的名稱。

## <a name="unregistering-a-peer-name"></a>取消註冊對等名稱

若要取消註冊對等名稱，請呼叫 [**WSASetService**](pnrp-and-wsasetservice.md)。 *EssOperation* 參數的值必須為 **RNRSERVICE \_ DELETE**。 您可以使用本主題的下列各節中的指導方針，對 **WSASetService** 參數和 [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) 結構進行必要的設定。

## <a name="configuring-wsasetservice"></a>設定 WSASetService

當應用程式呼叫 [**WSASetService**](pnrp-and-wsasetservice.md)時，必須根據下列規格設定參數：

-   *essOperation* 的值必須為 **RNRSERVICE \_ DELETE**。
-   *dwFlags* 必須是零 (0) 。
-   *lpqsRegInfo* 必須指向 [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) 結構，此結構必須使用本主題下一節中的指導方針進行設定。

## <a name="configuring-wsaqueryset"></a>設定 WSAQUERYSET

[**WSAQUERYSET**](pnrp-and-wsaqueryset.md)結構必須根據下列規格進行設定：

-   **dwSize** 必須指定 [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) 結構的大小。
-   **lpszServiceInstanceName** 必須指向正在取消註冊的對等名稱。
-   **lpBlob** 必須指向 [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) 結構。
-   **lpcsaBuffer** 必須指向地址清單。

> [!Note]  
> 其餘成員將在 [**PNRP 和 WSASetService**](pnrp-and-wsasetservice.md)中說明。

 

## <a name="an-example-of-unregistering-a-peer-name"></a>取消註冊對等名稱的範例

下列程式碼片段示範如何在使用 [**WSAQUERYSET**](pnrp-and-wsaqueryset.md)結構呼叫 [**WSASetService**](pnrp-and-wsasetservice.md)時提供正確的資訊，以取消註冊對等名稱。


```C++
#define UNICODE
#include <initguid.h>
#include <p2p.h>

#pragma comment(lib, "ws2_32.lib")

//-------------------------------------------------------------------------
// Function: PnrpUnregister
//
// Purpose:  Unregister the given name from a PNRP cloud
//
// Arguments:
//   pwzIdentity : identity string originally used to register the name
//   pwzName     : name to unregister from PNRP
//   pwzCloud    : name of the cloud to unregister from, NULL = global cloud
//
// Returns:  HRESULT
//
HRESULT PnrpUnregister(PWSTR pwzIdentity, PWSTR pwzName, PWSTR pwzCloud)
{
    HRESULT         hr = S_OK;
    PNRPINFO        pnrpInfo = {0};
    BLOB            blPnrpData = {0};
    WSAQUERYSET     querySet = {0};
    INT             iRet;

    //
    // build the WSAQUERYSET required to unregister
    //
    pnrpInfo.dwSize = sizeof(pnrpInfo);
    pnrpInfo.dwLifetime = 60 * 60 * 8; // 8 hours
    pnrpInfo.lpwszIdentity = pwzIdentity;

    blPnrpData.cbSize = sizeof(pnrpInfo);
    blPnrpData.pBlobData = (BYTE*)&pnrpInfo;

    querySet.dwSize = sizeof(querySet);
    querySet.dwNameSpace = NS_PNRPNAME;
    querySet.lpServiceClassId = (LPGUID)&SVCID_PNRPNAME;
    querySet.lpszServiceInstanceName = pwzName;
    querySet.lpszContext = pwzCloud;
    querySet.lpBlob = &blPnrpData;

    // unregister the name with PNRP
    iRet = WSASetService(&querySet, RNRSERVICE_DELETE, 0);
    if (iRet != 0)
    {
        hr = HRESULT_FROM_WIN32(WSAGetLastError());
    }

    return hr;
}
```



 

 



