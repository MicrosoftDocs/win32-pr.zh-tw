---
description: 安全性服務提供者介面 (SSPI) 為安全的分散式應用程式提供通用的產業標準介面。
ms.assetid: c3cebb9d-9094-493f-96d3-763a0c282dfb
title: 安全性服務提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2121940337d0f4e06c53981cf30f0125180c466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985473"
---
# <a name="security-service-providers"></a><span data-ttu-id="bef8c-103">安全性服務提供者</span><span class="sxs-lookup"><span data-stu-id="bef8c-103">Security Service Providers</span></span>

<span data-ttu-id="bef8c-104">安全性服務提供者介面 (SSPI) 為安全的分散式應用程式提供通用的產業標準介面。</span><span class="sxs-lookup"><span data-stu-id="bef8c-104">The Security Service Provider Interface (SSPI) provides a universal, industry-standard interface for secure distributed applications.</span></span> <span data-ttu-id="bef8c-105">對等圖形 API 提供了一種方法，可讓應用程式藉由指定安全性服務提供者 (SSP) 來保護圖形中的連結，這是一個可實作為 SSPI 介面的 DLL。</span><span class="sxs-lookup"><span data-stu-id="bef8c-105">The Peer Graphing API provides a way for applications to secure links in a graph by specifying a Security Service Provider (SSP), which is a DLL that implements an SSPI interface.</span></span> <span data-ttu-id="bef8c-106">應用程式會在使用 [**PeerGraphCreate**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate)建立圖形時指定 SSP。</span><span class="sxs-lookup"><span data-stu-id="bef8c-106">An application specifies an SSP when it creates a graph by using [**PeerGraphCreate**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate).</span></span>

<span data-ttu-id="bef8c-107">如需建立您自己的 SSP 的詳細資訊，請參閱 [圖表參考連結](graphing-reference-links.md)清單中的 SSPI 檔連結。</span><span class="sxs-lookup"><span data-stu-id="bef8c-107">For more information about creating your own SSP, see the SSPI documentation link in the list of [Graphing Reference Links](graphing-reference-links.md).</span></span>

## <a name="programming-considerations-for-implementing-an-ssp"></a><span data-ttu-id="bef8c-108">執行 SSP 的程式設計考慮</span><span class="sxs-lookup"><span data-stu-id="bef8c-108">Programming Considerations for Implementing an SSP</span></span>

<span data-ttu-id="bef8c-109">從 SSP 內呼叫應用程式時，請特別小心。</span><span class="sxs-lookup"><span data-stu-id="bef8c-109">Use caution when calling into an application from within an SSP.</span></span> <span data-ttu-id="bef8c-110">下列考慮適用于 SSP 回呼：</span><span class="sxs-lookup"><span data-stu-id="bef8c-110">The following considerations apply to SSP callbacks:</span></span>

-   <span data-ttu-id="bef8c-111">回呼不應該花很長的時間來傳回，因為它們是在連接協商期間呼叫。</span><span class="sxs-lookup"><span data-stu-id="bef8c-111">Callbacks should not take a long time to return, because they are called during connection negotiation.</span></span> <span data-ttu-id="bef8c-112">如果建立連接需要太長的時間，可以卸載連接。</span><span class="sxs-lookup"><span data-stu-id="bef8c-112">If it takes too long for a connection to be established, the connection can be dropped.</span></span>
-   <span data-ttu-id="bef8c-113">對等圖形 API 會根據系統的實際負載，動態調整連接逾時值。</span><span class="sxs-lookup"><span data-stu-id="bef8c-113">The Peer Graphing API dynamically adjusts connection timeout values, based on the actual load of a system.</span></span> <span data-ttu-id="bef8c-114">最低的超時值為20秒。</span><span class="sxs-lookup"><span data-stu-id="bef8c-114">The lowest timeout value is 20 seconds.</span></span>
-   <span data-ttu-id="bef8c-115">為了避免潛在的鎖死情況，應用程式不能從回呼存取對等圖形資料庫。</span><span class="sxs-lookup"><span data-stu-id="bef8c-115">To avoid potential deadlock situations, an application must not access the peer graphing database from a callback.</span></span> <span data-ttu-id="bef8c-116">如果應用程式需要來自圖形資料庫的資訊，應用程式可以快取所需的資訊，然後從回呼內參考快取。</span><span class="sxs-lookup"><span data-stu-id="bef8c-116">If an application requires information from the graphing database, the application can cache the necessary information, and then refer to the cache from within the callback.</span></span> <span data-ttu-id="bef8c-117">快取也可協助縮短連線時間。</span><span class="sxs-lookup"><span data-stu-id="bef8c-117">Caching can also help decrease connection time.</span></span>

