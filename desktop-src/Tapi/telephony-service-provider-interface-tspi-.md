---
description: 電話語音服務提供者 (TSPI) 處理通訊程式設計的裝置特定控制項。
ms.assetid: da54e219-9adb-4a12-baab-52f2b2fb7c66
title: '電話語音服務提供者介面 (TSPI) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a9d8ac4fd15fbc2685073e5954e14951f33acd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984700"
---
# <a name="telephony-service-provider-interface-tspi"></a><span data-ttu-id="20d62-103">電話語音服務提供者介面 (TSPI) </span><span class="sxs-lookup"><span data-stu-id="20d62-103">Telephony Service Provider Interface (TSPI)</span></span>

<span data-ttu-id="20d62-104">電話語音服務提供者 (TSPI) 處理通訊程式設計的裝置特定控制項。</span><span class="sxs-lookup"><span data-stu-id="20d62-104">A Telephony Service Provider (TSPI) handles device-specific controls for communications programming.</span></span> <span data-ttu-id="20d62-105">TSP 必須符合電話語音服務提供者 (TSPI) ，才能在 Microsoft 電話語音環境內作為服務提供者。</span><span class="sxs-lookup"><span data-stu-id="20d62-105">A TSP must conform to the Telephony Service Provider (TSPI) in order to function as a service provider within the Microsoft Telephony environment.</span></span> <span data-ttu-id="20d62-106">TSPI 會定義由通訊設備提供的電話語音服務提供者所公開的外部函數。</span><span class="sxs-lookup"><span data-stu-id="20d62-106">TSPI defines the external functions exposed by a telephony service provider supplied with communications equipment.</span></span>

<span data-ttu-id="20d62-107">TSP 作者必須熟悉 [Microsoft 電話語音總覽](./microsoft-telephony-overview.md)中的材質，其中涵蓋了一般的電話語音架構，並概述數個電話語音 api 的通用材質。</span><span class="sxs-lookup"><span data-stu-id="20d62-107">A TSP author must be familiar with the material in [Microsoft Telephony Overview](./microsoft-telephony-overview.md), which covers general telephony architecture and provides an overview of material common to several telephony APIs.</span></span> <span data-ttu-id="20d62-108">例如，本節包含會話控制作業（例如公園）的清單，其中包含每項作業的說明，並跳至相關的 TAPI 2.2、TAPI 3 和 TSPI 程式設計專案。</span><span class="sxs-lookup"><span data-stu-id="20d62-108">For example, this section contains a list of session control operations, such as Park, with descriptions of each operation and jumps to related TAPI 2.2, TAPI 3, and TSPI programming elements.</span></span>

<span data-ttu-id="20d62-109">下列總覽涵蓋 TSP 作者需求專屬的相關內容。</span><span class="sxs-lookup"><span data-stu-id="20d62-109">The following overviews cover material specific to the needs of a TSP author.</span></span> <span data-ttu-id="20d62-110">請注意，撰寫 TSP 最困難的部分是裝置和作業系統特定的詳細資料，這不在本檔的討論範圍內。</span><span class="sxs-lookup"><span data-stu-id="20d62-110">Please note that the most difficult parts of writing a TSP are device-and operating-system-specific details, which are outside the scope of this document.</span></span>

<span data-ttu-id="20d62-111">TSPI 總覽分為下列幾節：</span><span class="sxs-lookup"><span data-stu-id="20d62-111">The TSPI overview is divided into the following sections:</span></span>

