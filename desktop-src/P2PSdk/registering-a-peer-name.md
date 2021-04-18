---
description: 若要註冊對等名稱，應用程式必須提供下列資訊： IP 位址 listPeer identityPeer nameIf 不安全的對等名稱，身分識別是選擇性的。
ms.assetid: 4de87146-3ea1-4019-9d3f-59de296083ae
title: 註冊對等名稱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b0944c4a41c02ff221aa1cc6a0b84ed881a9453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978267"
---
# <a name="registering-a-peer-name"></a><span data-ttu-id="00e84-103">註冊對等名稱</span><span class="sxs-lookup"><span data-stu-id="00e84-103">Registering a Peer Name</span></span>

<span data-ttu-id="00e84-104">若要註冊對等名稱，應用程式必須提供下列資訊：</span><span class="sxs-lookup"><span data-stu-id="00e84-104">To register a peer name, an application must provide the following information:</span></span>

-   <span data-ttu-id="00e84-105">IP 位址清單</span><span class="sxs-lookup"><span data-stu-id="00e84-105">IP address list</span></span>
-   [<span data-ttu-id="00e84-106">對等身分識別</span><span class="sxs-lookup"><span data-stu-id="00e84-106">Peer identity</span></span>](creating-a-peer-identity.md)
-   [<span data-ttu-id="00e84-107">對等名稱</span><span class="sxs-lookup"><span data-stu-id="00e84-107">Peer name</span></span>](peer-names.md)

<span data-ttu-id="00e84-108">如果對等名稱是不安全的，則身分識別是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="00e84-108">If a peer name is unsecured, an identity is optional.</span></span> <span data-ttu-id="00e84-109">如果對等身分識別已指定為 **Null**，則對等名稱解析通訊協定 (PNRP) 會使用內部的預設對等身分識別。</span><span class="sxs-lookup"><span data-stu-id="00e84-109">If a peer identity is specified as **NULL**, the Peer Name Resolution Protocol (PNRP) uses an internal, default peer identity.</span></span>

## <a name="registering-a-peer-name"></a><span data-ttu-id="00e84-110">註冊對等名稱</span><span class="sxs-lookup"><span data-stu-id="00e84-110">Registering a Peer Name</span></span>

