---
description: 您在設定應用程式的驗證等級時，便會決定當用戶端呼叫應用程式時，應執行何種程度的驗證。
ms.assetid: a59935de-6b8f-4c0a-8479-e30bc0509698
title: 設定伺服器應用程式的驗證層級
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83450b3f8d1939d08cc3d16a21f438c8da6f8fc1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972969"
---
# <a name="setting-an-authentication-level-for-a-server-application"></a><span data-ttu-id="070e7-103">設定伺服器應用程式的驗證層級</span><span class="sxs-lookup"><span data-stu-id="070e7-103">Setting an Authentication Level for a Server Application</span></span>

<span data-ttu-id="070e7-104">您在設定應用程式的驗證等級時，便會決定當用戶端呼叫應用程式時，應執行何種程度的驗證。</span><span class="sxs-lookup"><span data-stu-id="070e7-104">When you set an authentication level for an application, you determine what degree of authentication is performed when clients call into the application.</span></span> <span data-ttu-id="070e7-105">較高的驗證層級提供更高的安全性和資料完整性，不過通常會降低效能。</span><span class="sxs-lookup"><span data-stu-id="070e7-105">Higher authentication levels provide greater security and data integrity, although usually with some performance degradation.</span></span> <span data-ttu-id="070e7-106">如需詳細資訊，請參閱 [用戶端驗證](client-authentication.md)。</span><span class="sxs-lookup"><span data-stu-id="070e7-106">For more information, see [Client Authentication](client-authentication.md).</span></span>

<span data-ttu-id="070e7-107">**若要選取伺服器應用程式的驗證層級**</span><span class="sxs-lookup"><span data-stu-id="070e7-107">**To select an authentication level for a server application**</span></span>

1.  <span data-ttu-id="070e7-108">以滑鼠右鍵按一下您要設定驗證的 COM + 應用程式，然後按一下 [ **屬性**]。</span><span class="sxs-lookup"><span data-stu-id="070e7-108">Right-click the COM+ application for which you are setting authentication, and then click **Properties**.</span></span>

2.  <span data-ttu-id="070e7-109">在 [應用程式屬性] 對話方塊中，按一下 [ **安全性** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="070e7-109">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="070e7-110">在 [ **呼叫的驗證等級** ] 方塊中，選取適當的層級。</span><span class="sxs-lookup"><span data-stu-id="070e7-110">In the **Authentication level for calls** box, select the appropriate level.</span></span> <span data-ttu-id="070e7-111">層級如下所示，以最低到最高的安全性排序：</span><span class="sxs-lookup"><span data-stu-id="070e7-111">The levels are as follows, ordered from lowest to highest security:</span></span>

    -   <span data-ttu-id="070e7-112">**None**：</span><span class="sxs-lookup"><span data-stu-id="070e7-112">**None**.</span></span> <span data-ttu-id="070e7-113">不會進行驗證。</span><span class="sxs-lookup"><span data-stu-id="070e7-113">No authentication occurs.</span></span>
    -   <span data-ttu-id="070e7-114">**連接**。</span><span class="sxs-lookup"><span data-stu-id="070e7-114">**Connect**.</span></span> <span data-ttu-id="070e7-115">只有在進行連接之後才驗證認證。</span><span class="sxs-lookup"><span data-stu-id="070e7-115">Authenticates credentials only when the connection is made.</span></span>
    -   <span data-ttu-id="070e7-116">**呼叫**。</span><span class="sxs-lookup"><span data-stu-id="070e7-116">**Call**.</span></span> <span data-ttu-id="070e7-117">在一切呼叫的開始驗證認證。</span><span class="sxs-lookup"><span data-stu-id="070e7-117">Authenticates credentials at the beginning of every call.</span></span>
    -   <span data-ttu-id="070e7-118">封 **包**。</span><span class="sxs-lookup"><span data-stu-id="070e7-118">**Packet**.</span></span> <span data-ttu-id="070e7-119">驗證認證，並證實收到所有呼叫資料。</span><span class="sxs-lookup"><span data-stu-id="070e7-119">Authenticates credentials and verifies that all call data is received.</span></span> <span data-ttu-id="070e7-120">這是 COM+ 伺服器應用程式的預設值。</span><span class="sxs-lookup"><span data-stu-id="070e7-120">This is the default setting for COM+ server applications.</span></span>
    -   <span data-ttu-id="070e7-121">封 **包完整性**。</span><span class="sxs-lookup"><span data-stu-id="070e7-121">**Packet Integrity**.</span></span> <span data-ttu-id="070e7-122">驗證認證，並證實在傳輸中沒有呼叫資料被修改。</span><span class="sxs-lookup"><span data-stu-id="070e7-122">Authenticates credentials and verifies that no call data has been modified in transit.</span></span>
    -   <span data-ttu-id="070e7-123">封 **包隱私權**。</span><span class="sxs-lookup"><span data-stu-id="070e7-123">**Packet Privacy**.</span></span> <span data-ttu-id="070e7-124">驗證認證，並加密封包，包括資料和寄件人的識別 (Identity) 和簽章。</span><span class="sxs-lookup"><span data-stu-id="070e7-124">Authenticates credentials and encrypts the packet, including the data and the sender's identity and signature.</span></span>

4.  <span data-ttu-id="070e7-125">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="070e7-125">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="070e7-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="070e7-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="070e7-127">啟用程式庫應用程式的驗證</span><span class="sxs-lookup"><span data-stu-id="070e7-127">Enabling Authentication for a Library Application</span></span>](enabling-authentication-for-a-library-application.md)
</dt> </dl>

 

 



