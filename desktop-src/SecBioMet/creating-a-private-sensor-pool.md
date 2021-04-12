---
title: 建立私人感應器集區
description: 如何使用 Windows 生物特徵辨識架構 API 來建立私人感應器集區。
ms.assetid: 79944E30-A3D4-411D-A551-3B309DEA6FEA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8eda88f8a9bd0befcbf5527e52d572ec7ca55ce2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372487"
---
# <a name="creating-a-private-sensor-pool"></a><span data-ttu-id="f1160-103">建立私人感應器集區</span><span class="sxs-lookup"><span data-stu-id="f1160-103">Creating a Private Sensor Pool</span></span>

<span data-ttu-id="f1160-104">私用感應器集區是保留給用戶端應用程式專用的生物識別單位集合。</span><span class="sxs-lookup"><span data-stu-id="f1160-104">A private sensor pool is a collection of biometric units reserved for exclusive use by a client application.</span></span> <span data-ttu-id="f1160-105">私人集區支援專屬的驗證方法，並可讓用戶端應用程式使用廠商指定的控制命令來存取生物識別單位。</span><span class="sxs-lookup"><span data-stu-id="f1160-105">Private pools support proprietary authentication methods and enable a client application to access a biometric unit by using vendor-specified control commands.</span></span>

<span data-ttu-id="f1160-106">下列主題包含的程式碼範例會示範如何建立私人感應器集區。</span><span class="sxs-lookup"><span data-stu-id="f1160-106">The following topics contain code examples that show how to create a private sensor pool.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f1160-107">本節內容</span><span class="sxs-lookup"><span data-stu-id="f1160-107">In this section</span></span>



| <span data-ttu-id="f1160-108">主題</span><span class="sxs-lookup"><span data-stu-id="f1160-108">Topic</span></span>                                                                         | <span data-ttu-id="f1160-109">描述</span><span class="sxs-lookup"><span data-stu-id="f1160-109">Description</span></span>                                                                                          |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f1160-110">感應器集區</span><span class="sxs-lookup"><span data-stu-id="f1160-110">Sensor Pools</span></span>](sensor-pools.md)<br/>                                   | <span data-ttu-id="f1160-111">描述三種可能的感應器集區：系統、私人和未指派。</span><span class="sxs-lookup"><span data-stu-id="f1160-111">Describes three possible sensor pools: system, private, and unassigned.</span></span><br/>                   |
| [<span data-ttu-id="f1160-112">私人集區設定</span><span class="sxs-lookup"><span data-stu-id="f1160-112">Private Pool Setup</span></span>](private-pool-setup.md)<br/>                       | <span data-ttu-id="f1160-113">包含安裝程式主控台專案。</span><span class="sxs-lookup"><span data-stu-id="f1160-113">Contains the setup console project.</span></span><br/>                                                       |
| [<span data-ttu-id="f1160-114">私用集區身分識別</span><span class="sxs-lookup"><span data-stu-id="f1160-114">Private Pool Identity</span></span>](private-pool-identity.md)<br/>                 | <span data-ttu-id="f1160-115">包含識別主控台專案。</span><span class="sxs-lookup"><span data-stu-id="f1160-115">Contains the identification console project.</span></span><br/>                                              |
| [<span data-ttu-id="f1160-116">私人集區註冊</span><span class="sxs-lookup"><span data-stu-id="f1160-116">Private Pool Enrollment</span></span>](private-pool-enrollment.md)<br/>             | <span data-ttu-id="f1160-117">包含註冊主控台專案。</span><span class="sxs-lookup"><span data-stu-id="f1160-117">Contains the enrollment console project.</span></span><br/>                                                  |
| [<span data-ttu-id="f1160-118">私用集區 Helper 函數</span><span class="sxs-lookup"><span data-stu-id="f1160-118">Private Pool Helper Functions</span></span>](private-pool-helper-functions.md)<br/> | <span data-ttu-id="f1160-119">包含安裝、識別和註冊主控台專案的 helper 函數。</span><span class="sxs-lookup"><span data-stu-id="f1160-119">Contains helper functions for the setup, identification, and enrollment console projects.</span></span><br/> |
| [<span data-ttu-id="f1160-120">建立用戶端應用程式</span><span class="sxs-lookup"><span data-stu-id="f1160-120">Create client applications</span></span>](creating-client-applications.md)<br/>     | <span data-ttu-id="f1160-121">如何使用 Windows 生物特徵辨識架構 API 來建立用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="f1160-121">How to use the Windows Biometric Framework API to create client applications.</span></span><br/>             |



 

 

 





