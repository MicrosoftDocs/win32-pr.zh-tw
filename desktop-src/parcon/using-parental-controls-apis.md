---
description: 使用家長監護 Api
ms.assetid: 3d0bb750-0882-4b95-a595-38611f161ca9
title: 使用家長監護 Api
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4ed69815bc04e00a3cae07f16530f8ea837f24a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989386"
---
# <a name="using-parental-controls-apis"></a><span data-ttu-id="cc1c5-103">使用家長監護 Api</span><span class="sxs-lookup"><span data-stu-id="cc1c5-103">Using Parental Controls APIs</span></span>

## <a name="api-selection"></a><span data-ttu-id="cc1c5-104">API 選取專案</span><span class="sxs-lookup"><span data-stu-id="cc1c5-104">API Selection</span></span>

<span data-ttu-id="cc1c5-105">如「總覽」一節所述，開發牽涉到使用最多三個 Api：</span><span class="sxs-lookup"><span data-stu-id="cc1c5-105">As noted in the overview section, development involves use of up to three APIs:</span></span>

-   <span data-ttu-id="cc1c5-106">基本設定存取：家長能控制 Wpcapi 中定義的最低相容性 COM API (合規性 API) ，以便簡單存取家長監護的主要控制項狀態子集。</span><span class="sxs-lookup"><span data-stu-id="cc1c5-106">Basic settings access: the Parental Controls minimum compliance COM API (Compliance API) defined in Wpcapi.h for simple access to a key subset of Parental Controls state.</span></span>
-   <span data-ttu-id="cc1c5-107">完整設定寫入/讀取權限：只有在 ISV 需要修改設定時，才需要使用一小部分的 WMI COM API 來進行完整存取。</span><span class="sxs-lookup"><span data-stu-id="cc1c5-107">Full settings write/read access: use of a small subset of the WMI COM API for full access is only required if the ISV needs to modify settings.</span></span> <span data-ttu-id="cc1c5-108">使用 API 的主要原因是新增 UI 擴充性連結、取代 Web 內容篩選，或新增至全電腦的 HTTP 應用程式或 URL 篩選豁免清單。</span><span class="sxs-lookup"><span data-stu-id="cc1c5-108">Addition of a UI extensibility link, replacement of the Web Content Filter, or additions to the computer-wide HTTP application or URL filtering exemption lists are the primarily reasons to use the API.</span></span> <span data-ttu-id="cc1c5-109">由於 WMI 家長監護控制項命名空間使用方式提供了基礎設定存放區的原始存取權，因此 Isv 應該在解讀其他設定的相依性時，小心地解讀個別設定的狀態。</span><span class="sxs-lookup"><span data-stu-id="cc1c5-109">As the WMI Parental Controls namespace usage provides raw access to the underlying settings store, ISVs should proceed with caution in interpreting state from individual settings that may in fact have gating dependencies on other settings.</span></span> <span data-ttu-id="cc1c5-110">因此，建議使用合規性 API 來讀取該 API 所公開之所有值的狀態。</span><span class="sxs-lookup"><span data-stu-id="cc1c5-110">It is therefore recommended to use the Compliance API for reading state for all values exposed by that API.</span></span>
-   <span data-ttu-id="cc1c5-111">記錄： Windows Vista 事件追蹤和報告系統 API (也稱為 ETW) ，可將活動事件發佈到家長監護記錄中，以及 WpcEvent 中定義的事件描述元和陣列列舉。</span><span class="sxs-lookup"><span data-stu-id="cc1c5-111">Logging: the Windows Vista Event Tracing and Reporting system API (also referred to as ETW) for publishing activity events into the Parental Controls logs, in conjunction with event descriptors and array enumerations defined in WpcEvent.h.</span></span>

<span data-ttu-id="cc1c5-112">所有 Api 都可作為標準使用者來呼叫。</span><span class="sxs-lookup"><span data-stu-id="cc1c5-112">All of the APIs are callable as a standard user.</span></span> <span data-ttu-id="cc1c5-113">若為記錄，任何使用者都可能發生來源記錄事件。</span><span class="sxs-lookup"><span data-stu-id="cc1c5-113">For logging, any user may source log events.</span></span> <span data-ttu-id="cc1c5-114">如果呼叫端沒有系統管理員許可權，呼叫以抓取或變更其他使用者的設定將會失敗。</span><span class="sxs-lookup"><span data-stu-id="cc1c5-114">Calling to retrieve or change settings for another user will fail if the caller does not have administrator privileges.</span></span> <span data-ttu-id="cc1c5-115">換句話說，標準使用者只能存取自己的設定，而且只可供閱讀。</span><span class="sxs-lookup"><span data-stu-id="cc1c5-115">In other words, a standard user can access his or her own settings only, and only for reading.</span></span>

<span data-ttu-id="cc1c5-116">這些章節將進一步討論設定和記錄 API 使用量：</span><span class="sxs-lookup"><span data-stu-id="cc1c5-116">Settings and logging API usage are discussed further in these sections:</span></span>

-   [<span data-ttu-id="cc1c5-117">使用家長監護設定 Api</span><span class="sxs-lookup"><span data-stu-id="cc1c5-117">Using Parental Controls Settings APIs</span></span>](using-parental-controls-settings-apis.md)
-   [<span data-ttu-id="cc1c5-118">使用適用于家長監護的記錄 Api</span><span class="sxs-lookup"><span data-stu-id="cc1c5-118">Using Logging APIs for Parental Controls</span></span>](using-logging-apis-for-parental-controls.md)

## <a name="development-environment"></a><span data-ttu-id="cc1c5-119">開發環境</span><span class="sxs-lookup"><span data-stu-id="cc1c5-119">Development Environment</span></span>

<span data-ttu-id="cc1c5-120">開發家長監護需要存取三個標頭檔： Wpc .h、WpcApi .h 和 WpcEvent .h。</span><span class="sxs-lookup"><span data-stu-id="cc1c5-120">Developing for Parental Controls requires access to three header files: Wpc.h, WpcApi.h, and WpcEvent.h.</span></span> <span data-ttu-id="cc1c5-121">Wpc 是一種收集器，其中包含公用合規性 API 和事件標頭的設定，因此您可以在應用程式程式碼中包含 Wpc。</span><span class="sxs-lookup"><span data-stu-id="cc1c5-121">Wpc.h is a collector that includes the settings public compliance API and event headers, so it is sufficient to include Wpc.h in application code.</span></span>

<span data-ttu-id="cc1c5-122">WMI API 的讀取/寫入權限是由 Wpcsprov. mof 檔案所指定。</span><span class="sxs-lookup"><span data-stu-id="cc1c5-122">Read/write permissions to the WMI API is specified by the Wpcsprov.mof file.</span></span> <span data-ttu-id="cc1c5-123">此檔案會安裝到 Windows System32 目錄下的 WBEM 子目錄。</span><span class="sxs-lookup"><span data-stu-id="cc1c5-123">This file is installed to the WBEM subdirectory under the Windows System32 directory.</span></span>

<span data-ttu-id="cc1c5-124">Microsoft Windows 軟體開發套件 (SDK) 包含範例程式碼，以強化此處顯示的範例程式碼，並提供簡單的命令列導向工具來進行 API 探索或整合測試。</span><span class="sxs-lookup"><span data-stu-id="cc1c5-124">The Microsoft Windows Software Development Kit (SDK) contains sample code to reinforce example code shown here and provide simple command-line driven tools for API exploration or integration testing.</span></span>

 

 



