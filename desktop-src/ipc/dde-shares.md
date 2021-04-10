---
description: DDE 共用是一種機器資源。
ms.assetid: 98d24300-52cc-4f0d-b74f-c58b823ac5f3
title: DDE 共用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 012c219897187c9e68b5b9e662b93678b77974c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849527"
---
# <a name="dde-shares"></a><span data-ttu-id="63170-103">DDE 共用</span><span class="sxs-lookup"><span data-stu-id="63170-103">DDE Shares</span></span>

<span data-ttu-id="63170-104">\[不再支援網路 DDE。</span><span class="sxs-lookup"><span data-stu-id="63170-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="63170-105">Windows Vista 上有 Nddeapi.dll，但是所有的函式呼叫都會傳回 NDDE \_ 未 \_ 執行。\]</span><span class="sxs-lookup"><span data-stu-id="63170-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="63170-106">DDE 共用是一種機器資源。</span><span class="sxs-lookup"><span data-stu-id="63170-106">DDE shares are a machine resource.</span></span> <span data-ttu-id="63170-107">它們類似于檔案共用，因為它們是用來控制對資源的存取。</span><span class="sxs-lookup"><span data-stu-id="63170-107">They are similar to file shares because they are used to control access to a resource.</span></span> <span data-ttu-id="63170-108">使用檔案共用時，資源為檔案。</span><span class="sxs-lookup"><span data-stu-id="63170-108">With file shares, the resource is a file.</span></span> <span data-ttu-id="63170-109">使用 DDE 共用時，資源會動態地交換資料。</span><span class="sxs-lookup"><span data-stu-id="63170-109">With DDE shares, the resource is dynamically exchanged data.</span></span> <span data-ttu-id="63170-110">交換的資料類型取決於提供資料的伺服器應用程式，以及要求資料的用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="63170-110">The type of data exchanged is determined by the server application that supplies the data and the client application that requests the data.</span></span>

<span data-ttu-id="63170-111">伺服器會呼叫 [**NDdeShareAdd**](nddeshareadd.md) 函式來建立 dde 共用，此共用儲存在 dde 共用資料庫管理員中， (DSDM) 。</span><span class="sxs-lookup"><span data-stu-id="63170-111">The server calls the [**NDdeShareAdd**](nddeshareadd.md) function to create the DDE share, which is stored in the DDE share database manager (DSDM).</span></span>

<span data-ttu-id="63170-112">用戶端會藉由連線至 DDE 共用來啟動 DDE 交談。</span><span class="sxs-lookup"><span data-stu-id="63170-112">The client starts the DDE conversation by connecting to the DDE share.</span></span> <span data-ttu-id="63170-113">用戶端必須呼叫 [**DdeInitialize**](/windows/win32/api/ddeml/nf-ddeml-ddeinitializea) 函式來初始化 DDEML，然後呼叫 [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) 函式以連接至 DDE 共用。</span><span class="sxs-lookup"><span data-stu-id="63170-113">The client must call the [**DdeInitialize**](/windows/win32/api/ddeml/nf-ddeml-ddeinitializea) function to initialize DDEML and call the [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) function to connect to the DDE share.</span></span> <span data-ttu-id="63170-114">在 **DdeConnect** 呼叫中，用戶端會指定服務名稱，如下所示：</span><span class="sxs-lookup"><span data-stu-id="63170-114">In the **DdeConnect** call, the client specifies the service name as follows:</span></span>

<span data-ttu-id="63170-115">\\\\*ComputerName* \\NDDE $</span><span class="sxs-lookup"><span data-stu-id="63170-115">\\\\*ComputerName*\\NDDE$</span></span>

<span data-ttu-id="63170-116">其中 *ComputerName* 是執行伺服器應用程式的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="63170-116">where *ComputerName* is the name of the computer running the server application.</span></span> <span data-ttu-id="63170-117">NDDE $ 表示提供給 [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) 的主題是名為 *ComputerName* 的遠端電腦上的 DDE 共用名稱。</span><span class="sxs-lookup"><span data-stu-id="63170-117">The NDDE$ indicates that the topic provided to [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) is the DDE share name on the remote computer named *ComputerName*.</span></span>

<span data-ttu-id="63170-118">有三種類型的 DDE 共用：舊樣式、新樣式和靜態。</span><span class="sxs-lookup"><span data-stu-id="63170-118">There are three types of DDE shares: old style, new style, and static.</span></span> <span data-ttu-id="63170-119">一般只支援靜態型別。</span><span class="sxs-lookup"><span data-stu-id="63170-119">It is typical to support only the static type.</span></span> <span data-ttu-id="63170-120">靜態共用的名稱使用下列慣例： *共用* 名 $。</span><span class="sxs-lookup"><span data-stu-id="63170-120">The names of static shares use the following convention: *ShareName*$.</span></span>

 

 
