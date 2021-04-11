---
description: 系統會根據儲存在登錄中的設定資訊來載入時間提供者。
ms.assetid: 67f79c31-9dd7-4e3f-bfe1-701b10611f91
title: 註冊時間提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a98e5e516db6b2c800c917c5e47da9bd75ba5c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849591"
---
# <a name="registering-a-time-provider"></a><span data-ttu-id="d0fbd-103">註冊時間提供者</span><span class="sxs-lookup"><span data-stu-id="d0fbd-103">Registering a Time Provider</span></span>

<span data-ttu-id="d0fbd-104">系統會根據儲存在登錄中的設定資訊來載入時間提供者。</span><span class="sxs-lookup"><span data-stu-id="d0fbd-104">The system loads a time provider based on its configuration information stored in the registry.</span></span> <span data-ttu-id="d0fbd-105">每次提供者都應建立下列登錄機碼：</span><span class="sxs-lookup"><span data-stu-id="d0fbd-105">Each time provider should create the following registry key:</span></span>

<span data-ttu-id="d0fbd-106">**HKEY \_LOCAL \_ MACHINE \\ System** \\ **CurrentControlSet** \\ **Services** \\ **W32Time** \\ **TimeProviders** \\ *ProviderName*</span><span class="sxs-lookup"><span data-stu-id="d0fbd-106">**HKEY\_LOCAL\_MACHINE\\System**\\**CurrentControlSet**\\**Services**\\**W32Time**\\**TimeProviders**\\*ProviderName*</span></span>

<span data-ttu-id="d0fbd-107">下表描述每個提供者的索引鍵中必須存在的值。</span><span class="sxs-lookup"><span data-stu-id="d0fbd-107">The following table describes the values that must exist in each provider's key.</span></span>



| <span data-ttu-id="d0fbd-108">值</span><span class="sxs-lookup"><span data-stu-id="d0fbd-108">Value</span></span>             | <span data-ttu-id="d0fbd-109">描述</span><span class="sxs-lookup"><span data-stu-id="d0fbd-109">Description</span></span>                                                                                                                                                                                                              |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0fbd-110">**DllName**</span><span class="sxs-lookup"><span data-stu-id="d0fbd-110">**DllName**</span></span>       | <span data-ttu-id="d0fbd-111">包含提供者之 DLL 的名稱。</span><span class="sxs-lookup"><span data-stu-id="d0fbd-111">The name of the DLL that contains the provider.</span></span> <span data-ttu-id="d0fbd-112">此值的類型為 **REG \_ SZ**。</span><span class="sxs-lookup"><span data-stu-id="d0fbd-112">This value has the type **REG\_SZ**.</span></span>                                                                                                                                     |
| <span data-ttu-id="d0fbd-113">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="d0fbd-113">**Enabled**</span></span>       | <span data-ttu-id="d0fbd-114">指出是否應啟動提供者。</span><span class="sxs-lookup"><span data-stu-id="d0fbd-114">Indicates whether the provider should be started.</span></span> <span data-ttu-id="d0fbd-115">如果這個值是1，則會啟動提供者。</span><span class="sxs-lookup"><span data-stu-id="d0fbd-115">If this value is 1, the provider is started.</span></span> <span data-ttu-id="d0fbd-116">否則，就不會啟動提供者。</span><span class="sxs-lookup"><span data-stu-id="d0fbd-116">Otherwise, the provider is not started.</span></span> <span data-ttu-id="d0fbd-117">此值的類型為 **REG \_ DWORD**。</span><span class="sxs-lookup"><span data-stu-id="d0fbd-117">This value has the type **REG\_DWORD**.</span></span>                                           |
| <span data-ttu-id="d0fbd-118">**InputProvider**</span><span class="sxs-lookup"><span data-stu-id="d0fbd-118">**InputProvider**</span></span> | <span data-ttu-id="d0fbd-119">指出提供者是否為輸入提供者或輸出提供者。</span><span class="sxs-lookup"><span data-stu-id="d0fbd-119">Indicates whether the provider is an input provider or an output provider.</span></span> <span data-ttu-id="d0fbd-120">如果這個值是1，則提供者是輸入提供者。</span><span class="sxs-lookup"><span data-stu-id="d0fbd-120">If this value is 1, the provider is an input provider.</span></span> <span data-ttu-id="d0fbd-121">否則，提供者就是輸出提供者。</span><span class="sxs-lookup"><span data-stu-id="d0fbd-121">Otherwise, the provider is an output provider.</span></span> <span data-ttu-id="d0fbd-122">此值的類型為 **REG \_ DWORD**。</span><span class="sxs-lookup"><span data-stu-id="d0fbd-122">This value has the type **REG\_DWORD**.</span></span> |



 

<span data-ttu-id="d0fbd-123">時間提供者管理員會列舉 **TimeProviders** 索引鍵下的索引鍵，並啟動每個啟用的提供者。</span><span class="sxs-lookup"><span data-stu-id="d0fbd-123">The time provider manager enumerates the keys under the **TimeProviders** key and starts each enabled provider.</span></span> <span data-ttu-id="d0fbd-124">提供者會在系統啟動時，以及每當有參數變更時啟動。</span><span class="sxs-lookup"><span data-stu-id="d0fbd-124">Providers are started at system startup and whenever there are parameter changes.</span></span>

<span data-ttu-id="d0fbd-125">每次提供者也可以將應用程式特定的設定資訊儲存在登錄中。</span><span class="sxs-lookup"><span data-stu-id="d0fbd-125">Each time provider can also store application-specific configuration information in the registry.</span></span>

 

 



