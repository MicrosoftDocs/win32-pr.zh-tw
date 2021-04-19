---
description: 家長監護 API 總覽
ms.assetid: 647e5df8-7c6d-466a-a3d4-eac13efa797d
title: 家長監護 API 總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0aa88592f2262b89f98cfd5baaac5ad2f35f959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978155"
---
# <a name="parental-controls-api-overview"></a><span data-ttu-id="a4726-103">家長監護 API 總覽</span><span class="sxs-lookup"><span data-stu-id="a4726-103">Parental Controls API Overview</span></span>

<span data-ttu-id="a4726-104">用於家長監護的 Api 會公開原則和內建限制設定，以及記錄功能。</span><span class="sxs-lookup"><span data-stu-id="a4726-104">APIs used for Parental Controls expose the policy and in-box restrictions settings, and logging functionality.</span></span>

## <a name="settings"></a><span data-ttu-id="a4726-105">設定</span><span class="sxs-lookup"><span data-stu-id="a4726-105">Settings</span></span>

<span data-ttu-id="a4726-106">提供兩個公用 Api：</span><span class="sxs-lookup"><span data-stu-id="a4726-106">Two public APIs are provided:</span></span>

-   <span data-ttu-id="a4726-107">輕量以 COM 為基礎的最小合規性 API (稱為「合規性 API」，) 主要是讓應用程式判斷是否應該開啟記錄。</span><span class="sxs-lookup"><span data-stu-id="a4726-107">A lightweight COM-based minimum compliance API (called the Compliance API) primarily for applications to determine whether logging should be turned on.</span></span> <span data-ttu-id="a4726-108">此外，還提供簡單的方法：</span><span class="sxs-lookup"><span data-stu-id="a4726-108">In addition, simple methods are provided for:</span></span>
    -   <span data-ttu-id="a4726-109">正在為 web 限制、時間限制、遊戲限制和應用程式限制，取得限制狀態。</span><span class="sxs-lookup"><span data-stu-id="a4726-109">Retrieving the restrictions state for web restrictions, time limits, games restrictions, and application restrictions.</span></span>
    -   <span data-ttu-id="a4726-110">正在抓取主動式 Web 內容篩選器的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a4726-110">Retrieving the ID of the active Web content filter.</span></span>
    -   <span data-ttu-id="a4726-111">決定是否應該顯示廠商使用者介面專案，與加入網域時的內建隱藏方式一致。</span><span class="sxs-lookup"><span data-stu-id="a4726-111">Determining whether vendor user interface elements should be shown, in a manner consistent with the in-box hiding when joined to a domain.</span></span>
    -   <span data-ttu-id="a4726-112">上次為使用者變更設定的時間。</span><span class="sxs-lookup"><span data-stu-id="a4726-112">Retrieving the last time a setting has been changed for a user.</span></span>
    -   <span data-ttu-id="a4726-113">抓取是否需要封鎖使用者的瀏覽器型或類似瀏覽器的檔案下載，以及要求該使用者的 Web 內容篩選器特別允許 URL 的能力。</span><span class="sxs-lookup"><span data-stu-id="a4726-113">Retrieving whether browser-based or browser-like file downloads need to be blocked for a user, and the ability to request a URL to be specifically allowed by the Web Content Filter for that user.</span></span>
    -   <span data-ttu-id="a4726-114">判斷使用者是否封鎖指定的遊戲。</span><span class="sxs-lookup"><span data-stu-id="a4726-114">Determining whether a given game is blocked for a user.</span></span>
-   <span data-ttu-id="a4726-115">Windows Management Instrumentation (的 WMI) API 存取家長監護命名空間，以完整寫入和讀取所有公開設定的存取權。</span><span class="sxs-lookup"><span data-stu-id="a4726-115">Windows Management Instrumentation (WMI) API access to a Parental Controls namespace for full write and read access to all exposed settings.</span></span> <span data-ttu-id="a4726-116">家長監護會部署 WMI 提供者，以管理基礎設定存放區的讀取/寫入權限，並適當地強制執行系統管理員和受控制使用者的許可權。</span><span class="sxs-lookup"><span data-stu-id="a4726-116">Parental Controls deploys a WMI Provider to manage read/write permissions to the underlying settings store with proper enforcement of privileges for administrators and controlled users.</span></span>

<span data-ttu-id="a4726-117">Isv 會要求使用合規性 API，並視需要使用 WMI API，根據應用程式或解決方案的功能來控制適用于子安全性的限制。</span><span class="sxs-lookup"><span data-stu-id="a4726-117">ISVs are requested to use the Compliance API, and the WMI API as necessary, to control restrictions as appropriate for child safety based on the functionality of the application or solution.</span></span>

## <a name="logging"></a><span data-ttu-id="a4726-118">記錄</span><span class="sxs-lookup"><span data-stu-id="a4726-118">Logging</span></span>

-   <span data-ttu-id="a4726-119">Windows standard 事件發佈和取用 Api 用於家長監護活動監視。</span><span class="sxs-lookup"><span data-stu-id="a4726-119">Windows standard event publishing and consuming APIs are used for Parental Controls activity monitoring.</span></span> <span data-ttu-id="a4726-120">Windows Vista 附隨報告和追蹤系統改進了先前 Windows (ETW) 功能事件追蹤的效能。</span><span class="sxs-lookup"><span data-stu-id="a4726-120">The Windows Vista Event Reporting and Tracing system has improved performance over previous Event Tracing for Windows (ETW) functionality.</span></span> <span data-ttu-id="a4726-121">家長監護會在 ETW 中定義其資料的唯一通道。</span><span class="sxs-lookup"><span data-stu-id="a4726-121">Parental Controls defines a unique channel for its data in ETW.</span></span>
-   <span data-ttu-id="a4726-122">Isv 要求使用事件發佈 API 來記錄使用者活動，如使用家長監護 Api 一節中所指定。</span><span class="sxs-lookup"><span data-stu-id="a4726-122">ISVs are requested to use the event publishing API to log user activity as specified in the Using Parental Controls APIs section.</span></span>

 

 