<span data-ttu-id="bef8c-118">呼叫 SSPI 進入點時，對等圖形基礎結構需要五個 (5) 函式的特定參數的特定值。</span><span class="sxs-lookup"><span data-stu-id="bef8c-118">When calling the SSPI entry points, the Peer Graphing Infrastructure requires specific values for specific parameters of five (5) functions.</span></span> <span data-ttu-id="bef8c-119">您無法變更提供給 SSP 的參數值，而且 SSP 可以忽略五個參數的值或正常處理這些參數的值。</span><span class="sxs-lookup"><span data-stu-id="bef8c-119">You cannot change these parameter values provided to SSP, and the SSP can either ignore the values for the five parameters or handle them gracefully.</span></span> <span data-ttu-id="bef8c-120">下列清單會識別這些特定參數和必要值：</span><span class="sxs-lookup"><span data-stu-id="bef8c-120">The following list identifies these specific parameters and required values:</span></span>

-   [<span data-ttu-id="bef8c-121">**AcquireCredentialsHandle**</span><span class="sxs-lookup"><span data-stu-id="bef8c-121">**AcquireCredentialsHandle**</span></span>](graphing-reference-links.md)

    <span data-ttu-id="bef8c-122">為 *pvGetKeyArgument* 參數指定一個 (1) 。</span><span class="sxs-lookup"><span data-stu-id="bef8c-122">Specify one (1) for the *pvGetKeyArgument* parameter.</span></span> <span data-ttu-id="bef8c-123">針對 *pszPrincipal*、 *pvLogonID* 和 *pGetKeyFn* 參數指定 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="bef8c-123">Specifies **NULL** for the *pszPrincipal*, *pvLogonID*, and *pGetKeyFn* parameters.</span></span>

-   [<span data-ttu-id="bef8c-124">**InitializeSecurityCoNtext**</span><span class="sxs-lookup"><span data-stu-id="bef8c-124">**InitializeSecurityContext**</span></span>](graphing-reference-links.md)

    <span data-ttu-id="bef8c-125">指定下列 *fCoNtextReq* 參數旗標： isc 要求 **\_ \_ 相互驗證的 \_ \| isc 要求 \_ \_ 機密性 isc \| 要求 \_ \_ 完整性 \| isc 要求 \_ 順序 \_ 偵測 \_ 到 \| isc \_ 需求 \_ 資料流程的 \| isc 要求 \_ \_ 配置 \_ 記憶體**。</span><span class="sxs-lookup"><span data-stu-id="bef8c-125">Specify the following flags for the *fContextReq* parameter: **ISC\_REQ\_MUTUAL\_AUTH \| ISC\_REQ\_CONFIDENTIALITY \| ISC\_REQ\_INTEGRITY \| ISC\_REQ\_SEQUENCE\_DETECT \| ISC\_REQ\_STREAM \| ISC\_REQ\_ALLOCATE\_MEMORY**.</span></span>

-   [<span data-ttu-id="bef8c-126">**AcceptSecurityCoNtext**</span><span class="sxs-lookup"><span data-stu-id="bef8c-126">**AcceptSecurityContext**</span></span>](graphing-reference-links.md)

    <span data-ttu-id="bef8c-127">為 *fCoNtextReq* 參數指定下列旗標： **asc 要求 \_ \_ 相互 \_ 驗證 asc \| 要求 \_ \_ 機密性 \| asc 要求 \_ \_ 完整性 asc 要求順序偵測 asc 要求 \| \_ \_ \_ \| \_ \_ 資料流程 \| asc \_ 需求 \_ 配置 \_ 記憶體**。</span><span class="sxs-lookup"><span data-stu-id="bef8c-127">Specify the following flags for the *fContextReq* parameter: **ASC\_REQ\_MUTUAL\_AUTH \| ASC\_REQ\_CONFIDENTIALITY \| ASC\_REQ\_INTEGRITY \| ASC\_REQ\_SEQUENCE\_DETECT \| ASC\_REQ\_STREAM \| ASC\_REQ\_ALLOCATE\_MEMORY**.</span></span>

-   [<span data-ttu-id="bef8c-128">**EncryptMessage**</span><span class="sxs-lookup"><span data-stu-id="bef8c-128">**EncryptMessage**</span></span>](graphing-reference-links.md)

    <span data-ttu-id="bef8c-129">針對 *fQOP* 和 *MessageSeqNo* 參數，指定零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="bef8c-129">Specify zero (0) for the *fQOP* and *MessageSeqNo* parameters.</span></span>

-   [<span data-ttu-id="bef8c-130">**DecryptMessage**</span><span class="sxs-lookup"><span data-stu-id="bef8c-130">**DecryptMessage**</span></span>](graphing-reference-links.md)

    <span data-ttu-id="bef8c-131">針對 *MessageSeqNo* 參數指定零 (0) ，針對 *PfQOP* 參數指定 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="bef8c-131">Specify zero (0) for the *MessageSeqNo* parameter and **NULL** for the *pfQOP* parameter.</span></span>

