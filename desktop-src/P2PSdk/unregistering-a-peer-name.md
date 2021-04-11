---
description: 當您取消註冊對等名稱時，會從對等名稱解析通訊協定（ (PNRP) 雲端）移除已註冊的名稱。
ms.assetid: a451988e-7026-4b3c-a7a3-366f9886aa02
title: 取消註冊對等名稱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd482cc9cfd8c32d7bc95edd00e866e2d87b7a55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944274"
---
# <a name="unregistering-a-peer-name"></a><span data-ttu-id="3cd4b-103">取消註冊對等名稱</span><span class="sxs-lookup"><span data-stu-id="3cd4b-103">Unregistering a Peer Name</span></span>

<span data-ttu-id="3cd4b-104">當您取消註冊對等名稱時，會從對等名稱解析通訊協定（ (PNRP) 雲端）移除已註冊的名稱。</span><span class="sxs-lookup"><span data-stu-id="3cd4b-104">When you unregister a peer name, a registered name is removed from a Peer Name Resolution Protocol (PNRP) cloud.</span></span>

## <a name="unregistering-a-peer-name"></a><span data-ttu-id="3cd4b-105">取消註冊對等名稱</span><span class="sxs-lookup"><span data-stu-id="3cd4b-105">Unregistering a Peer Name</span></span>

<span data-ttu-id="3cd4b-106">若要取消註冊對等名稱，請呼叫 [**WSASetService**](pnrp-and-wsasetservice.md)。</span><span class="sxs-lookup"><span data-stu-id="3cd4b-106">To unregister a peer name, call [**WSASetService**](pnrp-and-wsasetservice.md).</span></span> <span data-ttu-id="3cd4b-107">*EssOperation* 參數的值必須為 **RNRSERVICE \_ DELETE**。</span><span class="sxs-lookup"><span data-stu-id="3cd4b-107">The *essOperation* parameter must have a value of **RNRSERVICE\_DELETE**.</span></span> <span data-ttu-id="3cd4b-108">您可以使用本主題的下列各節中的指導方針，對 **WSASetService** 參數和 [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) 結構進行必要的設定。</span><span class="sxs-lookup"><span data-stu-id="3cd4b-108">Use the guidelines in the following sections of this topic to make the required configurations to the **WSASetService** parameters and the [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure.</span></span>

## <a name="configuring-wsasetservice"></a><span data-ttu-id="3cd4b-109">設定 WSASetService</span><span class="sxs-lookup"><span data-stu-id="3cd4b-109">Configuring WSASetService</span></span>

<span data-ttu-id="3cd4b-110">當應用程式呼叫 [**WSASetService**](pnrp-and-wsasetservice.md)時，必須根據下列規格設定參數：</span><span class="sxs-lookup"><span data-stu-id="3cd4b-110">When an application calls [**WSASetService**](pnrp-and-wsasetservice.md), the parameters must be configured according to the following specifications:</span></span>

-   <span data-ttu-id="3cd4b-111">*essOperation* 的值必須為 **RNRSERVICE \_ DELETE**。</span><span class="sxs-lookup"><span data-stu-id="3cd4b-111">*essOperation* must have a value of **RNRSERVICE\_DELETE**.</span></span>
-   <span data-ttu-id="3cd4b-112">*dwFlags* 必須是零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="3cd4b-112">*dwFlags* must be zero (0).</span></span>
-   <span data-ttu-id="3cd4b-113">*lpqsRegInfo* 必須指向 [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) 結構，此結構必須使用本主題下一節中的指導方針進行設定。</span><span class="sxs-lookup"><span data-stu-id="3cd4b-113">*lpqsRegInfo* must point to a [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure, which must be configured by using the guidelines in the following section of this topic.</span></span>

## <a name="configuring-wsaqueryset"></a><span data-ttu-id="3cd4b-114">設定 WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="3cd4b-114">Configuring WSAQUERYSET</span></span>

<span data-ttu-id="3cd4b-115">[**WSAQUERYSET**](pnrp-and-wsaqueryset.md)結構必須根據下列規格進行設定：</span><span class="sxs-lookup"><span data-stu-id="3cd4b-115">The [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure must be configured according to the following specifications:</span></span>

-   <span data-ttu-id="3cd4b-116">**dwSize** 必須指定 [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) 結構的大小。</span><span class="sxs-lookup"><span data-stu-id="3cd4b-116">**dwSize** must specify the size the [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure.</span></span>
-   <span data-ttu-id="3cd4b-117">**lpszServiceInstanceName** 必須指向正在取消註冊的對等名稱。</span><span class="sxs-lookup"><span data-stu-id="3cd4b-117">**lpszServiceInstanceName** must point to the peer name that is being unregistered.</span></span>
-   <span data-ttu-id="3cd4b-118">**lpBlob** 必須指向 [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) 結構。</span><span class="sxs-lookup"><span data-stu-id="3cd4b-118">**lpBlob** must point to a [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure.</span></span>
-   <span data-ttu-id="3cd4b-119">**lpcsaBuffer** 必須指向地址清單。</span><span class="sxs-lookup"><span data-stu-id="3cd4b-119">**lpcsaBuffer** must point to the address list.</span></span>

> [!Note]  
> <span data-ttu-id="3cd4b-120">其餘成員將在 [**PNRP 和 WSASetService**](pnrp-and-wsasetservice.md)中說明。</span><span class="sxs-lookup"><span data-stu-id="3cd4b-120">The remaining members are described in [**PNRP and WSASetService**](pnrp-and-wsasetservice.md).</span></span>

 

## <a name="an-example-of-unregistering-a-peer-name"></a><span data-ttu-id="3cd4b-121">取消註冊對等名稱的範例</span><span class="sxs-lookup"><span data-stu-id="3cd4b-121">An Example of Unregistering a Peer Name</span></span>

<span data-ttu-id="3cd4b-122">下列程式碼片段示範如何在使用 [**WSAQUERYSET**](pnrp-and-wsaqueryset.md)結構呼叫 [**WSASetService**](pnrp-and-wsasetservice.md)時提供正確的資訊，以取消註冊對等名稱。</span><span class="sxs-lookup"><span data-stu-id="3cd4b-122">The following code snippet shows you how to unregister a peer name by providing the correct information when calling [**WSASetService**](pnrp-and-wsasetservice.md) using the [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure.</span></span>


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



 

 