-   <span data-ttu-id="20d62-112">[一般程式設計考慮](/previous-versions/windows/desktop/legacy/ms725196(v=vs.85)) 包括 DLL 需求、適當的版本處理、TAPI 執行的錯誤檢查、TSPI 函式對應至 tapi 2.2 (Tapi/C) 功能的摘要，以及 TSPI 中表示的服務層級的討論。</span><span class="sxs-lookup"><span data-stu-id="20d62-112">[General Programming Considerations](/previous-versions/windows/desktop/legacy/ms725196(v=vs.85)) covers DLL requirements, proper handling of versions, error checks performed by TAPI, a summary of how TSPI functions correspond to TAPI 2.2 (TAPI/C) functions, and a discussion of levels of service as expressed in TSPI.</span></span>
-   <span data-ttu-id="20d62-113">[電話語音服務提供者的生命週期](life-cycle-of-a-telephony-service-provider.md)包含 TSP 操作階段的高階摘要。</span><span class="sxs-lookup"><span data-stu-id="20d62-113">The [Life Cycle of a Telephony Service Provider](life-cycle-of-a-telephony-service-provider.md) contains a high-level summary of a TSP's operational phases.</span></span>
-   <span data-ttu-id="20d62-114">[裝置存取](/previous-versions/windows/desktop/legacy/ms725183(v=vs.85)) 涵蓋了 TSP 如何將裝置資訊和控制項公開到 TAPI 的基本概念。</span><span class="sxs-lookup"><span data-stu-id="20d62-114">[Device Access](/previous-versions/windows/desktop/legacy/ms725183(v=vs.85)) covers the basics of how a TSP exposes device information and controls to TAPI.</span></span>
-   <span data-ttu-id="20d62-115">[會話存取](/previous-versions/windows/desktop/legacy/ms725266(v=vs.85)) 涵蓋了 TAPI 在通訊會話期間預期的 TSP。</span><span class="sxs-lookup"><span data-stu-id="20d62-115">[Session Access](/previous-versions/windows/desktop/legacy/ms725266(v=vs.85)) covers what TAPI expects of a TSP during a communications session.</span></span>
-   <span data-ttu-id="20d62-116">[媒體存取](/previous-versions/windows/desktop/legacy/ms725240(v=vs.85)) 可針對媒體串流提供一組有限的控制項。</span><span class="sxs-lookup"><span data-stu-id="20d62-116">[Media Access](/previous-versions/windows/desktop/legacy/ms725240(v=vs.85)) provides a limited set of controls over media streams.</span></span> <span data-ttu-id="20d62-117">使用媒體服務提供者可以更精細地控制，而服務提供者的作者應該在可行時使用此 API。</span><span class="sxs-lookup"><span data-stu-id="20d62-117">Much finer control is possible through use of a media service provider, and service provider authors should use this API whenever feasible.</span></span> <span data-ttu-id="20d62-118">TSPI 會提供 TSP/MSP 配對之間的通訊。</span><span class="sxs-lookup"><span data-stu-id="20d62-118">The TSPI provides for communications between a TSP/MSP pair.</span></span>
-   <span data-ttu-id="20d62-119">[電話裝置](/previous-versions/windows/desktop/legacy/ms725257(v=vs.85)) 涵蓋的補充資訊和操作是在 TSP 處理電話組控制時公開。</span><span class="sxs-lookup"><span data-stu-id="20d62-119">[Phone Devices](/previous-versions/windows/desktop/legacy/ms725257(v=vs.85)) covers the supplemental information and operations exposed if a TSP handles phone set control.</span></span> <span data-ttu-id="20d62-120">這些作業是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="20d62-120">These operations are optional.</span></span>
-   <span data-ttu-id="20d62-121">[電話語音服務提供程式 UI DLL 介面](the-telephony-service-provider-ui-dll-interface.md) 涵蓋的特殊函式，可讓使用者直接設定 TSP 功能的許多層面。</span><span class="sxs-lookup"><span data-stu-id="20d62-121">[The Telephony Service Provider UI DLL Interface](the-telephony-service-provider-ui-dll-interface.md) cover special functions that can be implemented to allow a user to directly set many aspects of a TSP's functionality.</span></span>

<span data-ttu-id="20d62-122">如需 TSPI 程式設計項目的詳細資訊，請參閱 [TSPI 參考](tspi-reference.md) 。</span><span class="sxs-lookup"><span data-stu-id="20d62-122">Please see the [TSPI Reference](tspi-reference.md) for details of the TSPI programming elements.</span></span>

 

 