<span data-ttu-id="bef8c-132">呼叫 [**EncryptMessage**](graphing-reference-links.md)時，會在 **SecBufferDesc** 結構中傳遞四個緩衝區。</span><span class="sxs-lookup"><span data-stu-id="bef8c-132">When calling [**EncryptMessage**](graphing-reference-links.md), four buffers are passed in the **SecBufferDesc** structure.</span></span> <span data-ttu-id="bef8c-133">下表指出傳遞緩衝區的順序。</span><span class="sxs-lookup"><span data-stu-id="bef8c-133">The following table identifies the order to pass the buffers.</span></span>

| <span data-ttu-id="bef8c-134">SSP 特定結構</span><span class="sxs-lookup"><span data-stu-id="bef8c-134">SSP-specific structure</span></span>         | <span data-ttu-id="bef8c-135">Description</span><span class="sxs-lookup"><span data-stu-id="bef8c-135">Description</span></span>                                                                                                                                                                                                       |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bef8c-136">**之 SECBUFFER \_ 資料流程 \_ 標頭**</span><span class="sxs-lookup"><span data-stu-id="bef8c-136">**SECBUFFER\_STREAM\_HEADER**</span></span>  | <span data-ttu-id="bef8c-137">包含安全性標頭資料。</span><span class="sxs-lookup"><span data-stu-id="bef8c-137">Contains the security header data.</span></span> <span data-ttu-id="bef8c-138">標頭緩衝區的大小是藉由呼叫 [**QueryCoNtextAttributes**](graphing-reference-links.md) 並指定 **SECPKG \_ ATTR \_ 資料流程 \_ 大小** 屬性取得。</span><span class="sxs-lookup"><span data-stu-id="bef8c-138">The size of the header buffer is obtained by calling [**QueryContextAttributes**](graphing-reference-links.md) and specifying the **SECPKG\_ATTR\_STREAM\_SIZES** attribute.</span></span>  |
| <span data-ttu-id="bef8c-139">**之 SECBUFFER \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="bef8c-139">**SECBUFFER\_DATA**</span></span>            | <span data-ttu-id="bef8c-140">包含要加密的純文字訊息。</span><span class="sxs-lookup"><span data-stu-id="bef8c-140">Contains the plain-text message to be encrypted.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="bef8c-141">**之 SECBUFFER \_ 資料流程 \_ 結尾**</span><span class="sxs-lookup"><span data-stu-id="bef8c-141">**SECBUFFER\_STREAM\_TRAILER**</span></span> | <span data-ttu-id="bef8c-142">包含安全性尾端資料。</span><span class="sxs-lookup"><span data-stu-id="bef8c-142">Contains the security trailer data.</span></span> <span data-ttu-id="bef8c-143">標頭緩衝區的大小是藉由呼叫 [**QueryCoNtextAttributes**](graphing-reference-links.md) 並指定 **SECPKG \_ ATTR \_ 資料流程 \_ 大小** 屬性取得。</span><span class="sxs-lookup"><span data-stu-id="bef8c-143">The size of the header buffer is obtained by calling [**QueryContextAttributes**](graphing-reference-links.md) and specifying the **SECPKG\_ATTR\_STREAM\_SIZES** attribute.</span></span> |
| <span data-ttu-id="bef8c-144">**之 SECBUFFER \_ 空白**</span><span class="sxs-lookup"><span data-stu-id="bef8c-144">**SECBUFFER\_EMPTY**</span></span>           | <span data-ttu-id="bef8c-145">未初始化。</span><span class="sxs-lookup"><span data-stu-id="bef8c-145">Not initialized.</span></span> <span data-ttu-id="bef8c-146">此緩衝區的大小為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="bef8c-146">The size of this buffer is zero (0).</span></span>                                                                                                                                                             |



 

<span data-ttu-id="bef8c-147">呼叫 [**DecryptMessage**](graphing-reference-links.md)時，對等圖形 API 只會傳遞四個 **之 secbuffer** 結構。</span><span class="sxs-lookup"><span data-stu-id="bef8c-147">When calling [**DecryptMessage**](graphing-reference-links.md), the Peer Graphing API passes exactly four **SecBuffer** structures.</span></span> <span data-ttu-id="bef8c-148">第一個緩衝區是 **之 secbuffer \_ 資料**，並且包含加密的訊息。</span><span class="sxs-lookup"><span data-stu-id="bef8c-148">The first buffer is **SECBUFFER\_DATA**, and contains an encrypted message.</span></span> <span data-ttu-id="bef8c-149">其餘的緩衝區用於輸出，其類型為 **之 secbuffer \_ 空白**。</span><span class="sxs-lookup"><span data-stu-id="bef8c-149">The remaining buffers are used for output, and are of type **SECBUFFER\_EMPTY**.</span></span>

<span data-ttu-id="bef8c-150">SSP 需要在一次呼叫中支援加密和解密大小為16K 以上的使用者資料緩衝區。</span><span class="sxs-lookup"><span data-stu-id="bef8c-150">The SSP needs to support encrypting and decrypting user data buffers with sizes of 16K and greater in one call.</span></span>

 

 