<span data-ttu-id="00e84-111">在識別 IP 位址清單、對等身分識別及對等名稱之後，應用程式可以藉由呼叫 [**WSASetService**](pnrp-and-wsasetservice.md)來註冊對等名稱。</span><span class="sxs-lookup"><span data-stu-id="00e84-111">After the IP address list, peer identity, and peer name are identified, the application can register a peer name by calling [**WSASetService**](pnrp-and-wsasetservice.md).</span></span> <span data-ttu-id="00e84-112">您可以使用本主題的下列各節中的指導方針，對 **WSASetService** 參數和 [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) 結構進行必要的設定。</span><span class="sxs-lookup"><span data-stu-id="00e84-112">Use the guidelines in the following sections of this topic to make the required configurations to the **WSASetService** parameters and the [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure.</span></span>

### <a name="configuring-wsasetservice"></a><span data-ttu-id="00e84-113">設定 WSASetService</span><span class="sxs-lookup"><span data-stu-id="00e84-113">Configuring WSASetService</span></span>

<span data-ttu-id="00e84-114">當應用程式呼叫 [**WSASetService**](pnrp-and-wsasetservice.md)時，必須根據下列規格設定參數：</span><span class="sxs-lookup"><span data-stu-id="00e84-114">When an application calls [**WSASetService**](pnrp-and-wsasetservice.md), the parameters must be configured according to the following specifications:</span></span>

-   <span data-ttu-id="00e84-115">*essOperation* 的值必須是 **RNRSERVICE \_ REGISTER**。</span><span class="sxs-lookup"><span data-stu-id="00e84-115">*essOperation* must have a value of **RNRSERVICE\_REGISTER**.</span></span>
-   <span data-ttu-id="00e84-116">*dwFlags* 必須是零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="00e84-116">*dwFlags* must be zero (0).</span></span>
-   <span data-ttu-id="00e84-117">*lpqsRegInfo* 必須指向 [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) 結構，此結構必須使用本主題的下列設定 **WSAQUERYSET** 一節中的指導方針進行設定。</span><span class="sxs-lookup"><span data-stu-id="00e84-117">*lpqsRegInfo* must point to a [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure, which must be configured by using the guidelines in the following **Configuring WSAQUERYSET** section of this topic.</span></span>

### <a name="configuring-wsaqueryset"></a><span data-ttu-id="00e84-118">設定 WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="00e84-118">Configuring WSAQUERYSET</span></span>

<span data-ttu-id="00e84-119">[**WSAQUERYSET**](pnrp-and-wsaqueryset.md)結構必須根據下列規格進行設定：</span><span class="sxs-lookup"><span data-stu-id="00e84-119">The [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure must be configured according to the following specifications:</span></span>

-   <span data-ttu-id="00e84-120">**dwSize** 必須指定 [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) 結構的大小。</span><span class="sxs-lookup"><span data-stu-id="00e84-120">**dwSize** must specify the size the [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure.</span></span>
-   <span data-ttu-id="00e84-121">**lpszServiceInstanceName** 必須指向正在註冊的對等名稱。</span><span class="sxs-lookup"><span data-stu-id="00e84-121">**lpszServiceInstanceName** must point to the peer name that is being registered.</span></span>
-   <span data-ttu-id="00e84-122">**lpBlob** 必須指向 [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) 結構。</span><span class="sxs-lookup"><span data-stu-id="00e84-122">**lpBlob** must point to a [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure.</span></span>
-   <span data-ttu-id="00e84-123">**lpcsaBuffer** 必須指向地址清單。</span><span class="sxs-lookup"><span data-stu-id="00e84-123">**lpcsaBuffer** must point to the address list.</span></span>

> [!Note]  
> <span data-ttu-id="00e84-124">其餘成員將在 [**PNRP 和 WSASetService**](pnrp-and-wsasetservice.md)中說明。</span><span class="sxs-lookup"><span data-stu-id="00e84-124">The remaining members are described in [**PNRP and WSASetService**](pnrp-and-wsasetservice.md).</span></span>

 

<span data-ttu-id="00e84-125">註冊對等名稱之後，對等基礎結構會提供資訊。</span><span class="sxs-lookup"><span data-stu-id="00e84-125">After a peer name is registered, the information is available to the Peer Infrastructure.</span></span> <span data-ttu-id="00e84-126">但是，註冊時間與其他節點的註冊資訊傳播之間會有延遲。</span><span class="sxs-lookup"><span data-stu-id="00e84-126">However, there is a delay between the registration time and the propagation of the registration information to other nodes.</span></span> <span data-ttu-id="00e84-127">在這段期間，其他節點可能無法解析新註冊的對等。</span><span class="sxs-lookup"><span data-stu-id="00e84-127">During that time, other nodes may not be able to resolve the newly registered peer.</span></span>

## <a name="example-of-registering-a-peer-name"></a><span data-ttu-id="00e84-128">註冊對等名稱的範例</span><span class="sxs-lookup"><span data-stu-id="00e84-128">Example of Registering a Peer Name</span></span>

<span data-ttu-id="00e84-129">下列程式碼片段示範如何在使用 [**WSAQUERYSET**](pnrp-and-wsaqueryset.md)結構呼叫 [**WSASetService**](pnrp-and-wsasetservice.md)時提供正確的資訊，以註冊對等名稱。</span><span class="sxs-lookup"><span data-stu-id="00e84-129">The following code snippet shows you how to register a peer name by providing the correct information when calling [**WSASetService**](pnrp-and-wsasetservice.md) using the [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure.</span></span>


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



 

 



